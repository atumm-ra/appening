# use the rest as arguments for targets
TARGET_ARGS := $(wordlist 2,$(words $(MAKECMDGOALS)),$(MAKECMDGOALS))
$(eval $(TARGET_ARGS):;@:)

-include .env

run:
	pdm config python.use_venv true && \
	pdm install && pdm run -v appening

compile:
	pdm run pyinstaller --collect-all appening -n {{cookiecutter.project_slug}} --onefile {{cookiecutter.project_slug}}/main.py

run-bin: compile
	./dist/{{cookiecutter.project_slug}}

shell:
	eval $(pdm venv activate)

flatrun:
	flatpak-builder --force-clean --disable-cache build-dir {{cookiecutter.app_id}}.yml
	flatpak-builder --user --install --force-clean build-dir {{cookiecutter.app_id}}.yml
	flatpak run {{cookiecutter.app_id}}
