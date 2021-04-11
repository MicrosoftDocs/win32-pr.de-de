---
title: Verwenden von Color in Direct2D
description: Verwenden von Color in Direct2D
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb195a4ad0bdd9ff32f1123a8a57ff2ce0aadbde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314823"
---
# <a name="using-color-in-direct2d"></a>Verwenden von Color in Direct2D

Direct2D verwendet das RGB-Farbmodell, in dem Farben durch Kombinieren verschiedener Werte von rot, grün und blau gebildet werden. Eine vierte Komponente, Alpha, misst die Transparenz eines Pixels. In Direct2D ist jede dieser Komponenten ein Gleit Komma Wert mit einem Bereich von \[ 0,0 1,0 \] . Bei den drei Farbkomponenten misst der Wert die Intensität der Farbe. Bei der Alpha Komponente bedeutet 0,0 vollständig transparent, und 1,0 bedeutet vollständig nicht transparent. In der folgenden Tabelle werden die Farben angezeigt, die sich aus verschiedenen Kombinationen von 100% Intensität ergeben.



| Red | Grün | Blau | Color   |
|-----|-------|------|---------|
| 0   | 0     | 0    | Schwarz   |
| 1   | 0     | 0    | Red     |
| 0   | 1     | 0    | Grün   |
| 0   | 0     | 1    | Blau    |
| 0   | 1     | 1    | Cyan    |
| 1   | 0     | 1    | Magenta |
| 1   | 1     | 0    | Gelb  |
| 1   | 1     | 1    | Weiß   |



 

![ein Bild, in dem RGB-Farben angezeigt werden.](images/graphics13.png)

Farbwerte zwischen 0 und 1 führen zu unterschiedlichen Schattierungen dieser reinen Farben. Direct2D verwendet die [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Struktur zur Darstellung von Farben. Im folgenden Code wird beispielsweise Magenta angegeben.


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



Sie können auch eine Farbe mithilfe der [**D2D1:: colorf**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) -Klasse angeben, die von der [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Struktur abgeleitet ist.


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Alpha Blending

Alpha Blending erstellt durch eine Kombination der Vordergrundfarbe mit der Hintergrundfarbe die folgende Formel.

<dl> Color = AF * CF + (1-AF) * CB  
</dl>

Wenn *CB* die Hintergrundfarbe ist, ist *CF* die Vordergrundfarbe, und *AF* ist der Alpha Wert der Vordergrundfarbe. Diese Formel wird auf jede Farbkomponente paarweise angewendet. Angenommen, die Vordergrundfarbe lautet **(r = 1,0, g = 0,4, b = 0,0)** mit **Alpha = 0,6** und die Hintergrundfarbe **(r = 0,0, g = 0,5, b = 1,0)**. Die resultierende Alpha gemischte Farbe lautet wie folgt:

R = (1,0 × 0,6 + 0 * 0,4) =. 6   
G = (0,4 × 0,6 + 0,5 * 0,4) =. 44  
B = (0 * 0,6 + 1,0 * 0,4) =. 40  

Die folgende Abbildung zeigt das Ergebnis dieses Mischungs Vorgangs.

![ein Bild, das Alpha Blending anzeigt.](images/graphics15.png)

## <a name="pixel-formats"></a>Pixel Formate

In der [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Struktur wird nicht beschrieben, wie ein Pixel im Arbeitsspeicher dargestellt wird. In den meisten Fällen spielt dies keine Rolle. Direct2D behandelt alle internen Details der Übersetzung von Farbinformationen in Pixel. Möglicherweise müssen Sie jedoch das Pixel Format kennen, wenn Sie direkt mit einer Bitmap im Arbeitsspeicher arbeiten, oder wenn Sie Direct2D mit Direct3D oder GDI kombinieren.

Die [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) definiert eine Liste von Pixel Formaten. Die Liste ist recht lang, aber nur einige davon sind für Direct2D relevant. (Die anderen werden von Direct3D verwendet.)



| Pixel Format                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**DXGI- \_ Format \_ B8G8R8A8 \_ unorm**<br/> | Dies ist das gängigste Pixel Format. Alle Pixel Komponenten (rot, grün, blau und Alpha) sind 8-Bit-Ganzzahlen ohne Vorzeichen. Die Komponenten werden in der *BGRA* -Reihenfolge im Arbeitsspeicher angeordnet. (Siehe Abbildung unten.)<br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**DXGI- \_ Format \_ R8G8B8A8 \_ unorm**<br/> | Pixel Komponenten sind 8-Bit-Ganzzahlen ohne Vorzeichen in *RGBA* -Reihenfolge. Das heißt, die roten und blauen Komponenten werden in Relation zum **DXGI- \_ Format \_ B8G8R8A8 \_ unorm** ausgetauscht. Dieses Format wird nur für Hardware Geräte unterstützt.<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**DXGI- \_ Format \_ a8 \_ unorm**<br/>                   | Dieses Format enthält eine 8-Bit-Alpha Komponente ohne RGB-Komponenten. Dies ist nützlich zum Erstellen von Deck Kraft Masken. Weitere Informationen zum Verwenden von Deck Kraft Masken in Direct2D finden Sie unter [kompatible A8-Renderziele (Übersicht](/windows/desktop/Direct2D/compatible-a8-rendertargets)).<br/> |



 

In der folgenden Abbildung wird das BGRA-Pixel Layout dargestellt.

![ein Diagramm, das das BGRA-Pixel Layout anzeigt.](images/graphics14.png)

Um das Pixel Format eines Renderziels abzurufen, nennen Sie [**ID2D1RenderTarget:: GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat). Das Pixel Format entspricht möglicherweise nicht der Bildschirmauflösung. Beispielsweise kann die Anzeige auf eine 16-Bit-Farbe festgelegt werden, auch wenn das Renderziel eine 32-Bit-Farbe verwendet.

### <a name="alpha-mode"></a>Alpha-Modus

Ein Renderziel verfügt auch über einen Alpha-Modus, der definiert, wie die Alpha Werte behandelt werden.



| Alpha-Modus                           | Beschreibung                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D2D1 \_ alpha \_ Modus \_ ignorieren**        | Es erfolgt keine Alpha Mischung. Alpha Werte werden ignoriert.                                                                                                                                                                                                                                                                          |
| **D2D1 \_ alpha \_ Modus \_ direkt**      | Gerade alpha. Die Farbkomponenten des Pixels stellen die Farbintensität vor Alpha Blending dar.                                                                                                                                                                                                                           |
| **D2D1 \_ alpha \_ Modus ist \_ vorab multipliziert** | Ein prämultipliziertes alpha. Die Farbkomponenten des Pixels stellen die Farbintensität multipliziert mit dem Alpha-Wert dar. Dieses Format ist effizienter zum renderingwert, als gerade Alpha, da der Begriff (AF CF) aus der Alpha Mischungs Formel voraus berechnet ist. Dieses Format eignet sich jedoch nicht für das Speichern in einer Bilddatei. |



 

Im folgenden finden Sie ein Beispiel für den Unterschied zwischen einem geraden Alpha und einem prämultiplizierten alpha. Angenommen, die gewünschte Farbe ist rein rot (100% Intensität) mit 50% alpha. Als Direct2D-Typ würde diese Farbe als (1, 0, 0, 0,5) dargestellt werden. Die rote Komponente des Pixels ist 0xFF, bei der die Verwendung von Straight Alpha und der Annahme von 8-Bit-Farbkomponenten erfolgt. Bei Verwendung von prämultipliziertem Alpha wird die rote Komponente um 50% auf denselben Wert von 0x80 skaliert.

Der [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Datentyp stellt immer Farben dar, die gerade Alpha verwendet. Direct2D konvertiert Pixel bei Bedarf in ein prämultipliziertes Alpha Format.

Wenn Sie wissen, dass das Programm keine Alpha Mischung durchführt, erstellen Sie das Renderziel mit dem Modus " **D2D1 \_ Alpha Mode \_ \_ Ignore** ". Dieser Modus kann die Leistung verbessern, da Direct2D die Alpha Berechnungen überspringen kann. Weitere Informationen finden Sie unter [verbessern der Leistung von Direct2D-Anwendungen](/windows/desktop/Direct2D/improving-direct2d-performance).

## <a name="next"></a>Nächste

[Anwenden von Transformationen in Direct2D](applying-transforms-in-direct2d.md)

 

