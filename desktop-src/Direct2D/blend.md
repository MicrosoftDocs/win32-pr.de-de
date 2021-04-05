---
title: Fülleffekt
description: Verwenden Sie den Blend-Effekt, um 2 Bilder zu kombinieren. Dieser Effekt hat 26 Blend-Modi.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- Blend-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859229"
---
# <a name="blend-effect"></a>Fülleffekt

Verwenden Sie den Blend-Effekt, um 2 Bilder zu kombinieren. Dieser Effekt hat 26 Blend-Modi.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Blend.

-   [Kombination von Beispielen](#blending-examples)
-   [Effekt Eigenschaften](#effect-properties)
-   [Blend-Modi](#blend-modes)
-   [HSL-Farb Raum Konvertierungen](#hsl-color-space-conversions)
    -   [Umstellen von RGB in HSL](#converting-from-rgb-to-hsl)
    -   [Umstellen von HSL in RGB](#converting-from-hsl-to-rgb)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Beispielcode](#sample-code)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="blending-examples"></a>Kombination von Beispielen

Im folgenden finden Sie ein Beispiel Bild für jeden Blend-Modus des Blend-Effekts. Eine vollständige Liste der Blend-Modi und der entsprechenden moduseigenschaften finden Sie im nächsten Abschnitt.

![Beispiel: Screenshot aller verfügbaren Blend-Modi.](images/blend-modes.png)

Im folgenden finden Sie ein weiteres Beispiel für die Verwendung des Ausschluss Modus.



| Vor Bild 1                                                             |
|----------------------------------------------------------------------------|
| ![das erste Quell Bild vor dem Effekt.](images/default-before.jpg)    |
| Vor Abbildung 2                                                             |
| ![Das zweite Bild vor dem Effekt.](images/4-arthimetic-composite2.jpg) |
| Nach                                                                      |
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



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                 | BESCHREIBUNG                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> D2D1 \_ Blend- \_ Prop- \_ Modus<br/> | Der für den Effekt verwendete Blend-Modus. Weitere Informationen finden Sie unter [Blend-Modi](#blend-modes) . Der Typ ist der D2D1 \_ Blend- \_ Modus.<br/> Der Standardwert ist D2D1 \_ Blend \_ Mode \_ Multiplikation.<br/> |



 

## <a name="blend-modes"></a>Füllmethoden

In der hier aufgeführten Tabelle werden alle Blend-Modi dieses Effekts angezeigt. Die Hilfsfunktionen, die erforderlich sind, um die Ausgabe des Effekts zu berechnen, finden Sie im nächsten Abschnitt.

Farbe: O <sub>prgb</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* b <sub>A</sub> \* (1-f <sub>a</sub>)

Alpha: O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub>

Hierbei gilt:

-   O<sub>prgb</sub> ist die vorab multiplizierte Ausgabe Farbe
-   O<sub>A</sub> ist Ausgabe Alpha
-   B<sub>RGB</sub> ist die nicht vorab multiplizierte Zielfarbe
-   B<sub>a</sub> ist Destination Alpha
-   F<sub>RGB</sub> ist die nicht vorab multiplizierte Quellfarbe
-   F<sub>A</sub> ist Quell-Alpha
-   *f*(S <sub>RGB</sub>, D <sub>RGB</sub>) ist eine Blend-Funktion, die je nach Blend-Modus variiert.

Einige der Blend-Modi erfordern eine Konvertierung in den und aus dem Farbton-, Sättigungs-und Helligkeits Raum (HSL) in RGB.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enumeration</th>
<th>Gleichung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKEN</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_MULTIPLY</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_COLOR_BURN</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LINEAR_BURN</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKER_COLOR</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTEN</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SCREEN</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR_DODGE</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_DODGE</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTER_COLOR</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_OVERLAY</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_SOFT_LIGHT</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_LIGHT</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_VIVID_LIGHT</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_LIGHT</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_PIN_LIGHT</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_MIX</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIFFERENCE</td>
<td>Einfache Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = Abs (f<sub>RGB</sub> - B<sub>RGB</sub>)</td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_EXCLUSION</td>
<td>Grundlegende Blend-Formeln mit <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = f<sub>RGB</sub> + b<sub>RGB</sub>   2 * f<sub>RGB</sub> * b<sub>RGB</sub></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_HUE</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SATURATION</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LUMINOSITY</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DISSOLVE</td>
<td>Gegeben:
<ul>
<li>Eine Szenen Koordinaten-XY für das aktuelle Pixel</li>
<li>Ein deterministischer Pseudozufallszahlen Generator Rand (XY), der auf der Ausgangswert-Koordinate (XY) basiert, mit einer unausgewogenen Verteilung der Werte von [0,0]</li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SUBTRACT</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIVISION</td>
<td>Einfache Blend-Formel nur für Alpha. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Für alle Blend-Modi wird der Ausgabewert vorab multipliziert und an den Bereich \[ 0, 1 gebunden \] .

 

## <a name="hsl-color-space-conversions"></a>HSL-Farb Raum Konvertierungen

Die Komponente "Brillanz" wird mithilfe der RGB-Gewichtungen berechnet:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Umstellen von RGB in HSL

![mathematische Formel, die die Transformation zwischen RGB-Farbe und HSL-Farbe beschreibt.](images/blend-rgb-to-hsl-1.png)

Dabei werden *S* und *L* im Bereich von \[ \] -1,0, 5,0  und L im Bereich von 0,0, 1,0 und H platziert \[ \] .

### <a name="converting-from-hsl-to-rgb"></a>Umstellen von HSL in RGB

Um die andere Methode zu konvertieren, verwenden wir die Umkehrung der vorherigen Berechnungen.

Wenn *S* = 0, dann *R*  =  *G*  =  *B*  =  *L*

Andernfalls gibt es sechs von Hue abhängige Fälle:

Wenn *H* größer als 0 ist, befinden sich die Werte im red/Magenta-Sektor, in dem *R*  >  *B*  >  *G* ist.

![mathematische equaiton-Schritt 1 von sechs, der die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1rm.png)

Wenn *H* größer oder gleich 0 und kleiner als 1 ist, befinden sich die Werte im roten/gelben Sektor, in dem *R*  >  *G*  >  *B* liegt.

![mathematische equaiton-Schritt 2 von sechs, der die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1ry.png)

Wenn *H* größer oder gleich 1 und kleiner als 2 ist, befinden sich die Werte im gelben/grünen Sektor, in dem *G*  >  *R*  >  *B*.

![mathematische equaiton-Schritt 3 von sechs, der die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1yg.png)

Wenn *H* größer oder gleich 2 und kleiner als 3 ist, befinden sich die Werte im grünen/Cyan-Sektor, in dem *G*  >  *B*  >  *R* liegt.

![mathematische equaiton-Schritt 4 von sechs, die die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1gc.png)

Wenn *H* größer oder gleich 3 und kleiner als 4 ist, befinden sich die Werte im Cyan/Blue-Sektor, in dem *B*  >  *G*  >  *R* liegt.

![mathematische equaiton Step 5 of Six, um die HSL-Farbe in RGB umzuwandeln.](images/blend-hsl-to-rgb-1cb.png)

Wenn *H* größer oder gleich 4 ist, befinden sich die Werte im Blue/Magenta-Sektor, in dem *B*  >  *R*  >  *G* ist.

![mathematische equaiton-Schritt 6 von sechs, die die HSL-Farbe in RGB umwandelt.](images/blend-hsl-to-rgb-1bm.png)

Da die Mischungs Modi beliebige Kombinationen von HSL-Komponenten aus zwei unterschiedlichen Farben bilden, ist es üblich, dass der konvertierte RGB-Wert außerhalb des Spiel Bereichs liegt, d. h., eine oder mehrere channelkomponenten liegen möglicherweise außerhalb des gültigen Bereichs von \[ 0,0, 1,0 \] . Diese Farben werden wieder in den Farbskala eingefügt, indem die Sättigung minimal reduziert und sowohl Farbton als auch Helligkeit beibehalten werden:

![mathematische Formel, die die Korrekturen beschreibt, die für nicht von Farbskala Instanzen erforderlich sind.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Ausgabe Bitmap

Das Ausgabe Bitmap für diesen Effekt ist immer die Größe der Union der beiden Eingabe Bilder.

## <a name="sample-code"></a>Beispielcode

Um ein Beispiel für diesen Effekt zu erhalten, laden Sie das [Beispiel Direct2D Composite Effect Modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)herunter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

