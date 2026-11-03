<div align="center">

# T9 Code

**A phone-first fork of [T3 Code](https://github.com/pingdotgg/t3code).**

Dictate to your agents instead of typing, annotate their answers, listen to replies with text-to-speech and steer a session from a game controller. The Mac app follows upstream's nightly builds.

**[Download for Mac](https://github.com/jonpage0/t3code-releases/releases)**&emsp;[See what's different](#at-a-glance)

<img src=".github/readme/phone-swipe-send.png" width="240" alt="A thread washed green from the right edge, with a green send-arrow disc under the Git button: letting go of this swipe sends the reply">&nbsp;&nbsp;<img src=".github/readme/phone-note-inline.png" width="240" alt="A note being written on the word 'sum' in an assistant reply, with Remove and Save, and a pill counting one pending note above the composer">

<sub>Pull far enough and the cue turns green to send. A note pinned to one word of an answer.</sub>

</div>

## At a glance

Everything upstream T3 Code does, plus:

| Feature                                       | What it does                                          | Where       |
| --------------------------------------------- | ----------------------------------------------------- | ----------- |
| [Swipe to dictate](#swipe-to-dictate)         | Swipe left to dictate, pull until it's green to send  | iPhone      |
| [Enhanced annotations](#enhanced-annotations) | Pin comments to passages and send them with a reply   | Everywhere  |
| [TTS responses](#tts-responses)               | Hear any finished reply in one of five voices         | Everywhere  |
| [Game controller](#game-controller)           | Run sessions from a gamepad, dictation included       | iPhone      |
| [Model controls](#model-controls)             | Favorites-first picker, one-glyph badges, cycle keys  | iPhone, Mac |
| [Finding threads](#finding-threads)           | Group by status or project, open details from a title | iPhone      |
| [Provider fixes](#server-and-providers)       | Codex tiers with managed sign-in, Opus at Extra High  | Server      |
| [Nightly Mac builds](#how-builds-are-made)    | Signed, notarized, rebuilt on upstream nightlies      | Mac         |

## On iPhone

Run a session with the keyboard down: dictate, annotate, listen, or pick up a controller.

### Swipe to dictate

Swipe left across a thread to start dictating into the draft, and swipe again to stop. A disc under the Git button shows what letting go will do: blue starts dictation, red stops one that's recording, and green sends. Pull until it turns green, marked by a firm tap, and letting go sends the message as soon as the transcript is ready. Ease back and it only dictates.

<p align="center">
  <img src=".github/readme/phone-swipe-dictate-light.png" width="240" alt="A thread in light mode washed blue from the right edge, with a blue microphone disc under the Git button: a short swipe left starts dictation">&nbsp;&nbsp;<img src=".github/readme/phone-microphone-settings.png" width="240" alt="Microphone settings: Apple or Parakeet on device, Swipe left to dictate switched on, Pull to send set to Medium, and Hide microphone button">
</p>

- Turn it on in **Settings → Microphone**; it's off by default. Once you're used to it, you can hide the microphone button.
- **Pull to send** sets how far that is: Short, Medium (the default), Long, or Off for a swipe that only dictates.
- While you're writing a note, the swipe dictates into the note. The message box shows its recording bar, labelled **Dictating into note**, and the cursor waits after the new text.
- Choose Apple dictation or **Parakeet on device**. Parakeet is a one-time download of about 632 MB, and audio never leaves the phone.
- Code blocks and tables that can still scroll keep scrolling, so a swipe across them doesn't start dictation.

### Enhanced annotations

Select a passage in a reply and choose **Annotate**. Your comment is pinned to that passage, and your notes go out with the next message, quotes included.

<p align="center">
  <img src=".github/readme/phone-annotate-menu-light.png" width="240" alt="The iOS selection menu over a reply, offering Annotate, Copy and Copy as Markdown">&nbsp;&nbsp;<img src=".github/readme/phone-notes-review.png" width="240" alt="The Pending notes sheet showing a quoted passage with its comment and Show passage, Edit and Remove actions">
</p>

- Tap a highlighted passage to reopen its note.
- A notes pill in the floating row above the composer, beside the working status, opens a sheet where you can edit or remove each note, or jump back to its passage.
- Notes can go out on their own, without a message. The reply itself is never changed.

### TTS responses

Every finished reply has Play and Stop at the end of its action row. The text goes straight to xAI speech, with no rewrite and no extra agent turn, and starts playing while it's still being generated.

<p align="center">
  <img src=".github/readme/phone-speech-controls.png" width="240" alt="A finished reply with Play and Stop at the right end of its action row">&nbsp;&nbsp;<img src=".github/readme/phone-speech-voices.png" width="240" alt="The Speech voice sheet listing Eve, Ara, Leo, Rex and Sal, each with a short description">
</p>

- Five voices (Eve, Ara, Leo, Rex and Sal) and speeds from 0.7× to 1.5×, saved per server.
- Needs an xAI API key on the server. Add it in **Settings → Threads** on the phone or **Settings → General** on the Mac, or export `XAI_API_KEY`. The key never leaves the server.
- The same controls appear on Mac and web, where <kbd>Cmd</kbd>+<kbd>Option</kbd>+<kbd>P</kbd> pauses and resumes and adding <kbd>Shift</kbd> stops.
- Playback runs in the foreground, one reply at a time.

### Game controller

Pair a gamepad and the phone becomes a remote for your agents. The shoulder buttons switch sessions, the D-pad moves focus and Options sends. Hold the right trigger to dictate into the composer, a note or an answer to an agent's question; letting go transcribes but never sends.

<p align="center">
  <img src=".github/readme/phone-controller-landscape.png" width="560" alt="The landscape controller workspace with the session sidebar, compact header and tools rail">
</p>

<p align="center">
  <img src=".github/readme/phone-controller-settings.png" width="240" alt="Game controller settings with the Generic gamepad preset and its button mappings">
</p>

- Presets for the ohsnap! MCON and generic gamepads. Remap any button, or add shoulder chords, in **Settings → Game controller**.
- Rotate the phone for a landscape workspace with a session sidebar and a Terminal, Files and Git rail. Or lock the phone to portrait.
- Approval and question cards work from the controller. Send and Stop need a fresh press and never repeat.
- **Test inputs** shows what each button does without sending, approving or running anything.

### Model controls

The model sheet opens on your favorites, with provider, effort and speed controls pinned beneath the list; the yellow star shows everything else. In the composer, the model is a single badge: a sun for Sol, a moon for Luna, a music note for Opus, a closed book for Fable.

<p align="center">
  <img src=".github/readme/phone-model-picker.png" width="240" alt="The model sheet listing Codex and Claude models, with filter, permissions, effort, speed and favorites controls pinned beneath the list">
</p>

- Effort reads as four rising bars, then one flame for Max and two for Ultra. A bolt appears only for Fast or Ultrafast.
- A thin ring around the send button shows how full the context window is.

### Finding threads

Group the thread list by status or by project. Fold the projects you're not working in and drag the rest into your own order.

<p align="center">
  <img src=".github/readme/phone-thread-list.png" width="240" alt="The thread list grouped by project, with one project folded and two expanded to show their threads">&nbsp;&nbsp;<img src=".github/readme/phone-thread-details.png" width="240" alt="The compact thread details panel opened from the title: project, environment, workspace and branch as label-and-value rows, then shortcuts to files, terminal, Git, agents and thread settings">
</p>

- The environment, project and grouping filters stay hidden until you pull down past the top.
- Tap a thread's title for a compact panel with its project, environment, workspace and branch, and shortcuts to files, terminal, Git, agents and settings.
- On a hardware keyboard, <kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>[</kbd> and <kbd>]</kbd> switch sessions, and <kbd>Ctrl</kbd>+<kbd>Tab</kbd> returns to the last one.

## On Mac and the web

Faster ways to answer an agent from the keyboard.

### Enhanced annotations

Select text in a reply and press <kbd>R</kbd> to annotate it, or choose **Agree** or **Disagree** to add the quote with that comment already written. Nothing is sent until you send it.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset=".github/readme/desktop-annotate-toolbar-dark.png">
  <img src=".github/readme/desktop-annotate-toolbar-light.png" width="820" alt="A reply with a bright yellow draft quote, a lighter sent quote, and the selection toolbar offering Annotate, Agree and Disagree">
</picture>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/readme/desktop-annotation-dark.png">
    <img src=".github/readme/desktop-annotation-light.png" width="320" alt="A popover listing two sent annotations, each with its comment above the quoted passage">
  </picture>
</p>

- <kbd>Enter</kbd> saves a note; <kbd>Cmd</kbd>/<kbd>Ctrl</kbd>+<kbd>Enter</kbd> saves it and sends the message. Drag the editor by its grab bar to move it out of the way.
- Quotes stay highlighted: bright yellow in your draft, lighter once sent. Click one to read what you wrote.
- The thread details card lists your current drafts and, folded beneath them, everything already sent.
- Rebind Annotate, Agree and Disagree in **Settings → Keybindings**.

### Keyboard

| Keys                                                           | Does                   |
| -------------------------------------------------------------- | ---------------------- |
| <kbd>Hyper</kbd>+<kbd>,</kbd>                                  | Next favorite model    |
| <kbd>Hyper</kbd>+<kbd>/</kbd>                                  | Next speed tier        |
| <kbd>Cmd</kbd>+<kbd>Option</kbd>+<kbd>E</kbd>                  | Raise reasoning effort |
| <kbd>Cmd</kbd>+<kbd>Option</kbd>+<kbd>P</kbd>                  | Pause or resume speech |
| <kbd>Cmd</kbd>+<kbd>Option</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> | Stop speech            |
| <kbd>R</kbd> with text selected                                | Annotate the selection |

<kbd>Hyper</kbd> is <kbd>Cmd</kbd>+<kbd>Ctrl</kbd>+<kbd>Option</kbd>+<kbd>Shift</kbd>. Off the Mac, read <kbd>Cmd</kbd> as <kbd>Ctrl</kbd>. Holding a combination doesn't repeat it. Change any of these in **Settings → Keybindings**.

## Server and providers

Changes on the server, so every client gets them.

- **Codex speed tiers with T3-managed ChatGPT sign-in.** The picker shows the tiers your account offers, such as Fast, and uses the chosen one for turns and text generation.
- **Opus 5.5 starts at Extra High effort** unless you choose another level.
- **Accurate Claude update checks.** Native Claude installs are compared with Claude's own release feed, so a current install no longer says it needs an update.
- **Quotes survive a provider switch.** Quoted passages and their comments carry over in full when a thread changes provider.
- **Remote servers stay on upstream.** The fork publishes no server builds, so remote and SSH servers update to the upstream nightly your Mac build is based on, and count as current there.

## Install and update

### Mac

1. Download the newest **arm64 `.dmg`** from [Releases](https://github.com/jonpage0/t3code-releases/releases). Builds are for Apple Silicon, signed and notarized.
2. Drag the app to Applications. It installs as **T3 Code (Nightly)**.
3. Connect your providers as you would in T3 Code. Later builds arrive through the app's own update control, from the fork's release feed instead of official T3 releases. Its popover lists each release's fixes, not just its highlights.

A fork version is the upstream build number × 1000 + n, so `0.1.7-nightly.20261102.4080002` is the second fork build on upstream nightly 4080. Native passkeys are off in these builds; browser sign-in works.

### iPhone

The iPhone app is in a small, invited TestFlight beta and updates over the air between builds. There is no public iPhone download or App Store release yet.

- **Settings → About → Version** shows which update is running.
- Pair it with the server in the Mac app above. Upstream servers also work, but without server-side fork features such as TTS responses.

## How builds are made

Releases are cut by hand when upstream publishes a new nightly. The nightly is merged into the fork, the fork's checks and its own tests run against it, and the Mac app is then built, signed, notarized and published here. A failed check stops the release before anything is published.

- Release notes keep upstream's highlights and fixes, and link back to this page.
- This repository holds only Mac installers, update metadata and checksums. The fork's source and the iPhone builds are maintained privately.

## Credit and license

T9 Code is built on [T3 Code](https://github.com/pingdotgg/t3code) by T3 Tools Inc., and nearly all of it is their work. This is an unofficial personal fork, not affiliated with or supported by T3 Tools. For upstream's install guide and documentation, see the [T3 Code repository](https://github.com/pingdotgg/t3code).

T3 Code is MIT-licensed. Its license is in [LICENSE](LICENSE), and the app includes its license and dependency notices.
