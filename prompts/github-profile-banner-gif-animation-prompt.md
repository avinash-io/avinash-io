# GitHub Profile Banner — Animated GIF Creation Prompt

## ROLE

Act as a professional image-processing and GIF optimization specialist.

Create a polished animated GIF from the user's supplied personal GitHub profile banner PNG.

The result must preserve the user's original banner artwork as faithfully as possible while adding only the requested animations.

The guiding principle is:

PRESERVE FIRST. ANIMATE SECOND.

This is an image-processing task, NOT a redesign or recreation task.

---

## INPUTS

The user will provide:

1. A source PNG containing their personal GitHub profile/banner artwork.
2. Optionally, a second reference image showing the desired colors/style for the animated equalizer.

Treat the supplied source PNG as the single source of truth for all static artwork.

If a reference image is supplied, use it ONLY to understand the desired appearance/colors of the newly generated animated equalizer.

Do NOT copy, recolor, redraw, or modify the user's existing static artwork based on the reference image.

---

# 1. STATIC ARTWORK PRESERVATION

Every animation frame MUST begin as an exact copy of the original source PNG.

Do NOT:

- redesign the banner
- regenerate the banner
- redraw the mascot
- redraw text
- change fonts
- change font weight
- change text positioning
- change the background
- change borders
- change icons
- change decorative elements
- change gradients
- change shadows
- change contrast
- globally brighten the image
- globally darken the image
- globally sharpen the image
- apply global color grading
- apply global saturation changes
- apply global hue changes
- apply global filters
- apply AI enhancement to the complete image

Only the explicitly designated animation regions may be modified.

If there is uncertainty about whether a pixel belongs to a static element:

LEAVE THE PIXEL UNCHANGED.

---

# 2. ANIMATION 1 — EQUALIZER / AUDIO VISUALIZER

Identify the existing equalizer/audio-visualizer area in the user's banner.

The equalizer should be animated smoothly so that its bars/dots move vertically as if responding to audio.

The animation should look natural rather than random.

Use:

- multiple independent bars
- different heights
- different animation phases
- smooth transitions
- sine-wave or similarly smooth motion
- subtle variation between neighboring bars
- a repeating seamless cycle

Do NOT animate the entire banner.

Do NOT move the equalizer horizontally.

Do NOT move surrounding artwork.

Do NOT modify labels, text, borders, or other graphics surrounding the equalizer.

---

# 3. EQUALIZER STYLE

If the original banner already contains an equalizer, remove ONLY the old equalizer pixels inside its exact animation region before drawing the new animated equalizer.

Do NOT erase surrounding artwork.

Clear the entire designated equalizer animation rectangle rather than trying to identify individual old equalizer pixels by color.

Restore the cleared area using the original surrounding/background appearance.

Then draw the new equalizer on top.

The new equalizer should retain the visual character of the original design:

- dot-matrix appearance
- small circular/square LED-like elements
- clean spacing
- terminal/tech aesthetic
- sharp rendering
- smooth animation

If a reference image is supplied, use its bright color treatment ONLY for the new equalizer.

A suitable color progression may include:

- blue
- cyan
- turquoise
- green
- light green
- pink
- magenta

Do not force these colors if they conflict with the supplied reference image.

The reference image is a STYLE/COLOR REFERENCE ONLY.

---

# 4. ANIMATION 2 — TERMINAL CURSOR

Identify the user's name/title text in the banner.

If the design contains a terminal-style cursor immediately after the user's name or another text element, animate that cursor.

The cursor should:

- blink naturally
- alternate between visible and invisible states
- remain in exactly the same position
- match the existing cursor's dimensions
- match the existing cursor's style
- not move
- not alter the text around it

If the banner does not contain a cursor, do not invent one unless the user explicitly requests it.

The user's actual name MUST be detected from the supplied image rather than hard-coded into this prompt.

---

# 5. FRAME CONSTRUCTION

For every frame:

1. Load the original source PNG.
2. Create a fresh exact copy.
3. Modify ONLY the equalizer animation region.
4. Modify ONLY the cursor region, if present.
5. Leave every other pixel untouched.
6. Add the frame to the GIF.

Never repeatedly modify a previously modified frame.

Never use the previous frame as the base for the next frame.

This prevents animation artifacts and accidental changes to static artwork.

---

# 6. EQUALIZER REGION ISOLATION

Before generating the GIF, accurately determine the bounding box of the equalizer.

The bounding box must contain:

- the existing equalizer
- the replacement equalizer

It must NOT contain:

- unrelated text
- labels
- borders
- dividers
- icons
- decorative graphics
- the user's name
- the mascot
- other static artwork

If necessary, inspect the source image at pixel level before processing.

Do not guess the bounding box when it can be determined from the image.

---

# 7. CURSOR REGION ISOLATION

Determine the smallest practical bounding box containing the cursor.

The cursor region must NOT include surrounding text.

Do not redraw the user's name.

Do not modify anti-aliased text pixels.

Only replace the cursor itself.

---

# 8. ANIMATION TIMING

Preferred configuration:

- 40–48 frames
- ideally 48 frames
- approximately 90 ms per frame
- approximately 4.3 seconds total animation
- infinite loop

Use a seamless repeating animation.

The final frame should transition naturally back into the first frame.

If file-size constraints require fewer frames, reduce the frame count while maintaining smooth motion.

---

# 9. GIF QUALITY

The final output MUST be a real animated GIF.

It must NOT be:

- a PNG renamed to `.gif`
- a single-frame GIF
- a static image embedded inside a GIF container

Verify that:

- the file format is GIF
- frame count > 1
- animation timing exists
- loop is infinite
- dimensions match the source PNG

---

# 10. GITHUB COMPATIBILITY

The GIF is intended for use in a GitHub profile README.

Prioritize:

- reasonable file size
- sharp text
- readable static artwork
- smooth animation
- good color reproduction
- fast loading

Target:

UNDER 10 MB.

Prefer approximately 5–8 MB when possible.

If the first GIF exceeds the target:

1. Optimize the palette.
2. Optimize frame storage.
3. Reduce unnecessary colors.
4. Reduce frame count if necessary.
5. Optimize GIF encoding.
6. Re-audit the result.

Do NOT sacrifice the static artwork merely to reduce file size.

---

# 11. IMPORTANT GIF PALETTE RULE

GIF uses a limited color palette.

Do NOT blindly apply aggressive global quantization that visibly damages the user's static artwork.

Use the best available palette strategy to preserve the source artwork.

If exact pixel preservation is technically impossible because of GIF palette limitations, prioritize:

1. Static artwork fidelity.
2. Text readability.
3. No unintended recoloring.
4. Animation quality.
5. File size.

Clearly report any unavoidable GIF palette limitation during the final audit.

---

# 12. ABSOLUTELY FORBIDDEN

Never perform any of the following:

- Global recoloring
- Global brightness adjustment
- Global contrast adjustment
- Global sharpening
- Global hue shifting
- Global saturation adjustment
- AI restyling
- Redrawing the complete banner
- Recreating text
- Recreating the mascot
- Changing the user's name
- Changing fonts
- Moving static elements
- Changing background colors
- Changing borders
- Changing decorative elements
- Applying the reference image's colors to static artwork
- Painting over text
- Painting over anti-aliased text
- Painting over icons
- Painting outside the animation masks

The supplied banner must remain visually identical everywhere except the explicitly animated regions.

---

# 13. MANDATORY QUALITY AUDIT

After creating the GIF, perform an automated audit.

Check all of the following.

## A. File validation

Verify:

- File is actually GIF.
- Frame count > 1.
- Dimensions equal the source PNG.
- Animation duration is correct.
- Loop is infinite.
- File size is reported in MB.

## B. Static-region audit

Create a mask containing ONLY:

- equalizer region
- cursor region

Compare every GIF frame against the original source PNG outside this mask.

The intended result is:

Static-region changed pixels = 0

If this cannot be achieved because of GIF palette limitations, identify and report the limitation rather than claiming perfect preservation.

## C. Equalizer audit

Verify:

- old equalizer is removed
- no ghost pixels remain
- no old equalizer colors remain outside the intended region
- new equalizer remains inside its bounding box
- animation changes between frames
- equalizer does not overwrite unrelated artwork

## D. Cursor audit

Verify:

- cursor stays in the correct location
- cursor does not move
- cursor alternates visibility
- surrounding text remains unchanged

## E. Visual audit

Inspect representative frames:

- first frame
- middle frame
- final frame

Check for:

- ghosting
- flickering
- color bleeding
- text damage
- background patches
- accidental recoloring
- animation artifacts
- broken transparency
- palette artifacts
- harsh transitions

---

# 14. FAILURE CONDITION

Do NOT deliver the GIF as final if:

- it is not actually animated
- it exceeds the GitHub target unnecessarily
- static artwork has been globally recolored
- text has been damaged
- the mascot has changed
- the background has changed
- the equalizer has ghost pixels
- the cursor is misplaced
- unrelated areas are animated
- the animation is visibly broken

Fix the problem and audit again.

---

# 15. OUTPUT

Use this filename:

github-profile-banner.gif

Do not use filenames tied to a specific person's name.

The output should be ready to place inside a GitHub profile README.

Example Markdown usage:

![GitHub Profile Banner](./github-profile-banner.gif)

---

# 16. FINAL REPORT

After successful creation, report:

- Filename
- File size
- Dimensions
- Frame count
- Frame duration
- Total animation duration
- Loop setting
- Static-region audit result
- Equalizer audit result
- Cursor audit result
- Whether the GIF meets the GitHub target size

Example:

Filename: github-profile-banner.gif
Format: GIF
Dimensions: 2048 × 682
Frames: 48
Frame duration: 90 ms
Total duration: ~4.32 seconds
Loop: Infinite
Static-region audit: PASS
Equalizer audit: PASS
Cursor audit: PASS
File size: 6.8 MB
GitHub target: PASS

---

# 17. PRIVACY / DATA HANDLING

Use only the images and information supplied by the user for this task.

Do not:

- extract unrelated personal information
- store personal information unnecessarily
- upload the user's banner to external services
- transmit the user's image to third parties
- embed hidden metadata containing personal information
- add identifying information that was not present in the source image

The processing should be performed locally whenever possible.

---

# CORE PRINCIPLE

PRESERVE FIRST.
ANIMATE SECOND.

The user's original banner is the source of truth.

Only the explicitly requested animation regions may change.

Everything else must remain untouched.
