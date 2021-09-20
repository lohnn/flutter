# This file is automatically processed to create .DEPS.git which is the file
# that gclient uses under git.
#
# See http://code.google.com/p/chromium/wiki/UsingGit
#
# To test manually, run:
#   python tools/deps2git/deps2git.py -o .DEPS.git -w <gclientdir>
# where <gcliendir> is the absolute path to the directory containing the
# .gclient file (the parent of 'src').
#
# Then commit .DEPS.git locally (gclient doesn't like dirty trees) and run
#   gclient sync..
# Verify the thing happened you wanted. Then revert your .DEPS.git change
# DO NOT CHECK IN CHANGES TO .DEPS.git upstream. It will be automatically
# updated by a bot when you modify this one.
#
# When adding a new dependency, please update the top-level .gitignore file
# to list the dependency's destination directory.

vars = {
  'chromium_git': 'https://chromium.googlesource.com',
  'swiftshader_git': 'https://swiftshader.googlesource.com',
  'dart_git': 'https://dart.googlesource.com',
  'flutter_git': 'https://flutter.googlesource.com',
  'fuchsia_git': 'https://fuchsia.googlesource.com',
  'github_git': 'https://github.com',
  'skia_git': 'https://skia.googlesource.com',
  # OCMock is for testing only so there is no google clone
  'ocmock_git': 'https://github.com/erikdoe/ocmock.git',
  'skia_revision': 'f62934b85a49a6a2b6ecb4812f3ba938a4d1715d',

  # WARNING: DO NOT EDIT canvaskit_cipd_instance MANUALLY
  # See `lib/web_ui/README.md` for how to roll CanvasKit to a new version.
  'canvaskit_cipd_instance': 'srPdrAoUIWOde-KMPE5S8koi64mejhae7NzvfR_7m3gC',

  # When updating the Dart revision, ensure that all entries that are
  # dependencies of Dart are also updated to match the entries in the
  # Dart SDK's DEPS file for that revision of Dart. The DEPS file for
  # Dart is: https://github.com/dart-lang/sdk/blob/master/DEPS.
  # You can use //tools/dart/create_updated_flutter_deps.py to produce
  # updated revision list of existing dependencies.
  'dart_revision': 'a0243abd09e324ca6856a9712b6244858edd78fc',

  # WARNING: DO NOT EDIT MANUALLY
  # The lines between blank lines above and below are generated by a script. See create_updated_flutter_deps.py
  'dart_boringssl_gen_rev': '7322fc15cc065d8d2957fccce6b62a509dc4d641',
  'dart_boringssl_rev': '1607f54fed72c6589d560254626909a64124f091',
  'dart_browser_launcher_rev': 'c6cc1025d6901926cf022e144ba109677e3548f1',
  'dart_clock_rev': 'a494269254ba978e7ef8f192c5f7fec3fc05b9d3',
  'dart_collection_rev': 'a4c941ab94044d118b2086a3f261c30377604127',
  'dart_devtools_rev': '2b47d9ed486479153ca2fd038000950674ed1beb',
  'dart_intl_tag': '0.17.0-nullsafety',
  'dart_linter_tag': '1.11.0',
  'dart_protobuf_rev': 'c1eb6cb51af39ccbaa1a8e19349546586a5c8e31',
  'dart_pub_rev': 'cafadd17ba285dad9ebe6d34c617bc0d70d096b3',
  'dart_resource_rev': '6b79867d0becf5395e5819a75720963b8298e9a7',
  'dart_root_certificates_rev': '692f6d6488af68e0121317a9c2c9eb393eb0ee50',
  'dart_shelf_proxy_tag': 'v1.0.0',
  'dart_shelf_static_rev': '202ec1a53c9a830c17cf3b718d089cf7eba568ad',
  'dart_watcher_rev': '3924194385fb215cef483193ed2879a618a3d69c',
  'dart_webdev_rev': '832b096c0c24798d3df46faa7b7661fe930573c2',
  'dart_webkit_inspection_protocol_rev': 'dd6fb5d8b536e19cedb384d0bbf1f5631923f1e8',

  'ocmock_tag': 'v3.7.1',

  # Build bot tooling for iOS
  'ios_tools_revision': '69b7c1b160e7107a6a98d948363772dc9caea46f',

  # Checkout Android dependencies only on platforms where we build for Android targets.
  'download_android_deps': 'host_cpu == "x64" and (host_os == "mac" or host_os == "linux")',

  # Checkout Windows dependencies only if we are building on Windows.
  'download_windows_deps' : 'host_os == "win"',

  # Checkout Linux dependencies only when building on Linux.
  'download_linux_deps': 'host_os == "linux"',

  # An LLVM backend needs LLVM binaries and headers. To avoid build time
  # increases we can use prebuilts. We don't want to download this on every
  # CQ/CI bot nor do we want the average Dart developer to incur that cost.
  # So by default we will not download prebuilts. This varible is needed in
  # the flutter engine to ensure that Dart gn has access to it as well.
  "checkout_llvm": False,
}

gclient_gn_args_file = 'src/third_party/dart/build/config/gclient_args.gni'
gclient_gn_args = [
  'checkout_llvm'
]

# Only these hosts are allowed for dependencies in this DEPS file.
# If you need to add a new host, contact chrome infrastructure team.
allowed_hosts = [
  'chromium.googlesource.com',
  'flutter.googlesource.com',
  'fuchsia.googlesource.com',
  'github.com',
  'skia.googlesource.com',
]

deps = {
  'src': 'https://github.com/flutter/buildroot.git' + '@' + '35c9dfd7d0950ab540ec98fadb1036e122ee3d38',

   # Fuchsia compatibility
   #
   # The dependencies in this section should match the layout in the Fuchsia gn
   # build. Eventually, we'll manage these dependencies together with Fuchsia
   # and not have to specific specific hashes.

  'src/third_party/benchmark':
   Var('fuchsia_git') + '/third_party/benchmark' + '@' + 'a779ffce872b4c811beef482e18bd0b63626aa42',

  'src/third_party/rapidjson':
   Var('fuchsia_git') + '/third_party/rapidjson' + '@' + 'ef3564c5c8824989393b87df25355baf35ff544b',

  'src/third_party/harfbuzz':
   Var('fuchsia_git') + '/third_party/harfbuzz' + '@' + '9a15acd28cf9c62a5820b6ed1013c4a7f8717d8c',

  'src/third_party/libcxx':
   Var('fuchsia_git') + '/third_party/libcxx' + '@' + '7524ef50093a376f334a62a7e5cebf5d238d4c99',

  'src/third_party/libcxxabi':
   Var('fuchsia_git') + '/third_party/libcxxabi' + '@' + '74d1e602c76350f0760bf6907910e4f3a4fccffe',

  'src/third_party/glfw':
   Var('fuchsia_git') + '/third_party/glfw' + '@' + '999f3556fdd80983b10051746264489f2cb1ef16',

  'src/third_party/shaderc':
   Var('github_git') + '/google/shaderc.git' + '@' + '948660cccfbbc303d2590c7f44a4cee40b66fdd6',

  'src/third_party/glslang':
   Var('github_git') + '/KhronosGroup/glslang.git' + '@' + '9431c53c84c14fa9e9cd37678262ebba55c62c87',

  'src/third_party/spirv_tools':
   Var('github_git') + '/KhronosGroup/SPIRV-Tools.git' + '@' + '1020e394cb1267332d58497150d2b024371a8e41',

  'src/third_party/spirv_headers':
   Var('github_git') + '/KhronosGroup/SPIRV-Headers.git' + '@' + '85b7e00c7d785962ffe851a177c84353d037dcb6',

  'src/third_party/spirv_cross':
   Var('github_git') + '/KhronosGroup/SPIRV-Cross.git' + '@' + '418542eaefdb609f548d25a1e3962fb69d80da63',


   # Chromium-style
   #
   # As part of integrating with Fuchsia, we should eventually remove all these
   # Chromium-style dependencies.

  'src/ios_tools':
   Var('chromium_git') + '/chromium/src/ios.git' + '@' + Var('ios_tools_revision'),

  'src/third_party/icu':
   Var('chromium_git') + '/chromium/deps/icu.git' + '@' + 'a38aef9142ace942a8bf166020c569f4cda0f8d3',

  'src/third_party/khronos':
   Var('chromium_git') + '/chromium/src/third_party/khronos.git' + '@' + '7122230e90547962e0f0c627f62eeed3c701f275',

  'src/third_party/googletest':
   Var('github_git') + '/google/googletest' + '@' + 'f5e592d8ee5ffb1d9af5be7f715ce3576b8bf9c4',

  'src/third_party/boringssl':
   Var('github_git') + '/dart-lang/boringssl_gen.git' + '@' + Var('dart_boringssl_gen_rev'),

  'src/third_party/boringssl/src':
   'https://boringssl.googlesource.com/boringssl.git' + '@' + Var('dart_boringssl_rev'),

  'src/third_party/dart':
   Var('dart_git') + '/sdk.git' + '@' + Var('dart_revision'),

  # WARNING: Unused Dart dependencies in the list below till "WARNING:" marker are removed automatically - see create_updated_flutter_deps.py.

  'src/third_party/dart/third_party/devtools':
   {'packages': [{'version': 'git_revision:2b47d9ed486479153ca2fd038000950674ed1beb', 'package': 'dart/third_party/flutter/devtools'}], 'dep_type': 'cipd'},

  'src/third_party/dart/third_party/pkg/args':
   Var('dart_git') + '/args.git@3b3f55766af13d895d2020ec001a28e8dc147f91',

  'src/third_party/dart/third_party/pkg/async':
   Var('dart_git') + '/async.git@c64220396e0fa2f7b380590abfedbd25635cd7a0',

  'src/third_party/dart/third_party/pkg/bazel_worker':
   Var('dart_git') + '/bazel_worker.git@0885637b037979afbf5bcd05fd748b309fd669c0',

  'src/third_party/dart/third_party/pkg/boolean_selector':
   Var('dart_git') + '/boolean_selector.git@665e6921ab246569420376f827bff4585dff0b14',

  'src/third_party/dart/third_party/pkg/browser_launcher':
   Var('dart_git') + '/browser_launcher.git' + '@' + Var('dart_browser_launcher_rev'),

  'src/third_party/dart/third_party/pkg/charcode':
   Var('dart_git') + '/charcode.git@84ea427711e24abf3b832923959caa7dd9a8514b',

  'src/third_party/dart/third_party/pkg/cli_util':
   Var('dart_git') + '/cli_util.git@8c504de5deb08fe32ecf51f9662bb37d8c708e57',

  'src/third_party/dart/third_party/pkg/clock':
   Var('dart_git') + '/clock.git' + '@' + Var('dart_clock_rev'),

  'src/third_party/dart/third_party/pkg/collection':
   Var('dart_git') + '/collection.git' + '@' + Var('dart_collection_rev'),

  'src/third_party/dart/third_party/pkg/convert':
   Var('dart_git') + '/convert.git@e063fdca4bebffecbb5e6aa5525995120982d9ce',

  'src/third_party/dart/third_party/pkg/crypto':
   Var('dart_git') + '/crypto.git@b5024e4de2b1c474dd558bef593ddbf0bfade152',

  'src/third_party/dart/third_party/pkg/csslib':
   Var('dart_git') + '/csslib.git@6338de25a09d098a62c9a1992c175e9ceb5b994a',

  'src/third_party/dart/third_party/pkg/dartdoc':
   Var('dart_git') + '/dartdoc.git@7fd237db737752800505eff510bf3fa8d3e00eb7',

  'src/third_party/dart/third_party/pkg/ffi':
   Var('dart_git') + '/ffi.git@4dd32429880a57b64edaf54c9d5af8a9fa9a4ffb',

  'src/third_party/dart/third_party/pkg/file':
   Var('dart_git') + '/external/github.com/google/file.dart/@0e09370f581ab6388d46fda4cdab66638c0171a1',

  'src/third_party/dart/third_party/pkg/fixnum':
   Var('dart_git') + '/fixnum.git@16d3890c6dc82ca629659da1934e412292508bba',

  'src/third_party/dart/third_party/pkg/glob':
   Var('dart_git') + '/glob.git@a62acf590598f458d3198d9f2930c1c9dd4b1379',

  'src/third_party/dart/third_party/pkg/html':
   Var('dart_git') + '/html.git@00cd3c22dac0e68e6ed9e7e4945101aedb1b3109',

  'src/third_party/dart/third_party/pkg/http':
   Var('dart_git') + '/http.git@778174bca2c13becd88ef3353309190b1e8b9479',

  'src/third_party/dart/third_party/pkg/http_multi_server':
   Var('dart_git') + '/http_multi_server.git@de1b312164c24a1690b46c6e97bd47eff40c4649',

  'src/third_party/dart/third_party/pkg/http_parser':
   Var('dart_git') + '/http_parser.git@202391286ddc13c4c3c284ac5b511f04697250ed',

  'src/third_party/dart/third_party/pkg/intl':
   Var('dart_git') + '/intl.git' + '@' + Var('dart_intl_tag'),

  'src/third_party/dart/third_party/pkg/json_rpc_2':
   Var('dart_git') + '/json_rpc_2.git@7e00f893440a72de0637970325e4ea44bd1e8c8e',

  'src/third_party/dart/third_party/pkg/linter':
   Var('dart_git') + '/linter.git' + '@' + Var('dart_linter_tag'),

  'src/third_party/dart/third_party/pkg/logging':
   Var('dart_git') + '/logging.git@575781ef196e4fed4fb737e38fb4b73d62727187',

  'src/third_party/dart/third_party/pkg/markdown':
   Var('dart_git') + '/markdown.git@9c4beaac96d8f008078e00b027915f81b665d2de',

  'src/third_party/dart/third_party/pkg/matcher':
   Var('dart_git') + '/matcher.git@6ba4a6d68bdfacff3d572c9ea98333dfc66fd6bf',

  'src/third_party/dart/third_party/pkg/mime':
   Var('dart_git') + '/mime.git@c931f4bed87221beaece356494b43731445ce7b8',

  'src/third_party/dart/third_party/pkg/mockito':
   Var('dart_git') + '/mockito.git@d39ac507483b9891165e422ec98d9fb480037c8b',

  'src/third_party/dart/third_party/pkg/oauth2':
   Var('dart_git') + '/oauth2.git@7cd3284049fe5badbec9f2bea2afc41d14c01057',

  'src/third_party/dart/third_party/pkg/path':
   Var('dart_git') + '/path.git@c20d73c3516d3a0061c90f14b761ff532b9bf707',

  'src/third_party/dart/third_party/pkg/pedantic':
   Var('dart_git') + '/pedantic.git@66f2f6c27581c7936482e83be80b27be2719901c',

  'src/third_party/dart/third_party/pkg/pool':
   Var('dart_git') + '/pool.git@7abe634002a1ba8a0928eded086062f1307ccfae',

  'src/third_party/dart/third_party/pkg/protobuf':
   Var('dart_git') + '/protobuf.git' + '@' + Var('dart_protobuf_rev'),

  'src/third_party/dart/third_party/pkg/pub':
   Var('dart_git') + '/pub.git' + '@' + Var('dart_pub_rev'),

  'src/third_party/dart/third_party/pkg/pub_semver':
   Var('dart_git') + '/pub_semver.git@a43ad72fb6b7869607581b5fedcb186d1e74276a',

  'src/third_party/dart/third_party/pkg/resource':
   Var('dart_git') + '/resource.git' + '@' + Var('dart_resource_rev'),

  'src/third_party/dart/third_party/pkg/shelf':
   Var('dart_git') + '/shelf.git@46483f896cc4308ee3d8e997030ae799b72aa16a',

  'src/third_party/dart/third_party/pkg/shelf_packages_handler':
   Var('dart_git') + '/shelf_packages_handler.git@78302e67c035047e6348e692b0c1182131f0fe35',

  'src/third_party/dart/third_party/pkg/shelf_proxy':
   Var('dart_git') + '/shelf_proxy.git' + '@' + Var('dart_shelf_proxy_tag'),

  'src/third_party/dart/third_party/pkg/shelf_static':
   Var('dart_git') + '/shelf_static.git' + '@' + Var('dart_shelf_static_rev'),

  'src/third_party/dart/third_party/pkg/shelf_web_socket':
   Var('dart_git') + '/shelf_web_socket.git@24fb8a04befa75a94ac63a27047b231d1a22aab4',

  'src/third_party/dart/third_party/pkg/source_map_stack_trace':
   Var('dart_git') + '/source_map_stack_trace.git@1c3026f69d9771acf2f8c176a1ab750463309cce',

  'src/third_party/dart/third_party/pkg/source_maps':
   Var('dart_git') + '/source_maps.git@53eb92ccfe6e64924054f83038a534b959b12b3e',

  'src/third_party/dart/third_party/pkg/source_span':
   Var('dart_git') + '/source_span.git@1be3c44045a06dff840d2ed3a13e6082d7a03a23',

  'src/third_party/dart/third_party/pkg/sse':
   Var('dart_git') + '/sse.git@9084339389eb441d0c0518cddac211a097e78657',

  'src/third_party/dart/third_party/pkg/stack_trace':
   Var('dart_git') + '/stack_trace.git@6788afc61875079b71b3d1c3e65aeaa6a25cbc2f',

  'src/third_party/dart/third_party/pkg/stream_channel':
   Var('dart_git') + '/stream_channel.git@d7251e61253ec389ee6e045ee1042311bced8f1d',

  'src/third_party/dart/third_party/pkg/string_scanner':
   Var('dart_git') + '/string_scanner.git@1b63e6e5db5933d7be0a45da6e1129fe00262734',

  'src/third_party/dart/third_party/pkg/term_glyph':
   Var('dart_git') + '/term_glyph.git@6a0f9b6fb645ba75e7a00a4e20072678327a0347',

  'src/third_party/dart/third_party/pkg/test':
   Var('dart_git') + '/test.git@099dcc4d052a30c6921489cfbefa1c8531d12975',

  'src/third_party/dart/third_party/pkg/test_reflective_loader':
   Var('dart_git') + '/test_reflective_loader.git@fcfce37666672edac849d2af6dffc0f8df236a94',

  'src/third_party/dart/third_party/pkg/typed_data':
   Var('dart_git') + '/typed_data.git@29ce5a92b03326d0b8035916ac04f528874994bd',

  'src/third_party/dart/third_party/pkg/usage':
   Var('dart_git') + '/usage.git@e0780cd8b2f8af69a28dc52678ffe8492da27d06',

  'src/third_party/dart/third_party/pkg/watcher':
   Var('dart_git') + '/watcher.git' + '@' + Var('dart_watcher_rev'),

  'src/third_party/dart/third_party/pkg/web_socket_channel':
   Var('dart_git') + '/web_socket_channel.git@6448ce532445a8a458fa191d9346df071ae0acad',

  'src/third_party/dart/third_party/pkg/webdev':
   Var('dart_git') + '/webdev.git' + '@' + Var('dart_webdev_rev'),

  'src/third_party/dart/third_party/pkg/webkit_inspection_protocol':
   Var('dart_git') + '/external/github.com/google/webkit_inspection_protocol.dart.git' + '@' + Var('dart_webkit_inspection_protocol_rev'),

  'src/third_party/dart/third_party/pkg/yaml':
   Var('dart_git') + '/yaml.git@2af44871f684c89e973a96e39026b8b88dda1987',

  'src/third_party/dart/third_party/pkg_tested/dart_style':
   Var('dart_git') + '/dart_style.git@14d9b6fd58cc4744676c12be3cc5eee2a779db82',

  'src/third_party/dart/third_party/pkg_tested/package_config':
   Var('dart_git') + '/package_config.git@fb736aa12316dd2d882b202a438a6946a4b4bea0',

  'src/third_party/dart/tools/sdks':
   {'packages': [{'version': 'version:2.15.0-82.0.dev', 'package': 'dart/dart-sdk/${{platform}}'}], 'dep_type': 'cipd'},

  # WARNING: end of dart dependencies list that is cleaned up automatically - see create_updated_flutter_deps.py.

  'src/third_party/colorama/src':
   Var('chromium_git') + '/external/colorama.git' + '@' + '799604a1041e9b3bc5d2789ecbd7e8db2e18e6b8',

  'src/third_party/expat':
   Var('flutter_git') + '/third_party/expat' + '@' + '1441fc5252746e53b285d15be7e65e4cd74d97eb',

  'src/third_party/freetype2':
   Var('flutter_git') + '/third_party/freetype2' + '@' + '1f03c1b2d7f2ae832a4fbe9d12bd96c3c15bbece',

  'src/third_party/root_certificates':
   Var('dart_git') + '/root_certificates.git' + '@' + Var('dart_root_certificates_rev'),

  'src/third_party/skia':
   Var('skia_git') + '/skia.git' + '@' +  Var('skia_revision'),

  'src/third_party/ocmock':
   Var('ocmock_git') + '@' +  Var('ocmock_tag'),

  'src/third_party/libjpeg-turbo':
   Var('fuchsia_git') + '/third_party/libjpeg-turbo' + '@' + '0fb821f3b2e570b2783a94ccd9a2fb1f4916ae9f',

  'src/third_party/libpng':
   Var('flutter_git') + '/third_party/libpng' + '@' + '45c760458b4a83d567cc42d21bd79a3b3fe21815',

  'src/third_party/libwebp':
   Var('chromium_git') + '/webm/libwebp.git' + '@' + '1.2.0',

  'src/third_party/wuffs':
   Var('skia_git') + '/external/github.com/google/wuffs.git' + '@' +  '1b9a6cb85b9f359595bd264d4c95da5d1291adc5',

  'src/third_party/fontconfig/src':
   Var('chromium_git') + '/external/fontconfig.git' + '@' + 'c336b8471877371f0190ba06f7547c54e2b890ba',

  'src/third_party/pyyaml':
   Var('fuchsia_git') + '/third_party/pyyaml.git' + '@' + '25e97546488eee166b1abb229a27856cecd8b7ac',

   # Upstream Khronos Vulkan Headers (v1.1.91)
   'src/third_party/vulkan':
   Var('github_git') + '/KhronosGroup/Vulkan-Docs.git' + '@' + 'v1.1.91',

   # Downstream Fuchsia Vulkan Headers (v1.2.174)
  'src/third_party/fuchsia-vulkan':
   Var('fuchsia_git') + '/third_party/Vulkan-Headers.git' + '@' + '0255987d2457576907f046c6d52b89bc6131981d',

   'src/third_party/swiftshader':
   Var('swiftshader_git') + '/SwiftShader.git' + '@' + '5d1e8540407c138f47028d64684f3da599430aa4',

   'src/third_party/angle':
   Var('github_git') + '/google/angle.git' + '@' + '06d194e2ae7b1d7e0eda0c0c911eff92dec7d3d1',

   'src/third_party/angle/third_party/vulkan-deps/vulkan-headers/src':
   Var('fuchsia_git') + '/third_party/Vulkan-Headers.git' + '@' + '5de4e8fab88ef0bd6994d9ddbcc864e3179b9e79',

   'src/third_party/abseil-cpp':
   Var('chromium_git') + '/chromium/src/third_party/abseil-cpp.git' + '@' + '2d8c1340f0350828f1287c4eaeebefcf317bcfc9',

   # Dart packages
  'src/third_party/pkg/archive':
  Var('github_git') + '/brendan-duncan/archive.git' + '@' + '3.1.2',

  'src/third_party/pkg/equatable':
  Var('github_git') + '/felangel/equatable.git' + '@' + '0ba67c72db8bed75877fc1caafa74112ee0bd921', # 2.0.2

  'src/third_party/pkg/file':
  Var('github_git') + '/google/file.dart.git' + '@' + '427bb20ccc852425d67f2880da2a9b4707c266b4', # 6.1.0

  'src/third_party/pkg/flutter_packages':
  Var('github_git') + '/flutter/packages.git' + '@' + '5617d089f26dd52da3bf05c9fa4620ef11a7419b', # various

  'src/third_party/pkg/gcloud':
  Var('github_git') + '/dart-lang/gcloud.git' + '@' + '92a33a9d95ea94a4354b052a28b98088d660e0e7', # 0.8.0-dev

  'src/third_party/pkg/googleapis':
  Var('github_git') + '/google/googleapis.dart.git' + '@' + '07f01b7aa6985e4cafd0fd4b98724841bc9e85a1', # various

  'src/third_party/pkg/platform':
  Var('github_git') + '/google/platform.dart.git' + '@' + 'f63fd0bc3021354a0687dc935962c9acc003f47e', # 3.0.1

  'src/third_party/pkg/process':
  Var('github_git') + '/google/process.dart.git' + '@' + '0c9aeac86dcc4e3a6cf760b76fed507107e244d5', # 4.2.1

  'src/third_party/pkg/process_runner':
  Var('github_git') + '/google/process_runner.git' + '@' + 'd632ea0bfd814d779fcc53a361ed33eaf3620a0b', # 4.0.1

  'src/third_party/pkg/vector_math':
  Var('github_git') + '/google/vector_math.dart.git' + '@' + 'v2.1.0',

  'src/third_party/pkg/when':
  Var('dart_git') + '/when.git' + '@' + '0.2.0',

  'src/gradle': {
    'packages': [
      {
        'version': 'version:7.0.2',
        'package': 'flutter/gradle'
      }
    ],
    'condition': 'download_android_deps',
    'dep_type': 'cipd'
  },

  'src/third_party/android_tools/ndk': {
     'packages': [
       {
        'package': 'flutter/android/ndk/${{platform}}',
        'version': 'version:r22.0.7026061'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

   'src/third_party/android_tools/google-java-format': {
     'packages': [
       {
        'package': 'flutter/android/google-java-format',
        'version': 'version:1.7-1'
       }
     ],
     # We want to be able to format these as part of CI, and the CI step that
     # checks formatting runs without downloading the rest of the Android build
     # tooling. Therefore unlike all the other Android-related tools, we want to
     # download this every time.
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/build-tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/build-tools/${{platform}}',
        'version': 'version:31.0.0S'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/platform-tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/platform-tools/${{platform}}',
        'version': 'version:31.0.2S'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/platforms': {
     'packages': [
       {
        'package': 'flutter/android/sdk/platforms',
        'version': 'version:31S'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/tools/${{platform}}',
        'version': 'version:26.1.1'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools/sdk/cmdline-tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/cmdline-tools',
        'version': 'latest',
       }
     ],
    'condition': 'download_android_deps',
    'dep_type': 'cipd',
  },

  'src/third_party/android_tools/sdk/licenses': {
     'packages': [
       {
        'package': 'flutter/android/sdk/licenses',
        'version': 'latest',
       }
     ],
    'condition': 'download_android_deps',
    'dep_type': 'cipd',
  },

  'src/third_party/android_embedding_dependencies': {
     'packages': [
       {
        'package': 'flutter/android/embedding_bundle',
        'version': 'last_updated:2021-08-10T22:12:57-0700'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/web_dependencies': {
     'packages': [
       {
         'package': 'flutter/web/canvaskit_bundle',
         'version': Var('canvaskit_cipd_instance')
       }
     ],
     'dep_type': 'cipd',
   },

  'src/third_party/java/openjdk': {
     'packages': [
       {
        'package': 'flutter/java/openjdk/${{platform}}',
        'version': 'version:11'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/flutter/third_party/gn': {
    'packages': [
      {
        'package': 'gn/gn/${{platform}}',
        'version': 'git_revision:24e2f7df92641de0351a96096fb2c490b2436bb8'
      },
    ],
    'dep_type': 'cipd',
  },

  # Clang on mac and linux are expected to typically be the same revision.
  # They are separated out so that the autoroller can more easily manage them.
  'src/buildtools/mac-x64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/mac-amd64',
        'version': 'OWP5QAE8i_HQjJnecLNDjqzhX6Rcuy2ujvfiQ4ZLxRkC'
      }
    ],
    'condition': 'host_os == "mac"',
    'dep_type': 'cipd',
  },

  'src/buildtools/linux-x64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/linux-amd64',
        'version': 'KK8UQefBW5faV9ukp57RggyEACXjJV3Nb5xnvHdXL8MC'
      }
    ],
    'condition': 'host_os == "linux"',
    'dep_type': 'cipd',
  },

  # TODO(fxb/4443): Remove this when Fuchsia can provide the Windows Clang Toolchain
  'src/third_party/llvm-build/Release+Asserts': {
    'packages': [
      {
        'package': 'flutter/clang/win-amd64',
        'version': 'git_revision:5ec206df8534d2dd8cb9217c3180e5ddba587393'
      }
    ],
    'condition': 'download_windows_deps',
    'dep_type': 'cipd',
  },

   # Get the SDK from https://chrome-infra-packages.appspot.com/p/fuchsia/sdk/core at the 'latest' tag
   # Get the toolchain from https://chrome-infra-packages.appspot.com/p/fuchsia/clang at the 'goma' tag

   'src/fuchsia/sdk/mac': {
     'packages': [
       {
        'package': 'fuchsia/sdk/core/mac-amd64',
        'version': 'YGOXMJb8skTtem5KE-awgkWH360A5bm2nl5kVii2cMYC'
       }
     ],
     'condition': 'host_os == "mac"',
     'dep_type': 'cipd',
   },
   'src/fuchsia/sdk/linux': {
     'packages': [
       {
        'package': 'fuchsia/sdk/core/linux-amd64',
        'version': 'a-fOk8gAq-X3A7HR7ccBBp4uvPUzHNheVnniE7qAiGcC'
       }
     ],
     'condition': 'host_os == "linux"',
     'dep_type': 'cipd',
   },

  # Windows SDK
  'src/third_party/windows_sdk': {
    'packages': [
      {
        'package': 'flutter/windows/windows-sdk',
        'version': 'build:10.0.19041.0'
      }
    ],
    'condition': 'download_windows_deps',
    'dep_type': 'cipd',
  },
  # CppWinRT tooling for UWP builds
  'src/third_party/cppwinrt': {
    'packages': [
      {
        'package': 'flutter/cppwinrt/win-amd64',
        'version': 'build:2.0.210505.3'
      }
    ],
    'condition': 'download_windows_deps',
    'dep_type': 'cipd',
  },

}

hooks = [
  {
    # Update the Windows toolchain if necessary.
    'name': 'win_toolchain',
    'condition': 'download_windows_deps',
    'pattern': '.',
    'action': ['python3', 'src/build/vs_toolchain.py', 'update'],
  },
  {
    # Ensure that we don't accidentally reference any .pyc files whose
    # corresponding .py files have already been deleted.
    'name': 'remove_stale_pyc_files',
    'pattern': 'src/tools/.*\\.py',
    'action': [
        'python3',
        'src/tools/remove_stale_pyc_files.py',
        'src/tools',
    ],
  },
  {
    'name': 'dia_dll',
    'pattern': '.',
    'condition': 'download_windows_deps',
    'action': [
      'python3',
      'src/flutter/tools/dia_dll.py',
    ],
  },
  {
    'name': 'linux_sysroot_x64',
    'pattern': '.',
    'condition': 'download_linux_deps',
    'action': [
      'python3',
      'src/build/linux/sysroot_scripts/install-sysroot.py',
      '--arch=x64'],
  },
  {
    'name': 'linux_sysroot_arm64',
    'pattern': '.',
    'condition': 'download_linux_deps',
    'action': [
      'python3',
      'src/build/linux/sysroot_scripts/install-sysroot.py',
      '--arch=arm64'],
  },
  {
    'name': 'pub get --offline',
    'pattern': '.',
    'action': [
      'python3',
      'src/flutter/tools/pub_get_offline.py',
    ]
  },
  {
    # This must run whenever the cppwinrt dependency is updated
    # to regenerate winrt headers
    'name': 'Generate winrt headers',
    'pattern': '.',
    'condition': 'download_windows_deps',
    'action': [
      'python3',
      'src/build/win/generate_winrt_headers.py',
    ]
  },
  {
    'name': 'Download prebuilt Dart SDK',
    'pattern': '.',
    'action': [
      'python3',
      'src/flutter/tools/download_dart_sdk.py',
    ]
  },
  {
    'name': 'Setup githooks',
    'pattern': '.',
    'action': [
      'python3',
      'src/flutter/tools/githooks/setup.py',
    ]
  }
]
