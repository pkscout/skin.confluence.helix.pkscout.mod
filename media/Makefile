TARGET=Textures.xbt
XBMCTEX=/Users/Shared/jenkins/workspace/OSX-64/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
ifeq (x86-osx,arm)
	$(XBMCTEX) -use_none -input . -output $(TARGET)
else
	$(XBMCTEX) -input . -output $(TARGET)

endif
$(XBMCTEX): force
	$(MAKE) -C /Users/Shared/jenkins/workspace/OSX-64/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

