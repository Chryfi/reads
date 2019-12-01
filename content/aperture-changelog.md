# Change Log

Aperture's change log.

## Aperture 1.3.3

This small patch adds more path fixture intepolations, cut fixture feature and fixes few annoying bugs.

**Compatible** with McLib `1.0.3`. It doesn't mean that future versions of McLib would be incompatible, but older versions are most likely incompatible.

* Added a feature to "cut" fixtures (split a fixture at cursor in two)
* Added more interpolations to `path` fixture
* Added an option to disable auto saving of camera profiles upon exiting (auto save is enabled by default)
* Added a keybind to add a path point to currently selected path (suggested by Kanguste)
* Added a key modifier or something to allow in flight mode to also move vertically where character is looking (suggested by Kanguste)
* Added an interactive fixture creation tool to allow setup markers and then create multiple fixtures at once user finishes
* Added a feature to change/replace selected fixture fixture
* Added a key modifier (alt) to duplicate a keyframe in graph and dope sheet views
* Changed the default key bind to smooth camera to nothing, so people wouldn't freak out and end up deleting the mod, because it's "broken"
* Changed the flight speed to be even smaller value (suggested by Kanguste)
* Fixed modifiers not getting copied when "generate keyframe"
* Fixed flight mode by disallowing enabling it during playback
* Fixed performance of Show Path feature (reported by Joziah2)
* Fixed issue with clicking on text fields of value/tick it will make the buttons disappear
* Fixed block position gets reset in look modifier (reported by Chunk7)
* Fixed ~~FOV~~ roll with outside and flight modes (reported by Kanguste)
* Fixed and invert flight mode mouse wheel adjustment
* Fixed duplicating dialog to not allow using the same name
* Fixed flight mode or other interactive measures not modifying current fixture before first scrubbing

## Aperture 1.3.2

This small patch adds a couple of neat features and fixes few annoying bugs.

**Compatible** with McLib `1.0.3`. It doesn't mean that future versions of McLib would be incompatible, but older versions are most likely incompatible.

<?php echo youtube('pnXXgouveRk', $domain) ?> 

* Added `forward` option to `look` modifier which makes the camera face forward based on the direction of movement (suggested by terbin)
* Added dope sheet GUI for the keyframe fixture (i.e. the All keyframe fixture channel)
* Added an overlay camera option in camera editor (suggested by Lolik)
* Added fixture preview loop (suggested by Agirres)
* Added duration marker for playback scrub
* Changed flight mode to disable when player starts scrubbing (or switching between stuff)
* Changed camera options' height to be relative to the fixture editor area
* Changed interpolation list vertically responsive (suggested by Agirres)
* Changed internal representation of position from `float` to `double` (suggested by terbin for far away recording)
* Changed `drag` modifier to handle normalization of yaw
* Changed channel buttons (All, X, Y, Z, etc.) in the keyframe fixture editor
* Fixed duplicate camera profile not showing duplicate profile in the list
* Fixed overlays not rendering relative to playback scrub
* Fixed outside mode copying actual player location (reported by Braigar)
* Fixed edit position not working properly with modifiers

## Aperture 1.3.1

Unfortunately, before I released Aperture 1.3, I made a couple of bug fixes. I haven't test it properly and haven't let anyone test it either. However, Agirres spotted my stupidity, and aw shit, here we go again.

* Fixed double clicking not working due to another bug fix
* Fixed path fixture go void on first tick when velocity control is enabled
* Fixed velocity control issue where it lags toward the end (reported by Agirres)

## Aperture 1.3

This is a massive update which adds a lot of advanced camera features which would make new camera moves possible. Beside that, many bugs were fixed, and several features of camera editor were greatly enhanced!

**Compatible** with McLib `1.0.1`. It doesn't mean that future versions of McLib would be incompatible, but older versions are most likely incompatible.

<?php echo youtube('_vfZYtiRfRs', $domain) ?> 

* Added zooming and scrolling to time line bar
* Added rule of thirds camera option (suggested by Sanchan, Agirres and 5DF)
* Added letterbox camera option with configurable aspect ratio (suggested by SeanFilmProduction, Agirres, 5DF, Andruxioid and few others)
* Added `hermite` interpolation to keyframe fixture
* Added duplicate camera profile button in profile manager
* Added `[`, `]` and `'`, `\` keybinds to control FOV and camera roll in flight mode (respectively)
* Added search bar to profile manager (suggested by Agirres)
* Added `null` fixture which acts like a placeholder for next/previous fixture (suggested by Agirres)
* Added keyframe-able velocity control to path fixture (suggested by terbin)
* Changed duration dragging to react not immediately, but rather after mouse move (reported by Andruxioid)
* Changed buttons places in profile manager (suggested by Agirres)
* Changed the player's game mode to spectator mode when spectator is enabling and entering the camera editor
* Changed camera runner and camera editor to restore last roll
* Changed tick field in keyframe fixture integer only
* Changed position of per point duration checkbox
* Improved keyframe/graph view:
    * Added keybinds to vertically or horizontally move keyframes while holding Ctrl or Shift keys (suggested by GroupM and Agirres)
    * Added dropdown to pick interpolation in keyframe fixture editor (suggested by Agirres)
    * Added proper zooming and value marks into graph viewer in keyframe fixture editor
    * Added double clicking in graph view to create/remove keyframes
    * Changed rendering of keyframe points, graph and bezier control points
* Fixed translation interpolation and easing localization keys
* Fixed `bezier` interpolation to have proper mathematical implementation
* Fixed crash related to dragging keyframe tick/value when no keyframe selected
* Fixed crash related to shifting duration
* Fixed crash in camera runner (reported by STH)
* Fixed look modifier GUI elements (reported by Lycoon)
* Fixed issue with incorrect fixture placement when adding new
* Fixed `360˚`+ seizure-like yaw (reported by BenyangOVO, ycwei982, Lycoon and terbin)
* Fixed circular fixture not setting FOV and roll (reported by Agirres)
* Fixed little area which causes scrub rewind near the center of the playback scrub
* Removed `look` and `follow` fixtures (use modifiers counterparts)
* Removed lots of old camera editing sub-commands

## Aperture 1.2

This is a major update which features a new camera fixture called **keyframe fixture** and complete rewrite of GUI code (which allows Blockbuster to more control over integration).

<?php echo youtube('fT7QeCqKMyU', $domain) ?> 

* Added `mclib` library mod as a dependency
* Added keyframe camera fixture
* Added an ability to remove camera profiles
* Added **Generate keyframe** button in path fixture panel (suggested by GroupM)
* Added offset tick marker to playback scrub in camera editor (suggested by GroupM)
* Added a mechanic to resize durations between two fixtures without indvidually resizing them (suggested by GroupM)
* Changed where added fixture will be placed – if no fixture selected, a new fixture will be placed at the end of camera profile, otherwise, after currently selected fixture
* Full rewrite of camera editor GUI to support McLib GUI framework
* Full rewrite of Aperture's events

## Aperture 1.1.1

This is a minor update which fixes some stuff and adds some random stuff regarding the camera. The highlight of this update is the outside mode, which can be used to playback camera while also body acting (detaching yourself from the camera). In some situations it might be glitchy, causing a chunk freeze, but this can be easily fixed by changing render distance.

* Added version updater (added by ycwei982)
* Added outside mode to camera options (it allows to act while being in camera, but it can be glitchy sometimes)
* Added `drag` modifier
* Added reset of FOV back in camera editor (reported by KazerLight)
* Added mouse wheel scrolling in `path` fixture's points widget (suggested by Andruxioid)
* Added `/minecraft:tp` and `/tp` config options for the server camera playback (added by ycwei982)
* Added Russian localization (thanks to Andruxioid)
* Fixed server crash related to `CLIENT`
* Fixed issue with crash related to inability to create a client camera profile folder with illegal filename characters (thanks to ItsRitchieW)
* Fixed player's pitch not going over 90 when running a camera profile
* Fixed sync issues with cloning `follow` modifier and saving `shake` modifier toggle
* Fixed crosshair appearing in the camera editor

## Aperture 1.1

This update fixes a lot of issues and adds few features to camera editor, and introduces camera modifiers. Camera modifiers are special camera behavior modifiers which can be added to camera fixtures. They can process fixture's output in a lot of different ways like shaking camera, looking or following an entity (while still be in the path), apply math formulas and much more!

<?php echo youtube('dKmurdnlj1A', $domain) ?> 

* Added a camera option in camera editor to display camera properties (during camera playback or sync mode)
* Added a trackpad field to change current frame in the camera editor 
* Added `/aperture play` command (which can be used to force play a camera profile on the server side)
* Added camera modifiers
    * Shake modifier – can apply different kinds of shake to the camera
    * Math modifier – allows users to specify a math equation which will modify camera based on that equation
    * Look modifier – just like look fixture, but as modifier
    * Follow modifier – just like follow fixture, but as modifier
    * Translate modifier – translates the fixture by XYZ
    * Angle modifier – modify the angle
    * Orbit modifier – revolves around given entity, can also copy entity's rotation
* Added `default` camera profile to camera editor for easier setup
* Added rewind (going to `0` frame) when camera playback reaches the end
* Added renaming of camera profiles in profile manager
* Added `Ctrl + S` saving shortcut to camera editor
* Changed color of highlighted point to a darker shade
* Fixed CFM mirror camera orientation problem
* Fixed scrubbing event not getting sent when pressing points in path fixture
* Fixed server camera profiles not getting loaded into current camera editor camera profile
* Fixed the way camera playback was working (it was fundamentally wrong)
* Refactored camera fixture and modifier registration (modders can use an API to add their own fixtures or modifiers)
* Switched camera profile rendering to a config option

## Aperture 1.0.1

This is a small patch update that aims to improve capabilities of the camera editor by adding some new features and fixing some bugs.

<?php echo youtube('y7-WsAq6Vlg', $domain) ?> 

* Added shortcuts in the camera editor:
    * `D` – deselect current camera fixture
    * `S` – toggle sync option
    * `F` – toggle flight mode option
    * `Space` – play/pause
    * `C` – copy player's position
    * `M` – move duration to cursor
    * `Left Arrow` & `Right Arrow` – to move next or previous frame
    * `Left Arrow` & `Right Arrow` while holding Shift – to move to next or previous fixture
* Added indicators for sync and flight mode
* Added path fixture to set per point duration
* Allow to use `Enter` to create a new camera profile in profiles manager
* Allow to fly in camera editor (flight mode)
* Allow camera to surpass 90 degree limit (in camera runner)
* Convert camera networking code from JSON to ByteBuf
* Improved sync feature – doesn't teleport the user straight away, only after the user will scrub the timeline
* Return user back to his previous game mode
* Send `CameraEditorScrubbedEvent` only when scrub was actually (or it was indirect, like from the jump buttons) scrubbed by the user

## Aperture 1.0

First release of Aperture mod. This release has everything Blockbuster cameras had but more. It includes its own camera editor, and stuff that other camera mods has.

Its all features are frame based, meaning this camera mod would work perfectly with Minema mod and without it.

<?php echo youtube('F2LdjUH-4Qs', $domain) ?> 

#### General

General features which were included in the first release. Following features are included:

* Camera editor – a GUI that allows you to edit camera profiles easier using specially designed GUI
* Camera profile fixtures rendering
* Lots of config options
* Different camera fixtures
    * Idle fixture – static camera
    * Path fixture – animating camera using path points
    * Look fixture – stationary camera fixture which looks on an entity specified by entity selector
    * Follow fixture – stationary camera fixture which sticks to an entity specified by entity selector
    * Circular fixture – camera which makes a circle around given point
* Key bindings for positioning and rotating your player 
* Smooth camera (vanilla cinematic camera alternative which is Minema-friendly)

#### Commands

Includes lots of commands for managing camera profile, camera fixtures, configuring your player position, rotation, camera roll and FOV, and lots more!

* Commands for managing camera profile
    * `/camera new` – creates new camera profile
    * `/camera save` – saves camera profile
    * `/camera load` – loads camera profile
    * `/camera clear` – removes all fixtures from camera profile
    * `/camera list` – lists all camera profiles which are loaded
    * `/camera close` – removes camera profile from the list of currently loaded camera profiles
* Commands for managing camera fixtures within camera profile
    * `/camera add` – adds a camera fixture to camera profile
    * `/camera edit` – edits a camera fixture
    * `/camera remove` – removes a camera fixture
    * `/camera move` – moves a camera fixture to another index
    * `/camera goto` – set player's position and rotation based on camera fixture
* Commands for managing player's attributes related to camera
    * `/camera step` – sets player's position relatively or absolutely
    * `/camera rotate` – sets player's rotation relatively or absolutely
    * `/camera roll` – sets or informs current camera roll (camera tilting)
    * `/camera fov` – sets or informs current camera FOV
    * `/camera default` – resets camera roll and FOV to default values
* Commands for camera playback
    * `/camera start` – starts camera playback
    * `/camera stop` – stops camera playback
* Commands for managing path fixtures
    * `/camera path add` – add a path point
    * `/camera path edit` – edit a path point
    * `/camera path remove` – remove a path point
    * `/camera path move` – move a path point
    * `/camera path goto` – set player's position and rotation based on a point in a path fixture

These are only for legacy purposes. If you don't want to use these, totally cool, camera editor way convenient and time saving than using commands.