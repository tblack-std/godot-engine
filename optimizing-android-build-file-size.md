Following this guideline: https://github.com/godotengine/godot/issues/18253

Setup in Windows

1. Get latest source: `git clone https://github.com/godotengine/godot.git`
2. Install **scons** https://scons.org/doc/production/HTML/scons-user/ch01s02.html: `python -m pip install scons`
3. Set environment variable `ANDROID_HOME` then check: `echo $env:ANDROID_HOME`
4. Run build: `scons -j6 platform=android --config=force target=template_release tools=no deprecated=no minizip=no xml=no builtin_glew=no builtin_libmpcdec=no disable_3d=yes disable_advanced_gui=yes builtin_openssl=no module_openssl_enabled=no builtin_libogg=no builtin_libtheora=no builtin_libvorbis=no builtin_opus=no builtin_speex=no builtin_squish=no builtin_zlib=no module_chibi_enabled=no module_cscript_enabled=no module_dds_enabled=no module_etc1_enabled=no module_gridmap_enabled=no module_ik_enabled=no module_mpc_enabled=no module_ogg_enabled=no module_opus_enabled=no module_pbm_enabled=no module_pvr_enabled=no module_speex_enabled=no module_squish_enabled=no module_theora_enabled=no module_vorbis_enabled=no`
