# Dark-Transparent-Tablet-Dashboard
Hey everyone — I honestly didn’t expect the post I shared to blow up like it did. I really appreciate all the interest and kind words!
As promised, here are the full details of the setup. To keep things consistent with how I presented it in the original Reddit post, we’ll break everything down in the same order, section by section.

![Banner](https://github.com/user-attachments/assets/5e1d01fd-7f0a-4f58-aa21-35d93eb4252c)

Below is a list of everything you’ll need to install from HACS to get a 100% match of the layout I shared:

**Cards**
- [Button Card](https://github.com/custom-cards/button-card)
- [Expander Card](https://github.com/Alia5/lovelace-expander-card)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [My-slilder-v2](https://github.com/AnthonMS/my-cards/blob/main/docs/cards/slider-v2.md)

**Graphs**
- [Mini Graph Card](https://github.com/kalkih/mini-graph-card)
- [Waterfall History Card](https://github.com/sxdjt/horizontal-waterfall-history-card)

**Layouts / templating:**
- [Auto Entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Card-Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Config Template Card](https://github.com/iantrich/config-template-card)
- [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
- [Local Conditional Card](https://github.com/PiotrMachowski/Home-Assistant-Lovelace-Local-Conditional-card) 
- [Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row)
- [Stack in Card](https://github.com/custom-cards/stack-in-card)
- [Vertical Stack in Card](https://github.com/ofekashery/vertical-stack-in-card)

**Theme**
- [Material You Theme](https://github.com/Nerwyn/material-you-theme)

**ETC**
- [Alarmo](https://github.com/nielsfaber/alarmo)
- [Calendar Card Pro](https://github.com/alexpfau/calendar-card-pro)
- [Mini Media Player](https://github.com/kalkih/mini-media-player)
- [WebRTC Camera](https://github.com/AlexxIT/WebRTC)

_Before we dive into the template, **here are the temperature ranges** I’ve set up across the dashboard graphs to maintain a consistent visual style throughout._

Below 16°C – 🟪 Very Cool
Light purple tones indicate chilly conditions, likely too cold for comfort without heating.

16°C to 17.9°C – 🟦 Cool
Light blue shades suggest it's a bit cool, possibly refreshing or just under comfortable indoors.

18°C to 21.9°C – 🟩 Comfortable
Soft green tones reflect an ideal room temperature—pleasant and mild.

22°C to 23.9°C – 🟨 Warm
Light amber tones imply a warm space, likely still comfortable but edging towards toasty.

24°C to 26.9°C – 🟥 Hot
Pinkish-red tones indicate the area is getting hot and might benefit from cooling.

27°C and above – 🔥 Very Hot
Deep red tones show it's very warm—likely uncomfortable, especially in enclosed areas like a garage.



**Alright—without further ado, let’s jump into the first section below.**


# 🖼️ First Image – Homepage Overview
![1-landscape](https://github.com/user-attachments/assets/90fb9e53-678e-4937-9b0d-f3279a05c96d)

This is the homepage, designed to surface the most essential information at a glance. Discclaimer: in order for this area to work, you need a Grid (layout card) to work, and add this [config](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Grid%20Template%20Config.txt) under Subview toggle.

**🔹 1st Row**

[**First column:**](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/First%20Image%20-%201st%20Row%20-%20First%20Column.txt)
- Clock & date
- Weather forecast with a custom [weather-icon](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Weather%20Condition%20Icon.txt)
- Room occupancy toggles (used to trigger climate automation)

[**Second Column:**](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/First%20Image%20-%201st%20Row%20-%20Second%20Column.txt)
- Tab 1: Indoor/outdoor temperature with climate control
- Tab 2: Sprinkler control

[**Third Column:**](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/First%20Image%20-%201st%20Row%20-%20Third%20Column.txt)
- Media card with speaker count

[**Fourth Column:**  ](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/First%20Image%20-%201st%20Row%20-%20Fourth%20Column.txt)
- Calendar showing schedules for me, my wife, and special events
- Alarm indicator and notification count, which links to the notification panel (weather, alarm, etc), see below for reference
![image](https://github.com/user-attachments/assets/2683fada-c8e4-4e64-8b1e-b8a7b53130ff)

**🔹 2nd Row**
[Room cards](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/First%20Image%20-%202nd%20Row%20-%20Room%20Card.txt) showing:
- Temperature and humidity
- Light toggle
- Count of open doors/windows (when applicable)

**🔹 3rd Row**

[Camera location header](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/First%20Image%20-%203rd%20Row%20-%20Camera%20Card%20Header.txt) and [camera cards](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/First%20Image%20-%203rd%20Row%20-%20Camera%20Card.txt)
- A set of four main security camera feeds for quick monitoring.
(Note: I had issues with swipe-card, so for now only four cameras are displayed.)

# 🖼️ Second Image – Room View
![2-landscape](https://github.com/user-attachments/assets/2adddeb8-c6c5-4db1-8f8b-ef7fb176b0c8)

This image shows a detailed room view, which I've divided into three main sections from left to right:

[**Left Section – Lighting Controls**](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Second%20Image%20-%20Left%20Section%20%E2%80%93%20Lighting%20Buttons.txt)

Swipe left or right to adjust the brightness of each light.
At the bottom, there’s a [collapsible card](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Second%20Image%20-%20Left%20Section%20%E2%80%93%20Collapsible%20Card.txt) that neatly hides lights we rarely interact with—helping keep the interface clean and uncluttered.

[**Middle Section – Climate Info**](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Second%20Image%20-%20Middle%20Section%20-%20Climate%20Info.txt)

Temperature - Uses a waterfall card with color-coded hex values to reflect thresholds that previously mentioned
Humidity - Only two color states — green (normal) and red (too high)

**Right Section – Aesthetic Filler**

Purely for visual balance Changes appearance based on time of day: day/night mode. This one is rendered through ChatGPT Plus with this prompt below:

_"Create a 3d isometric image from the photo attached. Make it look as close as possible. Refer for the second image (you can use mine) for your reference in generating the inmage"_


# 🖼️ Third Image – Notification & Weather Panel
![3-landscape](https://github.com/user-attachments/assets/e585a89c-6db6-4451-8e16-2526d033c45d)

This panel serves as a quick overview for notifications, weather info, and some dynamic visual elements.

**Left Section – [Active Timers](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Third%20Image%20-%20Left%20Section%20%E2%80%93%20Timer%20Examples.txt) & [Mushroom Chips Cards](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Third%20Image%20-%20Left%20Section%20%E2%80%93%20Chip%20Card%20Examples.txt)**

Contains hidden chips for various statuses such as:
- Recycle day
- Dryer / washing machine
- And more, depending on conditions

Below that is a [active light](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Third%20Image%20-%20Left%20Section%20%E2%80%93%20Active%20Lights.txt) status list, displaying which lights are currently on.

**Middle Section – Weather Info**

Shows current weather [status](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Third%20Image%20-%20Middle%20Section%20%E2%80%93%20Weather%20Status.txt), [forecast](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Third%20Image%20-%20Middle%20Section%20%E2%80%93%20Weather%20Forecast.txt), and active [warnings](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Third%20Image%20-%20Middle%20Section%20%E2%80%93%20Weather%20Warning.txt) (if any — none at the moment). Please note: the information shown here is highly dependent on your local sensors and weather integrations, so your results may vary depending on what you have set up.

**Right Section – Windy.com iFrame**

[Embedded Windy.com map](https://github.com/reylinux/Dark-Transparent-Tablet-Dashboard/blob/main/Third%20Image%20-%20Right%20Section%20%E2%80%93Windy.com%20iFrame.txt), which offers rich weather visualizations. You can toggle between different map layers (wind, rain, temperature, etc.) for a more detailed view. You'll need to get the URL from the Windy embed [here](https://embed.windy.com/config/map) and grab the URL within the quotes from the src section and put it in the iframe card.

# 🖼️ Fourth Image – Full Camera View
![6-landscape](https://github.com/user-attachments/assets/cb1452fb-2f45-47bf-95e1-447fbc79a6a2)

This page is dedicated to all security camera feeds for centralized monitoring.
I’m using a mix of Reolink CX410, CX810, and E1 Pro models.
Below each camera feed, I’ve added light switches for the corresponding or nearby area—allowing for quick and convenient control directly from the camera view.

# 🖼️ Fifth Image – Philips Hue Scene Controller
![4-landscape](https://github.com/user-attachments/assets/dfe8fedb-6f74-4941-bcde-f08978707a62)

This page contains a set of scenes I personally enjoy, designed specifically for the Living Area Hue lights (10+ lights total).

Scenes are triggered via automations and scripts, and only apply to the designated Hue lights.
- Once a scene is activated, an “Off” button appears.
- This button returns lights to their default automation behavior:
- Lights in occupied areas return to normal based on sensor detection.
- Unoccupied lights turn off gracefully, with a 2-second delay per light and a 3-second transition to maintain smooth visual flow.

# 🖼️ Sixth Image – Alarmo System
![5-landscape](https://github.com/user-attachments/assets/b351132e-7d7f-4e2d-b5e0-631ad8f17db6)

Last but not least, this is the dedicated page for Alarmo—my home alarm system integration. You can set this up very easily by adding Alarmo card through the UI.

Recently set this up and it's been surprisingly fun to test.
When triggered, it:
- Turns all living area lights red
- Plays an alarm siren sound through 8x Google Nest Minis in sync

Extra credits:
- [Custom weather buttons, Light Slider Cards](https://www.youtube.com/@My_Smart_Home)
- [Windy iFrame](https://www.reddit.com/r/homeassistant/comments/1l4hnx7/weather_dashboard_v100/)

# Sponsor ❤️
[<img width="170" height="37" alt="Buy me a coffee" src="https://github.com/user-attachments/assets/2bc7c798-1015-4293-b674-6680d8413a9c" />](https://buymeacoffee.com/reynaldisuu)

