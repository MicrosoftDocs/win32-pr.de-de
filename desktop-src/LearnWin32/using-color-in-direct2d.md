---
title: Verwenden von Farben in Direct2D
description: Verwenden von Farben in Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe6ded6d181ebcbca402161fe6af0b8fb8dd65f7d082632474136a9bd1ff551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631524"
---
# <a name="using-color-in-direct2d"></a>Verwenden von Farben in Direct2D

Direct2D verwendet das RGB-Farbmodell, in dem Farben durch Kombination verschiedener Werte von Rot, Grün und Blau gebildet werden. Die vierte Komponente alpha misst die Transparenz eines Pixels. In Direct2D ist jede dieser Komponenten ein Gleitkommawert mit einem Bereich von \[ 0,0 1,0 \] . Für die drei Farbkomponenten misst der Wert die Intensität der Farbe. Für die Alphakomponente bedeutet 0.0 vollständig transparent, und 1.0 bedeutet vollständig deckend. Die folgende Tabelle zeigt die Farben, die sich aus verschiedenen Kombinationen von 100 % Intensität ergeben.



| Red | Grün | Blau | Color   |
|-----|-------|------|---------|
| 0   | 0     | 0    | Schwarz   |
| 1   | 0     | 0    | Red     |
| 0   | 1     | 0    | Grün   |
| 0   | 0     | 1    | Blau    |
| 0   | 1     | 1    | Cyan    |
| 1   | 0     | 1    | Magenta |
| 1   | 1     | 0    | Gelb  |
| 1   | 1     | 1    | White   |



 

![Ein Bild, das RGB-Farben zeigt.](images/graphics13.png)

Farbwerte zwischen 0 und 1 führen zu unterschiedlichen Schattierungen dieser reinen Farben. Direct2D verwendet die [**D2D1 \_ COLOR \_ F-Struktur,**](/windows/desktop/Direct2D/d2d1-color-f) um Farben darzustellen. Der folgende Code gibt z. B. Magenta an.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



Sie können eine Farbe auch mithilfe der [**D2D1::ColorF-Klasse**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) angeben, die von der [**D2D1 \_ COLOR \_ F-Struktur**](/windows/desktop/Direct2D/d2d1-color-f) abgeleitet wird.


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Alphablending

Bei der Alphamischung werden durch die Kombination der Vordergrundfarbe mit der Hintergrundfarbe mithilfe der folgenden Formel durchscheinende Bereiche erstellt.

<dl> color = af * Cf + (1 - af) * Cb  
</dl>

Wobei *Cb* die Hintergrundfarbe, *Cf* die Vordergrundfarbe und *af* der Alphawert der Vordergrundfarbe ist. Diese Formel wird paarweise auf jede Farbkomponente angewendet. Angenommen, die Vordergrundfarbe ist **(R = 1,0, G = 0,4, B = 0,0)**, mit **alpha = 0,6,** und die Hintergrundfarbe ist **(R = 0,0, G = 0,5, B = 1,0).** Die resultierende Alphablendfarbe lautet:

R = (1,0 * 0,6 + 0 * 0,4) = .6   
G = (0,4 * 0,6 + 0,5 * 0,4) = .44  
B = (0 * 0,6 + 1,0 * 0,4) = .40  

Die folgende Abbildung zeigt das Ergebnis dieses Mischungsvorgangs.

![Ein Bild, das Alphablending zeigt.](images/graphics15.png)

## <a name="pixel-formats"></a>Pixelformate

Die [**D2D1 \_ COLOR \_ F-Struktur**](/windows/desktop/Direct2D/d2d1-color-f) beschreibt nicht, wie ein Pixel im Arbeitsspeicher dargestellt wird. In den meisten Fällen spielt dies keine Rolle. Direct2D verarbeitet alle internen Details der Übersetzung von Farbinformationen in Pixel. Möglicherweise müssen Sie jedoch das Pixelformat kennen, wenn Sie direkt mit einer Bitmap im Arbeitsspeicher arbeiten oder Direct2D mit Direct3D oder GDI kombinieren.

Die [**DXGI \_ FORMAT-Enumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) definiert eine Liste von Pixelformaten. Die Liste ist relativ lang, aber nur einige davon sind für Direct2D relevant. (Die anderen werden von Direct3D verwendet.)



| Pixelformat                                                                                                                           | Beschreibung                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**<br/> | Dies ist das gängigste Pixelformat. Alle Pixelkomponenten (Rot, Grün, Blau und Alpha) sind 8-Bit-Ganzzahlen ohne Vorzeichen. Die Komponenten werden in *BGRA-Reihenfolge* im Arbeitsspeicher angeordnet. (Weitere Informationen finden Sie in der folgenden Abbildung.)<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM**<br/> | Pixelkomponenten sind 8-Bit-Ganzzahlen ohne Vorzeichen in *RGBA-Reihenfolge.* Anders ausgedrückt: Die roten und blauen Komponenten werden gegenüber **DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM** ausgetauscht. Dieses Format wird nur für Hardwaregeräte unterstützt.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**\_DXGI-FORMAT \_ A8 \_ UNORM**<br/>                   | Dieses Format enthält eine 8-Bit-Alphakomponente ohne RGB-Komponenten. Dies ist nützlich zum Erstellen von Deckkraftmasken. Weitere Informationen zur Verwendung von Deckkraftmasken in Direct2D finden Sie unter [Kompatible A8-Renderziele – Übersicht.](/windows/desktop/Direct2D/compatible-a8-rendertargets)<br/> |



 

Die folgende Abbildung zeigt das BGRA-Pixellayout.

![Ein Diagramm, das das bgra-Pixellayout zeigt.](images/graphics14.png)

Um das Pixelformat eines Renderziels abzurufen, rufen Sie [**ID2D1RenderTarget::GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat)auf. Das Pixelformat stimmt möglicherweise nicht mit der Anzeigeauflösung überein. Beispielsweise kann die Anzeige auf eine 16-Bit-Farbe festgelegt werden, obwohl das Renderziel eine 32-Bit-Farbe verwendet.

### <a name="alpha-mode"></a>Alphamodus

Ein Renderziel verfügt auch über einen Alphamodus, der definiert, wie die Alphawerte behandelt werden.



| Alphamodus                           | Beschreibung                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D2D1 \_ ALPHA \_ MODE \_ IGNORE**        | Es wird keine Alphamischung durchgeführt. Alphawerte werden ignoriert.                                                                                                                                                                                                                                                                          |
| **D2D1 \_ ALPHA \_ MODE \_ STRAIGHT**      | Gerades Alpha. Die Farbkomponenten des Pixels stellen die Farbdichte vor der Alphamischung dar.                                                                                                                                                                                                                           |
| **D2D1 \_ \_ ALPHA-MODUS \_ VORMULTIPLIED** | Prämultipliiertes Alpha. Die Farbkomponenten des Pixels stellen die Farbstärke multipliziert mit dem Alphawert dar. Dieses Format ist effizienter zu rendern als ein gerades Alpha, da der Begriff (af Cf) aus der Alphablendingformel vorab berechnet wird. Dieses Format ist jedoch nicht zum Speichern in einer Bilddatei geeignet. |



 

Hier ist ein Beispiel für den Unterschied zwischen einem geraden alpha und einem prämultipliierten Alpha. Angenommen, die gewünschte Farbe ist rein rot (100 % Intensität) mit 50 % Alpha. Als Direct2D-Typ wird diese Farbe als (1, 0, 0, 0,5) dargestellt. Bei Verwendung eines geraden Alphas und unter Der Annahme von 8-Bit-Farbkomponenten wird die rote Komponente des Pixels 0xFF. Bei Verwendung eines prämultipliierten Alphas wird die rote Komponente um 50 % skaliert, um 0x80.

Der [**D2D1 \_ COLOR \_ F-Datentyp**](/windows/desktop/Direct2D/d2d1-color-f) stellt farben immer mithilfe von geradem Alpha dar. Direct2D konvertiert Pixel bei Bedarf in ein prämultipliiertes Alphaformat.

Wenn Sie wissen, dass das Programm keine Alphablendings durchführen wird, erstellen Sie das Renderziel mit dem Alphamodus **D2D1 \_ ALPHA \_ MODE \_ IGNORE.** Dieser Modus kann die Leistung verbessern, da Direct2D die Alphaberechnungen überspringen kann. Weitere Informationen finden Sie unter [Verbessern der Leistung von Direct2D-Anwendungen.](/windows/desktop/Direct2D/improving-direct2d-performance)

## <a name="next"></a>Nächste

[Anwenden von Transformationen in Direct2D](applying-transforms-in-direct2d.md)

 

