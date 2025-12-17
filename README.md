# Visual Oddball (iOS)

This Xcode project contains a **native SwiftUI** port of your “Visual Oddball” target-detection style task (originally provided in HTML/JavaScript).

## What’s implemented

- Start screen with **trial count** and **target probability (%)**
- Start screen **Speed** slider (left = faster, right = slower)
- Start screen option for **Blocks** (repeat the trial set across multiple blocks)
- Option to **keep target colour constant across blocks** or **re-randomize each block**
- Optional **fixation cross (+)** during blank intervals
- Countdown (3…2…1…Go!)
- Timed trial loop with **jittered ISI**, stimulus duration, and post-stim delay (matching your JS constants)
- Response collection (native version uses **tap anywhere**; easy to extend to hardware keyboard)
- Break screen between blocks (“End of Block” → tap to continue)
- End screen summary:
  - Hits / Misses / False Alarms / Correct Rejections
  - Accuracy, \(d'\), \(c\), Mean RT (correct)
  - RT histogram
  - CSV export via iOS file share/export

Main entry view: `TargetDetectionTaskView` (shown after a 5-second splash screen).

## Files to look at

- `Visual Oddball/Visual Oddball/TargetDetectionTaskView.swift` (SwiftUI screens)
- `Visual Oddball/Visual Oddball/TargetDetectionViewModel.swift` (timing + state machine)
- `Visual Oddball/Visual Oddball/TargetDetectionStats.swift` (SDT + CSV)


