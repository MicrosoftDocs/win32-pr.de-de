---
title: Fülleffekt
description: Verwenden Sie den Blend-Effekt, um zwei Bilder zu kombinieren. Dieser Effekt verfügt über 26 Mischungsmodi.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- Blend-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853043123c6eea9a87656a7450b1295236ed5d6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478196"
---
# <a name="blend-effect"></a>Fülleffekt

Verwenden Sie den Blend-Effekt, um zwei Bilder zu kombinieren. Dieser Effekt verfügt über 26 Mischungsmodi.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Blend.

-   [Beispiele für das Mischen](#blending-examples)
-   [Effekteigenschaften](#effect-properties)
-   [Blend-Modi](#blend-modes)
-   [HSL-Farbraumkonvertierungen](#hsl-color-space-conversions)
    -   [Konvertieren von RGB in HSL](#converting-from-rgb-to-hsl)
    -   [Konvertieren von HSL in RGB](#converting-from-hsl-to-rgb)
-   [Ausgabebitmap](#output-bitmap)
-   [Beispielcode](#sample-code)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="blending-examples"></a>Beispiele für das Mischen

Hier sehen Sie ein Beispielbild für jeden Blendmodus des Blend-Effekts. Eine vollständige Liste der Mischungsmodi und der entsprechenden Moduseigenschaften finden Sie im nächsten Abschnitt.

![Screenshot des Effektbeispiels aller verfügbaren Mischungsmodi.](images/blend-modes.png)

Im Folgenden finden Sie ein weiteres Beispiel für die Verwendung des Ausschlussmodus.



| Vor Abbildung 1                                                             |
|----------------------------------------------------------------------------|
| ![das erste Quellbild vor dem Effekt.](images/default-before.jpg)    |
| Vor Abbildung 2                                                             |
| ![das zweite Bild vor dem Effekt.](images/4-arthimetic-composite2.jpg) |
| Danach                                                                      |
| ![das Bild nach der Transformation.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekteigenschaften



| Anzeigename und Indexenumeration                 | BESCHREIBUNG                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> D2D1 \_ BLEND \_ PROP \_ MODE<br/> | Der für den Effekt verwendete Blendmodus. Weitere Informationen finden Sie unter [Blend-Modi.](#blend-modes) Der Typ ist D2D1 \_ BLEND \_ MODE.<br/> Der Standardwert ist D2D1 \_ BLEND \_ MODE \_ MULTIPLY.<br/> |



 

## <a name="blend-modes"></a>Füllmethoden

Die folgende Tabelle zeigt alle Mischungsmodi dieses Effekts. Die Hilfsfunktionen, die zum Berechnen der Ausgabe des Effekts erforderlich sind, befinden sich im nächsten Abschnitt.

Farbe: O <sub>PRGB</sub>  =  *f*(F <sub>RGB</sub>, B <sub>RGB</sub>) \* F <sub>A</sub> \* B <sub>A</sub> + F <sub>RGB</sub> \* F <sub>A</sub> \* (1 - B <sub>A</sub>) + B <sub>RGB</sub> \* B <sub>A</sub> \* (1 - F <sub>A</sub>)

Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub>

Hierbei gilt:

-   O<sub>PRGB</sub> ist die vormultiplikierte Ausgabefarbe.
-   O<sub>A</sub> ist Ausgabe-Alpha
-   B<sub>RGB</sub> ist die nicht vormultiplikierte Zielfarbe.
-   B<sub>A</sub> ist Ziel alpha
-   F<sub>RGB</sub> ist die nicht vormultiplikierte Quellfarbe.
-   F<sub>A</sub> ist quell alpha
-   *f*(S <sub>RGB</sub>, D <sub>RGB)</sub>ist eine Blendfunktion, die je nach Blendmodus variiert.

Einige der Mischungsmodi erfordern eine Konvertierung in und aus dem Farbraum für Farbton, Sättigung, Helligkeit (HSL) in RGB.




| Enumeration | Gleichung | 
|-------------|----------|
| D2D1_BLEND_MODE_DARKEN | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /> | 
| D2D1_BLEND_MODE_MULTIPLY | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /> | 
| D2D1_BLEND_MODE_COLOR_BURN | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /> | 
| D2D1_BLEND_MODE_LINEAR_BURN | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /> | 
| D2D1_BLEND_MODE_DARKER_COLOR | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /> | 
| D2D1_BLEND_MODE_LIGHTEN | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /> | 
| D2D1_BLEND_MODE_SCREEN | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /> | 
| D2D1_BLEND_MODE_COLOR_DODGE | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /> | 
| D2D1_BLEND_MODE_LINEAR_DODGE | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /> | 
| D2D1_BLEND_MODE_LIGHTER_COLOR | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /> | 
| D2D1_BLEND_MODE_OVERLAY | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /> | 
| D2D1_BLEND_MODE_SOFT_LIGHT | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /> | 
| D2D1_BLEND_MODE_HARD_LIGHT | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /> | 
| D2D1_BLEND_MODE_VIVID_LIGHT | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /> | 
| D2D1_BLEND_MODE_LINEAR_LIGHT | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /> | 
| D2D1_BLEND_MODE_PIN_LIGHT | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /> | 
| D2D1_BLEND_MODE_HARD_MIX | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /> | 
| D2D1_BLEND_MODE_DIFFERENCE | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>) | 
| D2D1_BLEND_MODE_EXCLUSION | Einfache Mischungsformeln mit <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 * F<sub>RGB</sub> * B<sub>RGB</sub> | 
| D2D1_BLEND_MODE_HUE | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /> | 
| D2D1_BLEND_MODE_SATURATION | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /> | 
| D2D1_BLEND_MODE_COLOR | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /> | 
| D2D1_BLEND_MODE_LUMINOSITY | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /> | 
| D2D1_BLEND_MODE_DISSOLVE | Gegeben:<ul><li>Eine Szenenkoordinate XY für das aktuelle Pixel</li><li>Ein deterministischer Pseudozufallszahlengenerator rand (XY) basierend auf der Startkoordinaten-XY mit unvoreingenommener Verteilung von Werten aus [0, 1]</li></ul><br /><img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br /> | 
| D2D1_BLEND_MODE_SUBTRACT | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /> | 
| D2D1_BLEND_MODE_DIVISION | Einfache Mischungsformel nur für Alpha. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /> | 




 

> [!Note]  
> Für alle Blend-Modi ist der Ausgabewert prämultipliziert und an den Bereich \[ 0, 1 klammert. \]

 

## <a name="hsl-color-space-conversions"></a>HSL-Farbraumkonvertierungen

Die Helligkeitskomponente wird mithilfe der RGB-Gewichtungen hier berechnet:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Konvertieren von RGB in HSL

![mathematische Formel, die die Transformation von rgb-Farbe in hsl-Farbe beschreibt.](images/blend-rgb-to-hsl-1.png)

Dadurch werden *S* und *L* im Bereich \[ 0,0, 1,0 \] und *H* im Bereich \[ -1,0, 5,0 \] platziert.

### <a name="converting-from-hsl-to-rgb"></a>Konvertieren von HSL in RGB

Um die umgekehrte Methode zu konvertieren, verwenden wir die Umkehrung der vorherigen Berechnungen.

Wenn *S* = 0 ist, dann *R*  =  *G*  =  *B*  =  *L*

Andernfalls gibt es sechs hue-abhängige Fälle:

Wenn *H* größer als 0 ist, befinden sich die Werte im Rot-Magenta-Sektor, in dem *R*  >  *B*  >  *G* liegt.

![mathematischer equaiton-Schritt 1 von sechs Konvertierungen der hsl-Farbe in rgb.](images/blend-hsl-to-rgb-1rm.png)

Wenn *H* größer oder gleich 0 und kleiner als 1 ist, befinden sich die Werte im rot-gelben Sektor, in dem *R*  >  *G*  >  *B*.

![mathematisches equaiton Schritt 2 von sechs Konvertieren der hsl-Farbe in rgb.](images/blend-hsl-to-rgb-1ry.png)

Wenn *H* größer oder gleich 1 und kleiner als 2 ist, befinden sich die Werte im gelben/grünen Sektor, in dem *G*  >  *R*  >  *B*.

![mathematisches equaiton Schritt 3 von sechs Konvertieren der hsl-Farbe in rgb.](images/blend-hsl-to-rgb-1yg.png)

Wenn *H* größer oder gleich 2 und kleiner als 3 ist, befinden sich die Werte im Grün/Cyan-Sektor, in dem *G*  >  *B*  >  *R*.

![mathematisches equaiton Schritt 4 von sechs Konvertieren der hsl-Farbe in rgb.](images/blend-hsl-to-rgb-1gc.png)

Wenn *H* größer oder gleich 3 und kleiner als 4 ist, befinden sich die Werte im Cyan/Blue-Sektor, in dem *B*  >  *G*  >  *R*.

![mathematischer equaiton Schritt 5 von sechs Konvertierung der hsl-Farbe in rgb.](images/blend-hsl-to-rgb-1cb.png)

Wenn *H* größer oder gleich 4 ist, befinden sich die Werte im blauen/magenta-Sektor, in dem *B*  >  *R*  >  *G liegt.*

![mathematisches equaiton Schritt 6 von sechs Konvertieren der hsl-Farbe in rgb.](images/blend-hsl-to-rgb-1bm.png)

Da die Mischungsmodi beliebige Kombinationen von HSL-Komponenten aus zwei verschiedenen Farben erstellen, ist es üblich, dass der konvertierte RGB-Wert out-of-gamut ist, d. h., eine oder mehrere Kanalkomponenten können außerhalb des zulässigen Bereichs von \[ 0,0, 1,0 \] liegen. Diese Farben werden wieder in den Gamut gebracht, indem die Sättigung minimal reduziert wird, während sowohl Farbton als auch Helligkeit beibehalten werden:

![mathematische Formel, die die Korrekturen beschreibt, die für out-of-gamut-Instanzen erforderlich sind.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Ausgabebitmap

Die Ausgabebitmap für diesen Effekt ist immer die Größe der Vereinigung der beiden Eingabebilder.

## <a name="sample-code"></a>Beispielcode

Laden Sie für ein Beispiel für diesen Effekt das [Direct2D-Beispiel für zusammengesetzte Effektmodi](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)herunter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

