TARGET = iphone:clang::13.1
include $(THEOS)/makefiles/common.mk
ARCHS = arm64 arm64e

BUNDLE_NAME = SignePrefs

SignePrefs_FILES = SIGRootListController.m KRLinkCell.m KRTableCell.m KRTwitterCell.m DuoTwitterCell.m KRLabeledSliderCell.m
SignePrefs_INSTALL_PATH = /Library/PreferenceBundles
SignePrefs_LIBRARIES = applist colorpicker
SignePrefs_FRAMEWORKS = UIKit
SignePrefs_PRIVATE_FRAMEWORKS = Preferences
SignePrefs_CFLAGS = -fobjc-arc -Wno-deprecated-declarations 

include $(THEOS_MAKE_PATH)/bundle.mk

internal-stage::
	$(ECHO_NOTHING)mkdir -p $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences$(ECHO_END)
	$(ECHO_NOTHING)cp entry.plist $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences/SignePrefs.plist$(ECHO_END)
