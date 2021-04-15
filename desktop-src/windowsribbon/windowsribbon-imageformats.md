---
title: Angeben von Menüband-Bild Ressourcen
description: Als umfassendes Befehls Präsentationssystem ist das Windows-Menüband-Framework so konzipiert, dass Bild Ressourcen in der gesamten Multifunktionsleisten-Benutzeroberfläche (UI) unterstützt werden. Alle Bild Ressourcen werden im Menüband-Markup deklariert oder von einer Menüband-Host Anwendung abgefragt.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Windows-Menüband, Bild Ressourcen
- Menüband, Bild Ressourcen
- Windows-Menüband, Transparenz
- Multifunktionsleiste, Transparenz
- Windows-Menüband, Farbtiefe
- Menüband, Farbtiefe
- Windows-Menüband, Kontrast
- Menüband, Kontrast
- Bild Ressourcen in der Windows-Multifunktionsleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473924"
---
# <a name="specifying-ribbon-image-resources"></a>Angeben von Menüband-Bild Ressourcen

Als umfassendes Befehls Präsentationssystem ist das Windows-Menüband-Framework so konzipiert, dass Bild Ressourcen in der gesamten Multifunktionsleisten-Benutzeroberfläche (UI) unterstützt werden. Alle Bild Ressourcen werden im [Menüband-Markup](windowsribbon-schema.md) deklariert oder von einer Menüband-Host Anwendung abgefragt.

Für Windows 8 und höher unterstützt das Menüband-Framework die folgenden Grafikformate: 32-Bit-ARGB-Bitmap-Dateien (BMP) und Portable Network Graphics-Dateien (PNG) mit Transparenz.

Für Windows 7 und früher müssen Bild Ressourcen dem standardmäßigen BMP-Grafikformat entsprechen, das in Windows verwendet wird.

> [!Note]  
> Ein Kompilierungsfehler kann auftreten, wenn ein nicht unterstütztes Bildformat für das Framework bereitgestellt wird.

 

## <a name="image-sizes"></a>Bildgrößen

Um bei der Größenänderung eines Anwendungsfensters eine größere Flexibilität für die Layouts von Menüband-Steuerelementen zu bieten, akzeptiert und rendert das Menüband-Framework Bilder in einer von zwei Größen: groß oder klein.

Die folgenden Bilder veranschaulichen eine Multifunktionsleistenanwendung, die mehrere Menü Bandgrößen durch flexible Steuerelement Layouts und die Ersetzung großer Bilder mit kleinen, soweit verfügbaren Bildern unterstützt.

Der folgende Screenshot zeigt das Menüband mit großen Bildern für die Zoom Steuerelemente.

![Screenshot, der ein Menüband anzeigt, das große Bilder für die Zoom Steuerelemente verwendet.](images/overviews/imageresources-largeimage.png)

Der folgende Screenshot zeigt, wie die Größe des Menübands mit kleinen Bildern für die Zoom Steuerelemente geändert wird.

![Screenshot, der ein Menüband anzeigt, das kleine Bilder für die Zoom Steuerelemente verwendet.](images/overviews/imageresources-smallimage.png)

Der folgende Screenshot zeigt das Menüband im ausgeblendeten Zustand. Das Menüband ist ausgeblendet, wenn alle möglichen Layouts der Steuerelemente erschöpft sind und das Menüband nicht mit einem verwendbaren Anwendungs Arbeitsbereich gerendert werden kann.

![Screenshot mit einem reduzierten Menüband](images/overviews/imageresources-noimage.png)

Für ein beliebiges Bild ist die genaue Pixelgröße von der Bildschirmauflösung oder von dpi (dots per inch) des verwendeten Monitors abhängig. Bei 96 dpi liegen große Bilder bei einer Größe von 32 x 32 Pixel und bei kleinen Bildern um 16 x 16 Pixel. Die Bildgrößen steigen auf lineare Weise relativ zu dpi, wie in der folgenden Tabelle dargestellt.



| DPI     | Kleines Bild  | Großes Bild  |
|---------|--------------|--------------|
| 96 dpi  | 16x16 Pixel | 32 x 32 Pixel |
| 120 dpi | 20 x 20 Pixel | 40 x 40 Pixel |
| 144 dpi | 24 x 24 Pixel | 48 x 48 Pixel |
| 192 dpi | 32 x 32 Pixel | 64x64 Pixel |



 

Das Menüband-Framework skaliert Bild Ressourcen nach Bedarf. Da die Größe der Größe jedoch unerwünschte Artefakte und Bildverschlechterung verursachen kann, wird dringend empfohlen, dass die Anwendung einen kleinen Satz von Bild Ressourcen bereitstellt, die verschiedene häufig verwendete dpi-Einstellungen umfassen. Wenn keine genaue Entsprechung gefunden wird, wird das nächste Bild zentral hoch-oder herunterskaliert.

Um dies zu vereinfachen, können Bild Ressourcen in Menüband-Markup mithilfe eines Satzes von [**Bild**](windowsribbon-element-image.md) Elementen für jedes [**Command**](windowsribbon-element-command.md) -Element deklariert werden. Zur Laufzeit wählt das Framework das Bild aus, das auf der Grundlage des *mindpi* -Attributs der einzelnen **Bild** Elemente angezeigt werden soll.

> [!IMPORTANT]
>
> Wenn eine Auflistung von Bild Ressourcen, die für die Unterstützung bestimmter Bildschirm DPI-Einstellungen entworfen wurden, über einen Satz von [**Bild**](windowsribbon-element-image.md) Elementen an das Menüband-Framework übergeben wird, verwendet das Framework das **Bild** mit einem *mindpi* -Attribut Wert, der mit der aktuellen Bildschirm-dpi-Einstellung übereinstimmt.
>
> Wenn kein [**Bild**](windowsribbon-element-image.md) Element mit einem *mindpi* -Wert deklariert wird, der mit der aktuellen Bildschirm dpi-Einstellung übereinstimmt, wählt das Framework das **Bild** aus, das den nächstgelegenen *mindpi* -Wert aufweist, der kleiner ist als die aktuelle Bildschirm dpi-Einstellung, und skaliert die Bildressource Wenn kein **Bild** Element mit einem *mindpi* -Attribut Wert, der kleiner als die aktuelle Bildschirm dpi-Einstellung ist, deklariert ist, wählt das Framework den nächsten *mindpi* -Wert aus, der größer als die aktuelle Bildschirm dpi-Einstellung ist, und skaliert die Bildressource nach unten.

 

Im folgenden Beispiel wird veranschaulicht, wie Sie einen Satz von Bildern deklarieren, um verschiedene Menü Bandgrößen und Systemeinstellungen zu unterstützen.


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



Wenn Images, die im Markup deklariert sind, zur Laufzeit aus irgendeinem Grund ungültig gemacht werden, wird die Host Anwendung nach neuen Bildern abgefragt. Wenn diese Images Programm gesteuert generiert und geladen werden, sollte die Anwendung versuchen, Bilder zurückzugeben, deren Größe den von der [SM \_ cxicon-System Metrik](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)festgelegten Standard-System Symbolgrößen entspricht.

> [!Note]  
> Große Bilder haben eine Größe von SM \_ cxicon von SM \_ cxicon, und kleine Images haben eine Größe von SM \_ cxicon/2 von SM \_ cxicon/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Farbtiefe, Transparenz und Kontrast

Es wird erwartet, dass reguläre Images im BPP-ARGB-Pixel Format (32 Bits pro Pixel) vorliegen und auf die standardmäßige System Symbolgröße skaliert werden. Dieses Format unterstützt Transparenz und Antialiasing (bei Verwendung von 8 Bits pro Kanal).

> [!WARNING]
> Viele Tools zur Bildbearbeitung behalten beim Laden oder Speichern von 32 bpp-Images nicht den 8-Bit-Alphakanal mit der höchsten Ordnung bei.

 

Damit ein Bild im Modus mit hohem Kontrast ordnungsgemäß angezeigt wird, muss es in einem 4-bpp-Format mit Palettengröße angezeigt werden. Wenn das Bild gerendert wird, ordnet das Menüband-Framework bestimmte Farben auf Grundlage des Kontrast Bilds des Bilds neu zu.

In der folgenden Tabelle wird das Farb Rendering Verhalten mit hohem Kontrast des Frameworks aufgelistet.



Pixelfarbe

RGB-Wert

Verhalten

Weißer Hintergrund

Dunkler Hintergrund

Magenta

800080

Transparent

Transparent

Box

000000

\_WindowText-Farbe

Weisse

Weisse

FFFFFF

Farb \_ Fenster

Box

dunkelgrau

808080

Farbe \_ 3dshadow

Farbe \_ 3dshadow

Grau

C0C0C0

Farbe \_ 3dface

Farbe \_ 3dface

hellgrau

Dfdfdf

Farbe \_ 3dlight

Farbe \_ 3dlight

dunkelblau

000080

–

Weisse



 

Weitere Informationen zu den vom Menüband-Framework unterstützten Bildformaten finden Sie in den folgenden Bereichen:

-   [BITMAPINFOHEADER-Struktur](/previous-versions//dd183376(v=vs.85)) : Beschreibt das 32 bpp-ARGB-Pixel Format.
-   [Funktion "deedibsection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) ": Beschreibt das Erstellen eines 32 bpp-ARGB-Pixel Formatierungs Bilds.
-   [LoadImage-Funktion](/windows/win32/api/winuser/nf-winuser-loadimagea) : Beschreibt das Laden eines 32 bpp-ARGB-Pixel Formatierungs Bilds.

## <a name="accessibility"></a>Eingabehilfen

Die Verwendung von Bild Ressourcen, um Informationen bereitzustellen, Steuerungsfunktionen zu vermitteln und den Anwendungs Zustand verfügbar zu machen, erhöht den Bedarf an Barrierefreiheits Anforderungen beim Entwerfen und entwickeln von Anwendungen.

Für grundlegende Unterstützung für hohe Kontraste ermöglicht das Menüband, dass ein separater Satz von Bilddateien angezeigt wird, wenn ein Design mit hohem Kontrast aktiv ist. Diese Bilder können 32 bpp oder 4 bpp sein, wobei Farben einer speziellen Palette zugeordnet werden, wobei dunkle und helle Farben in Abhängigkeit von der Vordergrund-und Hintergrundfarbe des aktiven Designs mit hohem Kontrast invertiert werden.

Im folgenden Beispiel wird veranschaulicht, wie Bild Ressourcen mit hohem Kontrast im Menüband-Markup deklariert werden:


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

[**Command. smallimages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[UI \_ pkey \_ smallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Command. largeimages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[UI \_ pkey \_ largeimage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Command. smallhighkontra stimages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[UI \_ pkey \_ smallhighkontra stimage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Command. largehighkontra stimages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[UI \_ pkey \_ largehighkontra stimage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 