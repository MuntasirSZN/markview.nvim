# Changelog

## [24.0.0](https://github.com/OXY2DEV/markview.nvim/compare/v23.1.0...v24.0.0) (2024-10-05)


### ⚠ BREAKING CHANGES

* **renderer:** Added more symbol definitions
* Added ability to detach/attach to a buffer
* name_hl for code blocks has been renamed to language_hl
* **highlights:** Fixed highlight groups for the plugin

### Features

* Ability to disable hybrid modes behavior when inside specific nodes ([7b913f9](https://github.com/OXY2DEV/markview.nvim/commit/7b913f9accb3739effdf2982789090cc570b9ec8)), closes [#154](https://github.com/OXY2DEV/markview.nvim/issues/154)
* Added a callback for split_view open ([6d4863c](https://github.com/OXY2DEV/markview.nvim/commit/6d4863c8575975e99b10c2950e06aebcdaf12ab2))
* Added a internal icon provider ([9923633](https://github.com/OXY2DEV/markview.nvim/commit/9923633fb6d029f3678311eff65c502a29e366cb))
* Added a simple code block creator and editor ([2d61f07](https://github.com/OXY2DEV/markview.nvim/commit/2d61f07d19fbf05e4247d5c974e9be0839c57657))
* Added ability to detach/attach to a buffer ([fd7fd02](https://github.com/OXY2DEV/markview.nvim/commit/fd7fd0213e3667b514b79ea18da89e86ec75734a))
* Added basic operator support ([e5fcd6a](https://github.com/OXY2DEV/markview.nvim/commit/e5fcd6a92e90ef0d22100a25c14b9877d475983b))
* Added option for setting maximum file length for rendering the entire file ([569fec1](https://github.com/OXY2DEV/markview.nvim/commit/569fec13ef831772bf898395b684c10f4a037e4d))
* **extras:** Added 2 new extra modules ([b2b2472](https://github.com/OXY2DEV/markview.nvim/commit/b2b2472cdf95139263ddcdfa6c9db789ad7a1f30))
* LaTeX parser now recognizes font commands ([fbe547c](https://github.com/OXY2DEV/markview.nvim/commit/fbe547c8ff90df2dd2040315a41e30ed5f32e7b4))
* New preset `minimal` for checkboxes ([7f675f8](https://github.com/OXY2DEV/markview.nvim/commit/7f675f891680a01fdf8d93ac72448f6aeef17d02))
* **parser:** Added support for footnotes ([1bd55e2](https://github.com/OXY2DEV/markview.nvim/commit/1bd55e21bc2def1c67bbcd94813fd4807b5d4fa5))
* **parser:** Internal link(obsidian) support ([837967f](https://github.com/OXY2DEV/markview.nvim/commit/837967f7465dcae4d30cfeda9157ed279d4b8927)), closes [#157](https://github.com/OXY2DEV/markview.nvim/issues/157)
* **renderer:** Added more symbol definitions ([963389b](https://github.com/OXY2DEV/markview.nvim/commit/963389bddf896584324a12a6f3c4d87250289131))
* **renderer:** More superscript characters for latex ([1bd55e2](https://github.com/OXY2DEV/markview.nvim/commit/1bd55e21bc2def1c67bbcd94813fd4807b5d4fa5))


### Bug Fixes

* `language` code block style has been renamed to `block` ([060a94b](https://github.com/OXY2DEV/markview.nvim/commit/060a94ba8d4d08660a40ed7ae94635c6fd410927))
* Added a checkhealth module ([b2d46d9](https://github.com/OXY2DEV/markview.nvim/commit/b2d46d945ae918978615cd07d4eb2147ef872fa7))
* Added a missing symbol to the LaTeX symbols table ([6d4863c](https://github.com/OXY2DEV/markview.nvim/commit/6d4863c8575975e99b10c2950e06aebcdaf12ab2))
* Added footnote configuration table to the default config ([d3d23cc](https://github.com/OXY2DEV/markview.nvim/commit/d3d23cc4a955a2b5bf8ee0976322868f808d06e4))
* Added highlight group for internal icons ([9230cda](https://github.com/OXY2DEV/markview.nvim/commit/9230cda6e45ecb2a741338b0fe81ffca9f06b208))
* Added highlight groups for the code block editor ([6cf12cd](https://github.com/OXY2DEV/markview.nvim/commit/6cf12cdf65aad8adc4f8d6e3c41c5b4634a26d38))
* Added missing `hybridDisable` & `hybridEnable` commands ([73b86f5](https://github.com/OXY2DEV/markview.nvim/commit/73b86f562e43b268a3f4ac4b6a21bddc63c928e2))
* Added missing overwrite option to treesitter injections ([89b65c3](https://github.com/OXY2DEV/markview.nvim/commit/89b65c35511a9039ddd326b8002f4bf739a14b99))
* Added new highlight groups ([7d2d763](https://github.com/OXY2DEV/markview.nvim/commit/7d2d763b1bd14fbbbe4ebb984cfa53d417c1c59f))
* Added support for \text{} & \set{} ([300e1fe](https://github.com/OXY2DEV/markview.nvim/commit/300e1fe3c7401d64337f28a8f64e2ffddc05ea0d)), closes [#162](https://github.com/OXY2DEV/markview.nvim/issues/162)
* Added the ability to overwrite injected queries ([4c41c66](https://github.com/OXY2DEV/markview.nvim/commit/4c41c668c12e1fe272123ed253c1e25a35474526))
* Adds the missing sign, sign_hl options for github style setext headings ([05dbce9](https://github.com/OXY2DEV/markview.nvim/commit/05dbce99c44f2f1a95ae2cbd3a74fbf6b8108f44))
* Better case handling for superscripts & subscripts ([b8eabd1](https://github.com/OXY2DEV/markview.nvim/commit/b8eabd1e0bc0175bc18fffd9312d77035c281c84))
* Changed list item & tables specification ([3724114](https://github.com/OXY2DEV/markview.nvim/commit/37241141f00a3f0763ea1ace18f522ea6e4f33f4))
* Checkbox now use the `match_string` option ([4fe3790](https://github.com/OXY2DEV/markview.nvim/commit/4fe379080564c3de6b8dcdc5c577891a066a2a82))
* Checkboxes now carry information regarding their list item ([c7385c9](https://github.com/OXY2DEV/markview.nvim/commit/c7385c9cbe7dbc9b61abf48417d5b26170496fd2))
* Default modes now contain command mode ([73b86f5](https://github.com/OXY2DEV/markview.nvim/commit/73b86f562e43b268a3f4ac4b6a21bddc63c928e2))
* Deprecated old checkbox ([afb87e6](https://github.com/OXY2DEV/markview.nvim/commit/afb87e6eb7465f4a92e61e011ef682b2be02eca8))
* Fixed a bug causing visual artifacts with tables in split view ([b2d46d9](https://github.com/OXY2DEV/markview.nvim/commit/b2d46d945ae918978615cd07d4eb2147ef872fa7))
* Fixed a bug not letting attached buffers be re-attached ([a2007c3](https://github.com/OXY2DEV/markview.nvim/commit/a2007c3aad0ca041532c44010dd1871248ac44b8))
* Fixed a bug when using hybrid mode with split view ([4273e03](https://github.com/OXY2DEV/markview.nvim/commit/4273e0372691031ecd1d1d1fb6cbb610f65a0b86))
* Fixed an issue causing hybrid mode not working with latex blocks ([207c39e](https://github.com/OXY2DEV/markview.nvim/commit/207c39ee40af0d4cd7091a53e6303a4882eba462))
* Fixed an issue causing treesitter injections to not work ([9a15f72](https://github.com/OXY2DEV/markview.nvim/commit/9a15f7202b4ff5123fdf0e9cd9e414f0cc3f4a68))
* Fixed block quote title rendering ([6d4863c](https://github.com/OXY2DEV/markview.nvim/commit/6d4863c8575975e99b10c2950e06aebcdaf12ab2))
* Fixed checkbox detection for list items ([39dd746](https://github.com/OXY2DEV/markview.nvim/commit/39dd7467e271621f97d897b09a627e20786c9f6f))
* Fixed definitions for callbacks ([b2d46d9](https://github.com/OXY2DEV/markview.nvim/commit/b2d46d945ae918978615cd07d4eb2147ef872fa7))
* Fixed extmark poaition of code blocks ([5f4e2c3](https://github.com/OXY2DEV/markview.nvim/commit/5f4e2c3c443bacb3f763f100d445d17ed521250c))
* Fixed handling of overlapping table borders ([9f7ff72](https://github.com/OXY2DEV/markview.nvim/commit/9f7ff72827e9a7d12f2662c9430245c02f3cc6f1))
* Fixed how list items are parsed ([17ed16e](https://github.com/OXY2DEV/markview.nvim/commit/17ed16ecee3b67ecc46bf4d60ba04cd35a22b883))
* Fixed incorrect annotations for callout match_string ([2b22590](https://github.com/OXY2DEV/markview.nvim/commit/2b2259009554c1fb5e312c72130e84b87ef6244c))
* Fixed incorrect cursor position on code blocks ([3abd13d](https://github.com/OXY2DEV/markview.nvim/commit/3abd13d483ece69d52e3b5883431995f6f7da5c0))
* Fixed incorrect highlight group for the ] in LaTeX brackets ([4fe3790](https://github.com/OXY2DEV/markview.nvim/commit/4fe379080564c3de6b8dcdc5c577891a066a2a82))
* Fixed incorrect option for n) type list items ([a823191](https://github.com/OXY2DEV/markview.nvim/commit/a823191375205426624a7ed147894e6df8fcffa9))
* Fixed incorrect parameter for footer rendering function ([4e0c8a1](https://github.com/OXY2DEV/markview.nvim/commit/4e0c8a1418f4a03a43842ee2f6decd1214df8473))
* Fixed incorrect width calculation of footnotes ([cc759e8](https://github.com/OXY2DEV/markview.nvim/commit/cc759e8dacc42e96b192271a1092619ae47a2558))
* Fixed indentation of treesitter injections ([9a15f72](https://github.com/OXY2DEV/markview.nvim/commit/9a15f7202b4ff5123fdf0e9cd9e414f0cc3f4a68))
* Fixed list item alignment inside of block quotes ([d28fb24](https://github.com/OXY2DEV/markview.nvim/commit/d28fb24bf47bbd646acbd73df7fe313c72c2435b))
* Fixed mathbf font support ([6d4863c](https://github.com/OXY2DEV/markview.nvim/commit/6d4863c8575975e99b10c2950e06aebcdaf12ab2))
* Fixed merge issue of highlight_groups ([4fe3790](https://github.com/OXY2DEV/markview.nvim/commit/4fe379080564c3de6b8dcdc5c577891a066a2a82))
* Fixed naming of font captures to be more flexible ([aad0149](https://github.com/OXY2DEV/markview.nvim/commit/aad0149767d2d3f1e8beb68833d9bf1c04881cbb))
* Fixed option name typo ([3036694](https://github.com/OXY2DEV/markview.nvim/commit/3036694ee55a2d386122c38baa42acab1ee085bb))
* Fixed overlapping table border issue ([f553e3f](https://github.com/OXY2DEV/markview.nvim/commit/f553e3fa04ae254c5f4d821e1e1281b57fcee652))
* Fixed presets ([3b6f737](https://github.com/OXY2DEV/markview.nvim/commit/3b6f737fd5d23bb53ece827135d382a3dccb1bd2))
* Fixed rendering of code blocks that use markdown inside them ([1f7c120](https://github.com/OXY2DEV/markview.nvim/commit/1f7c120a3fadb1cf2c55d112ff2e77d5f8a6fddf))
* Fixed rendering of list items when padding isn't used ([24ae03e](https://github.com/OXY2DEV/markview.nvim/commit/24ae03e8f80e2647e4fee5f7d4b36c78541a97e2)), closes [#163](https://github.com/OXY2DEV/markview.nvim/issues/163)
* Fixed right padding position of inline codes ([cc759e8](https://github.com/OXY2DEV/markview.nvim/commit/cc759e8dacc42e96b192271a1092619ae47a2558))
* Fixed superscript & subscript parsing ([fbe547c](https://github.com/OXY2DEV/markview.nvim/commit/fbe547c8ff90df2dd2040315a41e30ed5f32e7b4))
* Fixed typo ([6f4a7cd](https://github.com/OXY2DEV/markview.nvim/commit/6f4a7cd57e3ca4dd48ca76938a3d603f52b6be68))
* Fixed typos ([0475053](https://github.com/OXY2DEV/markview.nvim/commit/047505387e6d92669dfb23713cf95efc73f773f2))
* Fixed various bugs with extra mofules ([279040c](https://github.com/OXY2DEV/markview.nvim/commit/279040ce1173f6710a6c740483e0f5c5a484cd43))
* Fixed various typos ([a83f53e](https://github.com/OXY2DEV/markview.nvim/commit/a83f53e9c61669557abb1c00022405b3a7a731e4))
* Fixed visual glitch of headings, list items & checkboxes ([c29ce0f](https://github.com/OXY2DEV/markview.nvim/commit/c29ce0fad68db4a5879eeeadaa6e06865b3a0bf4))
* Fixed wording of annotation ([3d3ea4c](https://github.com/OXY2DEV/markview.nvim/commit/3d3ea4c42f376eb6d9cfe1dddb101c8871580e38))
* Fixed wrong amount of parameters being sent to parser function ([91302d2](https://github.com/OXY2DEV/markview.nvim/commit/91302d24cbbb7e1d39036d10c676aa59cf8a3867))
* Fixes handling of magic characters inside checkboxes ([74b5d60](https://github.com/OXY2DEV/markview.nvim/commit/74b5d60c3c53a6f12ea1c0513ecc4f332c6e7ba1)), closes [#156](https://github.com/OXY2DEV/markview.nvim/issues/156)
* Fixes wrong option name for the * list items ([4fe3790](https://github.com/OXY2DEV/markview.nvim/commit/4fe379080564c3de6b8dcdc5c577891a066a2a82))
* Heading's shift_width has been reverted to 1 ([4fe3790](https://github.com/OXY2DEV/markview.nvim/commit/4fe379080564c3de6b8dcdc5c577891a066a2a82))
* **highlights:** Fixed highlight groups for the plugin ([d7c55c6](https://github.com/OXY2DEV/markview.nvim/commit/d7c55c6a58568b0eb56936ea1bd62469b35ab350))
* **latex:** Removed unnecessary feature `brackets` ([eeb2bde](https://github.com/OXY2DEV/markview.nvim/commit/eeb2bdedfa3677f95306ac5c57971ebae85cc04d))
* Links/Images with list characters are overindented ([a55e185](https://github.com/OXY2DEV/markview.nvim/commit/a55e1853c0ccca7f570d97d74059f1b94ebab3f6))
* Made all parsers optional ([4671de6](https://github.com/OXY2DEV/markview.nvim/commit/4671de67c8c119f5c06f07fb417d9af39e399cf9))
* Made the table renderer use the new table parts spec ([1dc661e](https://github.com/OXY2DEV/markview.nvim/commit/1dc661e68d7772cecaad5e3f333c40e037172fa7))
* name_hl for code blocks has been renamed to language_hl ([05dbce9](https://github.com/OXY2DEV/markview.nvim/commit/05dbce99c44f2f1a95ae2cbd3a74fbf6b8108f44))
* Redraw autocmds are now cached ([d07ebbe](https://github.com/OXY2DEV/markview.nvim/commit/d07ebbedb2d606a5f3b8541dc2f84ad67981ad75))
* Removed `nvim-web-devicons` as a dependency for luarocks ([9c15e30](https://github.com/OXY2DEV/markview.nvim/commit/9c15e30415b73c5f79dca5a16873a2ed80e19a88)), closes [#152](https://github.com/OXY2DEV/markview.nvim/issues/152)
* Removed debug prints ([4f56916](https://github.com/OXY2DEV/markview.nvim/commit/4f5691676f592c885b7c3c59239c1ac693bce18e))
* Removed hard-coded virtual text value for LaTeX code blocks ([417490a](https://github.com/OXY2DEV/markview.nvim/commit/417490a70a4f8106a78109b4da13208916bc9632))
* Removed the message for latex support ([45b9f16](https://github.com/OXY2DEV/markview.nvim/commit/45b9f164b4cd82a5cd151c49bc3fd9495df39a96)), closes [#140](https://github.com/OXY2DEV/markview.nvim/issues/140)
* Removed useless html checker for table cells ([f91feb4](https://github.com/OXY2DEV/markview.nvim/commit/f91feb465414f0d24a86e7169f27a8011090deed)), closes [#160](https://github.com/OXY2DEV/markview.nvim/issues/160)
* Removes rendering of icons when the link starts with an emoji ([7cec2dd](https://github.com/OXY2DEV/markview.nvim/commit/7cec2ddf240ac654daeefe6012cff6fd222394fc))
* **renderer:** Added more custom links ([3f76267](https://github.com/OXY2DEV/markview.nvim/commit/3f762670cdffcc10361c6d3d467b7e0ddbdd6c7b))
* **renderer:** Deprecated "minimal" style of code blocks ([55dec1c](https://github.com/OXY2DEV/markview.nvim/commit/55dec1c0214faa31ba53562a76885656af90a762))
* **renderer:** Fixed html tag parsing ([3f76267](https://github.com/OXY2DEV/markview.nvim/commit/3f762670cdffcc10361c6d3d467b7e0ddbdd6c7b))
* **renderer:** Fixed incorrect concealmemt range for subscripts & superscripts in latex ([ba7b383](https://github.com/OXY2DEV/markview.nvim/commit/ba7b383f74fb1015fb136703f1200b25eda29bfa)), closes [#148](https://github.com/OXY2DEV/markview.nvim/issues/148)
* **renderer:** Subscript & superscripts are now more readable! ([963389b](https://github.com/OXY2DEV/markview.nvim/commit/963389bddf896584324a12a6f3c4d87250289131))
* **renderer:** Symbols now respect subscript & superscript ([963389b](https://github.com/OXY2DEV/markview.nvim/commit/963389bddf896584324a12a6f3c4d87250289131))
* Tables can now have a predefined width ([f139fab](https://github.com/OXY2DEV/markview.nvim/commit/f139fabd38aae0ea6b5ed2537b53237eae533a01))
* Transitioning from hard coded operators to more flexible node based one ([d2a879a](https://github.com/OXY2DEV/markview.nvim/commit/d2a879a79c9ec0aa8a64bae992b4ccb44b4c63ec))
* Updated config ([ea6c780](https://github.com/OXY2DEV/markview.nvim/commit/ea6c780a010fa21f2a804b23b8dc6fc55b4ac978))
* Updated config to follow newer spec ([93dc524](https://github.com/OXY2DEV/markview.nvim/commit/93dc524f99ab9a554a6f4f8390c84c91c96f32a8))
* Updated Setext heading style name ([cea88ba](https://github.com/OXY2DEV/markview.nvim/commit/cea88ba6879056104eb723e7e0d9fe7a1b9daf03))

## [23.1.0](https://github.com/OXY2DEV/markview.nvim/compare/v23.0.0...v23.1.0) (2024-09-09)


### Features

* Ability to toggle hybrid mode ([5738773](https://github.com/OXY2DEV/markview.nvim/commit/573877329dbfa2918f27e47dc5c0e92c06fe400e))


### Bug Fixes

* Added ability to hide escaped charaters ([1aa54de](https://github.com/OXY2DEV/markview.nvim/commit/1aa54de650b703d5f533494159519a9ee4a077e3)), closes [#144](https://github.com/OXY2DEV/markview.nvim/issues/144)
* Callout(s) no longer hide underlying text ([77b9b8c](https://github.com/OXY2DEV/markview.nvim/commit/77b9b8c78cf4dcfc433c37e73171f722cc0a6fe8))
* Checkboxes now hide the list markers ([d283507](https://github.com/OXY2DEV/markview.nvim/commit/d2835077de618d7215bc9aef4c3594497c72b8bf)), closes [#142](https://github.com/OXY2DEV/markview.nvim/issues/142)
* Removed the need to change callbacks to make hybrid mode work. ([5738773](https://github.com/OXY2DEV/markview.nvim/commit/573877329dbfa2918f27e47dc5c0e92c06fe400e))
* Tables now ignore (block_continuation) ([a2594d0](https://github.com/OXY2DEV/markview.nvim/commit/a2594d0df31e6b90a5302730148d535d030b1641))
* Teble renderer now can handle escaped characters ([1aa54de](https://github.com/OXY2DEV/markview.nvim/commit/1aa54de650b703d5f533494159519a9ee4a077e3))

## [23.0.0](https://github.com/OXY2DEV/markview.nvim/compare/v22.1.0...v23.0.0) (2024-09-08)


### ⚠ BREAKING CHANGES

* **renderer:** Added missing Obsidian callouts

### Features

* Added simple Latex support ([92f5320](https://github.com/OXY2DEV/markview.nvim/commit/92f53209eab8e1661cca4a2635b76a5c926d8fad)), closes [#138](https://github.com/OXY2DEV/markview.nvim/issues/138)
* **renderer:** Added missing Obsidian callouts ([ea71a5b](https://github.com/OXY2DEV/markview.nvim/commit/ea71a5bc6e0a0b28af62e2f21d264ddcc466bd51)), closes [#135](https://github.com/OXY2DEV/markview.nvim/issues/135)


### Bug Fixes

* Fixed a bug causing deleted buffers to not be removed from the attached buffers list ([e4b4b9d](https://github.com/OXY2DEV/markview.nvim/commit/e4b4b9d03b90350236ce88f5be723aa5a8610931)), closes [#137](https://github.com/OXY2DEV/markview.nvim/issues/137)
* Fixed how widths are calculated in code blocks ([59c15a2](https://github.com/OXY2DEV/markview.nvim/commit/59c15a2baec56c8fbb3f22151407978c27f389f8))
* Split view no longer loses it's state when changing plugin state with `:Markview ...` ([d6f0cb8](https://github.com/OXY2DEV/markview.nvim/commit/d6f0cb87b8cf8929fa8626f06ff0544b89eb9b7a))

## [22.1.0](https://github.com/OXY2DEV/markview.nvim/compare/v22.0.1...v22.1.0) (2024-08-31)


### Features

* Added split-view to the plugin ([308024c](https://github.com/OXY2DEV/markview.nvim/commit/308024cbcb783fe0c179a18f8e2a7b31406c8a37)), closes [#131](https://github.com/OXY2DEV/markview.nvim/issues/131)


### Bug Fixes

* Fixed a bug causing callbacks to not work. ([6641174](https://github.com/OXY2DEV/markview.nvim/commit/6641174ed030a0d7f305ce860f21097c28560fb9))
* Minor bug fixes for splitView ([3471b7b](https://github.com/OXY2DEV/markview.nvim/commit/3471b7b84b618464aed8e80f35531e5352d3869f))

## [22.0.1](https://github.com/OXY2DEV/markview.nvim/compare/v22.0.0...v22.0.1) (2024-08-28)


### Bug Fixes

* Added support for n) type number list ([a954ec8](https://github.com/OXY2DEV/markview.nvim/commit/a954ec86be1259d547d6fd9c18e8781c8c73c92f)), closes [#129](https://github.com/OXY2DEV/markview.nvim/issues/129) [#121](https://github.com/OXY2DEV/markview.nvim/issues/121)
* Custom links now inherit from `default` value ([a954ec8](https://github.com/OXY2DEV/markview.nvim/commit/a954ec86be1259d547d6fd9c18e8781c8c73c92f))

## [22.0.0](https://github.com/OXY2DEV/markview.nvim/compare/v21.0.1...v22.0.0) (2024-08-26)


### ⚠ BREAKING CHANGES

* Added the ability to use the plugin in other filetypes

### Features

* Added the ability to use the plugin in other filetypes ([e7e91ad](https://github.com/OXY2DEV/markview.nvim/commit/e7e91ad3320c8a3feabba27f5ac79953f99c2632))


### Bug Fixes

* Fixed a bug causing things not to render when scrolling short distances ([8f0b69a](https://github.com/OXY2DEV/markview.nvim/commit/8f0b69a170320c21f4b70517753ddf0aede15055))

## [21.0.1](https://github.com/OXY2DEV/markview.nvim/compare/v21.0.0...v21.0.1) (2024-08-25)


### Bug Fixes

* Fixed a bug causing markview to not render on cursor move in large files ([eba9507](https://github.com/OXY2DEV/markview.nvim/commit/eba950746173f8443b79b0b334f0c6a5d5797b55))
* Markview now assumes window width of the buffer. ([ec92e61](https://github.com/OXY2DEV/markview.nvim/commit/ec92e611419ca603aa0f1ae21ec159a7b4b82a54)), closes [#126](https://github.com/OXY2DEV/markview.nvim/issues/126)
* Markview now updats when entering the attached buffer ([87badab](https://github.com/OXY2DEV/markview.nvim/commit/87badab362d692025e717042c2ac052e7ff69fca)), closes [#126](https://github.com/OXY2DEV/markview.nvim/issues/126)
* Reduced flickering when scrolling short distances ([a1923f9](https://github.com/OXY2DEV/markview.nvim/commit/a1923f9a3ef6c0843eb95168c1ee510e2e6c86ab))

## [21.0.0](https://github.com/OXY2DEV/markview.nvim/compare/v20.1.0...v21.0.0) (2024-08-25)


### ⚠ BREAKING CHANGES

* Deprecated old presets

### Features

* Added alignment support for `label` headings ([2e0761e](https://github.com/OXY2DEV/markview.nvim/commit/2e0761ef44ffcd863898309509b5b40103aeb9c9)), closes [#124](https://github.com/OXY2DEV/markview.nvim/issues/124)
* Added support for custom hyperlinks ([03188a4](https://github.com/OXY2DEV/markview.nvim/commit/03188a4658f0c0fdc0b9dc0f9926eb4c393ca97a)), closes [#121](https://github.com/OXY2DEV/markview.nvim/issues/121)


### Bug Fixes

* Deprecated old presets ([2e0761e](https://github.com/OXY2DEV/markview.nvim/commit/2e0761ef44ffcd863898309509b5b40103aeb9c9))
* Fixed a bug causing patterns to be matched inside inline codes ([1193286](https://github.com/OXY2DEV/markview.nvim/commit/119328617657e90e775934dd53ffd6b31aae988f))
* Plugin now recognizes escaped columns ([28c70aa](https://github.com/OXY2DEV/markview.nvim/commit/28c70aa40554963cb79de80286f956edc3181bff))

## [20.1.0](https://github.com/OXY2DEV/markview.nvim/compare/v20.0.0...v20.1.0) (2024-08-21)


### Features

* Added custom checkbox states ([ff96638](https://github.com/OXY2DEV/markview.nvim/commit/ff96638f94b52a293f8479a5b99b04d583c2c4b2)), closes [#117](https://github.com/OXY2DEV/markview.nvim/issues/117)

## [20.0.0](https://github.com/OXY2DEV/markview.nvim/compare/v19.0.0...v20.0.0) (2024-08-20)


### ⚠ BREAKING CHANGES

* **renderer:** Added experimental support for lists inside block elements

### Bug Fixes

* Added experimental support for aligned checkbox desvription ([f9aba72](https://github.com/OXY2DEV/markview.nvim/commit/f9aba72c8d35ebe11eee7b4a4d7b10e92f18ec06)), closes [#107](https://github.com/OXY2DEV/markview.nvim/issues/107)
* Added option to change the indent size of list items ([d54039e](https://github.com/OXY2DEV/markview.nvim/commit/d54039e57fc6b263775a78473569f01224e2ddee)), closes [#96](https://github.com/OXY2DEV/markview.nvim/issues/96)
* Added the ability to open &lt;cfile&gt; links under cursor ([7f4639a](https://github.com/OXY2DEV/markview.nvim/commit/7f4639a53b3e3aac3ad5deab99b21097264f07cc)), closes [#97](https://github.com/OXY2DEV/markview.nvim/issues/97)
* Fixed a big casuing hybrid mode to become active on mode change ([15a49b5](https://github.com/OXY2DEV/markview.nvim/commit/15a49b532f2d79471db2c3ac2ee56e974ffb1dd4))
* Fixed a big causing highlight groups to not apply on empty config table ([1dd1d30](https://github.com/OXY2DEV/markview.nvim/commit/1dd1d3069d7f25ebefbeaf692af9f792e3414eab))
* Fixed a bug causing `callbacks` to not work on some functions ([a8e104b](https://github.com/OXY2DEV/markview.nvim/commit/a8e104badcc77534f3b4db2310545c70e28a890b)), closes [#104](https://github.com/OXY2DEV/markview.nvim/issues/104)
* Fixed a bug causing the `on_mode_changed()` callback to not fire ([cb7570b](https://github.com/OXY2DEV/markview.nvim/commit/cb7570be20acb3ad191385dee55db4e304bba42b))
* **gx:** Fixed a bug causing gx to not work with links. ([6d0bcce](https://github.com/OXY2DEV/markview.nvim/commit/6d0bcce3a74b10bcc79c04c5944bfc000381be49)), closes [#97](https://github.com/OXY2DEV/markview.nvim/issues/97)
* Made tables compatible with multi-col characters ([03290ce](https://github.com/OXY2DEV/markview.nvim/commit/03290ce2e0c9e426c53dc9a1efabd8a6ee1f4904)), closes [#42](https://github.com/OXY2DEV/markview.nvim/issues/42)
* **parser:** Added support for extra info on the code block start line ([7e0ad40](https://github.com/OXY2DEV/markview.nvim/commit/7e0ad400638b09205079693eb73307580f6303f3)), closes [#77](https://github.com/OXY2DEV/markview.nvim/issues/77)
* **parser:** Added support for labels in links ([1fc5d90](https://github.com/OXY2DEV/markview.nvim/commit/1fc5d90dbe6f8a171443b50875f7bbd794fdd607))
* Removed auto setting conceallevel & concealcursor ([798fd99](https://github.com/OXY2DEV/markview.nvim/commit/798fd991f5d163ed676877e87d8c65dc2d886cb9))
* Removed debug print for luminosity ([798fd99](https://github.com/OXY2DEV/markview.nvim/commit/798fd991f5d163ed676877e87d8c65dc2d886cb9)), closes [#101](https://github.com/OXY2DEV/markview.nvim/issues/101) [#102](https://github.com/OXY2DEV/markview.nvim/issues/102)
* **renderer:** `[]` are now counted when rendering tables ([c4f3d54](https://github.com/OXY2DEV/markview.nvim/commit/c4f3d544bd67b4ac0ebacc72091556841e81ca8b)), closes [#75](https://github.com/OXY2DEV/markview.nvim/issues/75)
* **renderer:** Added debounce to ModeChanged event ([c9fa106](https://github.com/OXY2DEV/markview.nvim/commit/c9fa1065098663c3bfe7e07656937c3d2f3dabea)), closes [#99](https://github.com/OXY2DEV/markview.nvim/issues/99) [#98](https://github.com/OXY2DEV/markview.nvim/issues/98)
* **renderer:** Added experimental support for lists inside block elements ([81c64a8](https://github.com/OXY2DEV/markview.nvim/commit/81c64a8cef523192aa084ccef469369f6ed8d7d1)), closes [#115](https://github.com/OXY2DEV/markview.nvim/issues/115)
* **renderer:** Added mode validator for hybrid_mode listeners ([c9fa106](https://github.com/OXY2DEV/markview.nvim/commit/c9fa1065098663c3bfe7e07656937c3d2f3dabea))
* **renderer:** Added option to disable top/bottom border & fixed a rendering error that occured when disabling "use_virt_lines" ([31d36e9](https://github.com/OXY2DEV/markview.nvim/commit/31d36e935fd962099fdacffe2629305e26eff8ed))
* **renderer:** Added support for language names in code blocks ([5db0e8e](https://github.com/OXY2DEV/markview.nvim/commit/5db0e8ea917d07ea1de6670cf256a4169c3d5601)), closes [#72](https://github.com/OXY2DEV/markview.nvim/issues/72)
* **renderer:** Added the filetype finding function to the code blocks renderer ([d69122d](https://github.com/OXY2DEV/markview.nvim/commit/d69122dbf3f340bd9f5dfbb55bef2f71ed65858d)), closes [#72](https://github.com/OXY2DEV/markview.nvim/issues/72)
* **renderer:** Fixed a big causing numbered lists to use virtual text ([6404094](https://github.com/OXY2DEV/markview.nvim/commit/6404094d692262bb446e2887822e2aa7d69f7efa))
* **renderer:** Fixed incorrect alignment of nested code blocks within lists ([738ddc0](https://github.com/OXY2DEV/markview.nvim/commit/738ddc0390449c0652f34b99a6cbe0699b2fcf58))
* **renderer:** Made icons optional ([6671dd4](https://github.com/OXY2DEV/markview.nvim/commit/6671dd45ea5eabbc11ba9c400b54991681e95464))
* **renderer:** Reworked hybrid_mode ([e29b7b5](https://github.com/OXY2DEV/markview.nvim/commit/e29b7b5ac6a9f238b7a3ff85042c91ba76edbda8))
* **renderer:** Table cells now respect the column count & the cell width ([a0d8a5d](https://github.com/OXY2DEV/markview.nvim/commit/a0d8a5db74107ffe91cb3cab6b3065b7baccb663)), closes [#75](https://github.com/OXY2DEV/markview.nvim/issues/75)

## [19.0.0](https://github.com/OXY2DEV/markview.nvim/compare/v18.0.0...v19.0.0) (2024-08-05)


### ⚠ BREAKING CHANGES

* **renderer:** Added support for simple html elements
* **renderer:** Support for tables that don't start at the start of the line

### Features

* Added support for HTML entites ([3b270c1](https://github.com/OXY2DEV/markview.nvim/commit/3b270c1dedbf02b4849341ff9e490a001041e248))
* **renderer:** Added basic language names to code blocks ([c9b4f77](https://github.com/OXY2DEV/markview.nvim/commit/c9b4f77e880eb0ab9afd370ad82e3758513a4a3a)), closes [#72](https://github.com/OXY2DEV/markview.nvim/issues/72)
* **renderer:** Added better validation for html tags in table cells ([ab0e54e](https://github.com/OXY2DEV/markview.nvim/commit/ab0e54e2992b3806fe2b3a68a49d050f1118159e))
* **renderer:** Added hybrid-mode support to the plugin ([4a93e15](https://github.com/OXY2DEV/markview.nvim/commit/4a93e155261508b89d5c6146ba6cc0da91be0883)), closes [#64](https://github.com/OXY2DEV/markview.nvim/issues/64)
* **renderer:** Added support for simple html elements ([94ce522](https://github.com/OXY2DEV/markview.nvim/commit/94ce522302f78167e278d3c7d82ff0206c74b4e3))
* **renderer:** Support for tables that don't start at the start of the line ([3c8b0dc](https://github.com/OXY2DEV/markview.nvim/commit/3c8b0dc5a9b02264f94137b23279db7d3198ac7a))
* replace tbl_islist to islist ([f1e66c7](https://github.com/OXY2DEV/markview.nvim/commit/f1e66c78ba28b3b2399a4b76febc42ceb3211fd1))


### Bug Fixes

* **parser:** Added logic for supporting markers inside code blocks ([a38dd1f](https://github.com/OXY2DEV/markview.nvim/commit/a38dd1f01c31b4201b4355fe8ebaa439621e5b35)), closes [#69](https://github.com/OXY2DEV/markview.nvim/issues/69)
* **parser:** Improved validation of pending checkboxes ([a6392dd](https://github.com/OXY2DEV/markview.nvim/commit/a6392ddeb627a4ebd218718bc4f80b5fca1a1803))
* **renderer:** Fixed a bug causing inconsistency between the left & right padding in inline codes ([0eb84e5](https://github.com/OXY2DEV/markview.nvim/commit/0eb84e5721dfd2ded1c598eba3ec018d5fd1cd9d))
* **renderer:** Fixed a bug causing the last line to have border placed on the wrong column ([e102b06](https://github.com/OXY2DEV/markview.nvim/commit/e102b060907173fcafaa8e5e4edde993452a9808))
* **renderer:** Fixed a bug leading to extmarks on the current line not being removed ([777c6aa](https://github.com/OXY2DEV/markview.nvim/commit/777c6aa50d623eed5a17fb39be60f23fbc7bd4bc))
* **renderer:** Fixed screen not updating in "no" mode ([60bc13b](https://github.com/OXY2DEV/markview.nvim/commit/60bc13b9492570d4d321391517eb9677918f540e)), closes [#70](https://github.com/OXY2DEV/markview.nvim/issues/70)
* **renderer:** Made headings use decorations around the text instead of replacing the main text ([41d57ab](https://github.com/OXY2DEV/markview.nvim/commit/41d57ab40603b702cd7b7b920c71f7b20ba202aa))