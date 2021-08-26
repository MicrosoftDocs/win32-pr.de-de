---
title: Angeben von Menübandbildressourcen
description: Als umfassendes Befehlspräsentationssystem ist das Windows Menüband-Framework so konzipiert, dass Bildressourcen in der gesamten Menüband-Benutzeroberfläche umfassend unterstützt werden. Alle Bildressourcen werden im Menübandmarkup deklariert oder von einer Menübandhostanwendung abgefragt.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Windows Menüband, Imageressourcen
- Menüband, Imageressourcen
- Windows Menüband, Transparenz
- Menüband, Transparenz
- Windows Menüband, Farbtiefe
- Menüband, Farbtiefe
- Windows Menüband, Kontrast
- Menüband, Kontrast
- Imageressourcen im menüband Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c485de9c0d9d1b51b09d4a2b9dba95dd30a778922750a7f388c7a5c8963cda6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932592"
---
# <a name="specifying-ribbon-image-resources"></a>Angeben von Menübandbildressourcen

Als umfassendes Befehlspräsentationssystem ist das Windows Menüband-Framework so konzipiert, dass Bildressourcen in der gesamten Menüband-Benutzeroberfläche umfassend unterstützt werden. Alle Bildressourcen werden im [Menübandmarkup](windowsribbon-schema.md) deklariert oder von einer Menübandhostanwendung abgefragt.

Für Windows 8 und höher unterstützt das Menübandframework die folgenden Grafikformate: 32-Bit-ARGB-Bitmapdateien (BMP) und PNG-Dateien (Portable Network Graphics) mit Transparenz.

Für Windows 7 und früher müssen Bildressourcen dem in Windows verwendeten BMP-Standardgrafikformat entsprechen.

> [!Note]  
> Ein Kompilierungsfehler kann auftreten, wenn ein nicht unterstütztes Bildformat für das Framework bereitgestellt wird.

 

## <a name="image-sizes"></a>Bildgrößen

Um beim Ändern der Größe eines Anwendungsfensters mehr Flexibilität für Menüband-Steuerelementlayouts zu bieten, akzeptiert und rendert das Menübandframework Bilder in einer von zwei Größen: groß oder klein.

Die folgenden Abbildungen veranschaulichen eine Menübandanwendung, die mehrere Menübandgrößen durch flexible Steuerelementlayouts und den Austausch großer Bilder durch kleine Bilder unterstützt, sofern verfügbar.

Der folgende Screenshot zeigt das Menüband mit großen Bildern für die Zoom-Steuerelemente.

![Screenshot eines Menübands, das große Bilder für die Zoomsteuerelemente verwendet.](images/overviews/imageresources-largeimage.png)

Der folgende Screenshot zeigt die gleiche Größe des Menübands mit kleinen Bildern für die Zoom-Steuerelemente.

![Screenshot eines Menübands, das kleine Bilder für die Zoomsteuerelemente verwendet.](images/overviews/imageresources-smallimage.png)

Der folgende Screenshot zeigt das Menüband im ausgeblendeten Zustand. Das Menüband wird ausgeblendet, wenn alle potenziellen Steuerelementlayouts erschöpft sind und das Menüband nicht mit einem verwendbaren Anwendungsarbeitsbereich gerendert werden kann.

![Screenshot eines reduzierten Menübands.](images/overviews/imageresources-noimage.png)

Für jedes Bild hängt die genaue Pixelgröße von der Anzeigeauflösung bzw. den DPI-Punkten (Dots per Inch) des verwendeten Monitors ab. Bei 96 dpi sind große Bilder 32 x 32 Pixel groß, und kleine Bilder haben eine Größe von 16 x 16 Pixeln. Die Bildgrößen nehmen linear relativ zu dpi zu, wie in der folgenden Tabelle dargestellt.



| DPI     | Kleines Bild  | Großes Bild  |
|---------|--------------|--------------|
| 96 dpi  | 16 x 16 Pixel | 32 x 32 Pixel |
| 120 dpi | 20 x 20 Pixel | 40 x 40 Pixel |
| 144 dpi | 24 x 24 Pixel | 48 x 48 Pixel |
| 192 dpi | 32 x 32 Pixel | 64 x 64 Pixel |



 

Das Menübandframework skaliert Imageressourcen nach Bedarf. Da die Größenänderung jedoch zu unerwünschten Artefakten und image degradation führen kann, wird dringend empfohlen, dass die Anwendung einen kleinen Satz von Imageressourcen bereitstellt, die verschiedene häufig verwendete DPI-Einstellungen umfassen. Wenn keine genaue Übereinstimmung gefunden wird, wird das nächste Bild hoch- oder herunterskaliert.

Um dies zu vereinfachen, können Bildressourcen im Menübandmarkup deklariert werden, indem für jedes [**Command-Element**](windowsribbon-element-command.md) eine Reihe von [**Image-Elementen**](windowsribbon-element-image.md) verwendet wird. Zur Laufzeit wählt das Framework das anzuzeigende Bild basierend auf dem *MinDPI-Attribut* jedes **Image-Elements** aus.

> [!IMPORTANT]
>
> Wenn dem Menübandframework über eine Reihe von [**Bildelementen**](windowsribbon-element-image.md) eine Sammlung von Bildressourcen bereitgestellt wird, die bestimmte Bildschirm-DPI-Einstellungen unterstützen sollen, verwendet das Framework das **Bild** mit einem *MinDPI-Attributwert,* der der aktuellen Bildschirm-DPI-Einstellung entspricht.
>
> Wenn kein [**Image-Element**](windowsribbon-element-image.md) mit einem *MinDPI-Wert* deklariert wird, der der DPI-Einstellung des aktuellen Bildschirms entspricht, wählt das Framework das **Bild** aus, das den nächsten *MinDPI-Wert* kleiner als die aktuelle Bildschirm-DPI-Einstellung hat, und skaliert die Bildressource nach oben. Wenn kein **Image-Element** mit einem *MinDPI-Attributwert* deklariert wird, der kleiner als die aktuelle Bildschirm-DPI-Einstellung ist, wählt das Framework den nächsten *MinDPI-Wert* aus, der größer als die aktuelle Bildschirm-DPI-Einstellung ist, und skaliert die Bildressource herunter.

 

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Satz von Bildern deklarieren, um verschiedene Menübandgrößen und Systemeinstellungen zu berücksichtigen.


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



Wenn im Markup deklarierte Images zur Laufzeit ungültig werden, wird die Hostanwendung nach neuen Images abgefragt. Wenn diese Images programmgesteuert generiert und geladen werden, sollte die Anwendung versuchen, Images zurückzugeben, deren Größe den standardmäßigen Systemsymbolgrößen entspricht, die von der [SM \_ CXICON-Systemmetrik](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)bestimmt werden.

> [!Note]  
> Große Images haben eine Größe von SM \_ CXICON von SM \_ CXICON, und kleine Images haben eine Größe von SM \_ CXICON/2 von SM \_ CXICON/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Farbtiefe, Transparenz und Kontrast

Es wird erwartet, dass reguläre Bilder im ARGB-Pixelformat (BPP) mit 32 Bits pro Pixel vorliegen und auf die Standardsymbolgröße des Systems skaliert werden. Dieses Format unterstützt sowohl Transparenz als auch Antialiasing (mit 8 Bits pro Kanal).

> [!WARNING]
> Viele Bildbearbeitungstools behalten beim Laden oder Speichern von 32 BPP-Bildern nicht den 8-Bit-Alphakanal mit der höchsten Reihenfolge bei.

 

Damit ein Bild im Modus mit hohem Kontrast ordnungsgemäß angezeigt wird, muss es in einem 4 BPP-palettenbasierten Pixelformat vorliegen. Wenn das Bild gerendert wird, weist das Menübandframework bestimmte Farben basierend auf dem Kontext mit hohem Kontrast des Bilds neu zu.

In der folgenden Tabelle ist das Verhalten beim Rendern von Farben mit hohem Kontrast des Frameworks aufgeführt.



Pixelfarbe

RGB-Wert

Verhalten

Weißer Hintergrund

Dunkler Hintergrund

Magenta

800080

Transparent

Transparent

Schwarz

000000

COLOR \_ WINDOWTEXT

Weiß

Weiß

FFFFFF

\_FARBFENSTER

Schwarz

DUNKELGRAU

808080

COLOR \_ 3DSHADOW

COLOR \_ 3DSHADOW

Grau

C0C0C0

COLOR \_ 3DFACE

COLOR \_ 3DFACE

HELLGRAU

DFDFDF

COLOR \_ 3DLIGHT

COLOR \_ 3DLIGHT

Dunkelblau

000080

–

Weiß



 

Weitere Informationen zu den vom Menübandframework unterstützten Bildformaten finden Sie in den folgenden Themen:

-   [BITMAPINFOHEADER-Struktur:](/previous-versions//dd183376(v=vs.85)) Beschreibt das 32-BPP-ARGB-Pixelformat.
-   [CreateDIBSection-Funktion:](/windows/win32/api/wingdi/nf-wingdi-createdibsection) Beschreibt das Erstellen eines Bilds im ARGB-Pixelformat mit 32 BPP.
-   [LoadImage-Funktion:](/windows/win32/api/winuser/nf-winuser-loadimagea) Beschreibt das Laden eines Bilds im ARGB-Pixelformat mit 32 BPP.

## <a name="accessibility"></a>Zugriff

Die Verwendung von Bildressourcen, um Informationen bereitzustellen, Steuerungsfunktionen bereitzustellen und den Anwendungszustand verfügbar zu machen, erhöht den Bedarf an Barrierefreiheitsanforderungen während des Anwendungsentwurfs und der Entwicklung.

Für grundlegende Unterstützung für hohen Kontrast ermöglicht das Menüband die Anzeige eines separaten Satzes von Bilddateien, wenn ein Design mit hohem Kontrast aktiv ist. Diese Bilder können 32 BPP oder 4 BPP sein, wobei Farben einer speziellen Palette zugeordnet sind, in der dunkle und helle Farben je nach Vordergrund- und Hintergrundfarben des aktiven Designs mit hohem Kontrast invertiert werden.

Im folgenden Beispiel wird veranschaulicht, wie Bildressourcen mit hohem Kontrast im Menübandmarkup deklariert werden:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Command.SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Command.LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 