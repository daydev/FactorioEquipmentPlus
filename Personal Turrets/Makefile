VERSION := 0.1.0
NAME := EquipmentPlusPersonalTurrets
FACTORIO_HOME := $$HOME/bin/games/factorio

all: clean build install_mod

build:
	mkdir build/
	mkdir build/$(NAME)_$(VERSION)
	cp -R info.json data.lua prototypes graphics locale build/$(NAME)_$(VERSION)
	cd build && zip -r $(NAME)_$(VERSION).zip $(NAME)_$(VERSION)

clean:
	rm -rf build/

install_mod:
	if [ -d $(FACTORIO_HOME) ] ; \
	then \
		rm -rf $(FACTORIO_HOME)/mods/$(NAME)_$(VERSION) ; \
		cp -R build/$(NAME)_$(VERSION) $(FACTORIO_HOME)/mods ; \
fi;