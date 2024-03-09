Following this guideline: https://github.com/godotengine/godot/issues/18253

Setup in Windows

1. Get latest source: `git clone https://github.com/godotengine/godot.git`

2. Install **scons** https://scons.org/doc/production/HTML/scons-user/ch01s02.html: `python -m pip install scons`

3. Set environment variable `ANDROID_HOME` then check: `echo $env:ANDROID_HOME`

4. Run build use params by [this tool](https://godot-build-options-generator.github.io/) : 

https://scons.org/doc/0.96.92/HTML/scons-man.html

https://docs.godotengine.org/en/stable/contributing/development/compiling/optimizing_for_size.html

- Original config file: `.scons_env.json`
- Custom config: create file `custom.py` at root folder of godotengine
- Full reference: https://github.com/GameSiProjects/OptimizeGodotLibSizeGuide/tree/main 

`scons platform=android target=template_release lto=full  optimize=size module_text_server_adv_enabled=no module_text_server_fb_enabled=yes disable_3d=yes disable_advanced_gui=yes verbose=yes`

5. Check build file size: open path `platform\android\java\lib\libs\release\arm64-v8a`
