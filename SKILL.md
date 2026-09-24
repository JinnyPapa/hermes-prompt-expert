# Prompt Expert

Takes simple, brief ideas and expands them into detailed, optimized prompts for image/video generation models.

## When to use
- User gives a simple image/video idea and wants the best result
- User explicitly asks for prompt optimization or expansion
- Before calling generation tools when the user's input is too brief

## Process

### Step 1: Clarify (if needed)
- What's the core subject?
- Any style references or mood?
- Aspect ratio / use case?
- If user gives all this, skip straight to Step 2.

### Step 2: Analyze & Expand
For a simple input like "cat on a rooftop", expand into:

**Image prompt structure:**
```
[Subject with specific details], [action/pose], [environment/background], 
[lighting conditions], [atmosphere/mood], [camera angle/lens], 
[style/medium], [quality tags]
```

**Video prompt structure:**
```
[Subject], [specific motion/action with timing], [camera movement], 
[environment], [lighting], [atmosphere], [audio if applicable], [style]
```

### Step 3: Model-Specific Optimization
- **FLUX 3 (video)**: Emphasize motion, camera work, subject consistency. Use prose, not tags.
- **Stable Diffusion / SDXL**: Use tag-based format, include quality tags (masterpiece, best quality)
- **Midjourney**: Natural language, include --ar, --style, --v parameters
- **DALL-E**: Detailed natural language descriptions work best

### Step 4: Present
- Show the expanded prompt
- Briefly explain key additions (why this lighting, why this camera angle)
- Ask if user wants adjustments before generating

## Example

**User input:** "futuristic city at night"

**Expanded (SDXL):**
```
detailed futuristic cyberpunk cityscape at night, neon lights reflecting on wet streets, 
tall holographic billboards, flying vehicles, dense skyscrapers with glowing windows, 
rain-soaked atmosphere, cinematic lighting, volumetric fog, low angle shot, 
wide-angle lens, highly detailed, 8k resolution, concept art style
```

**Expanded (FLUX 3 video):**
```
A sweeping camera movement through a dense futuristic city at night. 
Neon signs flicker above rain-slicked streets as holographic advertisements 
float between towering skyscrapers. Flying vehicles zip overhead leaving light 
trails. The camera slowly rises, revealing the vast sprawling metropolis 
beneath. Cinematic lighting with volumetric fog, deep blues and purples 
contrasted with neon pinks and greens. Ambient city sounds, distant traffic, 
low-frequency hum.
```

## Notes
- Ask user which model they're targeting if unclear
- For the user's setup: FLUX 3 for video, RTX 3090 for image generation
- User prefers Korean communication
- Always offer the expanded prompt before generating so user can approve