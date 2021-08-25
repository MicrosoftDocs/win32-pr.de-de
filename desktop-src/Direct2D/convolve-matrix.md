---
title: Faltungsmatrixeffekt
description: Verwenden Sie den Konvolve-Matrixeffekt, um einen beliebigen 2D-Kernel auf ein Bild anzuwenden. Sie können diesen Effekt verwenden, um Kanten zu verwischen, Kanten zu erkennen, Einzublenden oder ein Bild zu schärfen.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- Konvolve-Matrixeffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3b988e0bd48fece4d767fad29b63fe021c82d49d07dae5ab3f1b10b3f9794f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833374"
---
# <a name="convolve-matrix-effect"></a>Faltungsmatrixeffekt

Verwenden Sie den Konvolve-Matrixeffekt, um einen beliebigen 2D-Kernel auf ein Bild anzuwenden. Sie können diesen Effekt verwenden, um Kanten zu verwischen, Kanten zu erkennen, Einzublenden oder ein Bild zu schärfen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1ConvolveMatrix.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Skalierungsmodi](#scale-modes)
-   [Rahmenmodi](#border-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das folgende Beispiel zeigt die Eingabe und Ausgabe des Konvolve Matrix-Effekts mit einem 3 x 3-Kernel.



| Vorher                                                         |
|----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)     |
| Danach                                                          |
| ![das Bild nach der Transformation.](images/6-convolvematrix.png) |



 


```C++
ComPtr<ID2D1Effect> convolveMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ConvolveMatrix, &convolveMatrixEffect);

convolveMatrixEffect->SetInput(0, bitmap);
float matrix[9] = {-1, -1, -1, -1, 9, -1, -1, -1, -1};
convolveMatrixEffect->SetValue(D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(convolveMatrixEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Die Größe einer Einheit im Kernel. Die Einheiten befinden sich in (DIPs/Kerneleinheit), wobei eine Kerneleinheit die Größe des Elements im Konvolutionskernel darstellt. Der Wert 1 (DIP/Kerneleinheit) entspricht einem Pixel in einem Bild mit 96 DPI.<br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                   |
| Scalemode<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ SCALE \_ MODE<br/>                 | Der Interpolationsmodus, den der Effekt verwendet, um das Bild auf die entsprechende Kerneleinheitlänge zu skalieren. Es gibt sechs Skalierungsmodi, die in Qualität und Geschwindigkeit reichen.<br/> Der Typ ist D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE.<br/> Der Standardwert ist D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ SIZE \_ X<br/>           | Die Breite der Kernelmatrix. Die Einheiten werden in Kerneleinheiten angegeben. Der Typ ist UINT32.<br/> Der Standardwert ist 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ SIZE \_ Y<br/>           | Die Höhe der Kernelmatrix. Die Einheiten werden in Kerneleinheiten angegeben. Der Typ ist UINT32.<br/> Der Standardwert ist 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ MATRIX<br/>           | Die Kernelmatrix, die auf das Bild angewendet werden soll. Die Kernelelemente werden nicht begrenzt und als Gleitkommaelemente angegeben.<br/> Der erste Satz von *KernelSizeX-Zahlen* im FLOAT \[ \] entspricht der ersten Zeile im Kernel. Der zweite Satz von *KernelSizeX-Zahlen* entspricht der zweiten Zeile usw. bis zu *KernelSizeY-Zeilen.*<br/> Der Typ ist \[ \] FLOAT.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f, 0.0f, 1.0f, 0.0f, 0.0f, 0.0f, 0.0f}.<br/>                                                       |
| Divisor<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ DIVISOR<br/>                       | Die Kernelmatrix wird auf ein Pixel angewendet, und dann wird das Ergebnis durch diesen Wert geteilt. <br/> 0 verhält sich als Wert von float epsilon.<br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 1,0f.<br/>                                                                                                                                                                                                                                                                                                           |
| Verzerrung (Bias)<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ BIAS<br/>                             | Der Effekt wendet die Kernelmatrix, den Divisor, an, und dann wird der Bias dem Ergebnis hinzugefügt. Die Voreingenommenheit ist ungebunden und unitlos. Der Typ ist FLOAT.<br/> Der Standardwert ist 0,0f.<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ OFFSET<br/>           | Verschiebt den Konvolutionskernel von einer zentrierten Position auf dem Ausgabepixel in eine Position, die Sie nach links/rechts und nach oben/unten angeben. Der Offset wird in Kerneleinheiten definiert.<br/> Bei einigen Offsets und Kernelgrößen werden die Stichproben des Konvolutionskernels nicht in einem Pixelbildcenter landen. Die Pixelwerte für das Kernelbeispiel werden durch bilineare Interpolation berechnet.<br/> Der Typ ist D2D1 \_ VECTOR \_ 2F.<br/> Der Standardwert ist {0.0f, 0.0f}.<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ PRESERVE \_ ALPHA<br/>         | Gibt an, ob der Konvolutionskernel auf den Alphakanal oder nur auf die Farbkanäle angewendet wird.<br/> Wenn Sie diese Einstellung auf **TRUE** festlegen, wird der Konvolutionskernel nur auf die Farbkanäle angewendet.<br/> Wenn Sie diese Einstellung auf **FALSE** festlegen, wird der Konvolutionskernel auf alle Kanäle angewendet.<br/> Der Typ ist BOOL.<br/> Der Standardwert ist FALSE.<br/>                                                                                                                                               |
| BorderMode<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ BORDER \_ MODE<br/>               | Der Modus, der zum Berechnen des Rahmens des Bilds verwendet wird( soft oder hard). Weitere Informationen finden Sie unter [Border modes (Rahmenmodi).](https://www.bing.com/search?q=Border+modes)<br/> Der Typ ist D2D1 \_ BORDER \_ MODE.<br/> Der Standardwert ist D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> D2D1 \_ CONVOLVEMATRIX \_ \_ PROP-KLAMMERAUSGABE \_<br/>             | Gibt an, ob der Effekt Farbwerte zwischen 0 und 1 zusammenbindet, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt klammert die Werte, bevor er das Alpha vormultipliziert.<br/> Wenn Sie diese Einstellung auf TRUE festlegen, werden die Werte durch den Effekt klammern. Wenn Sie diese Einstellung auf FALSE festlegen, bindet der Effekt die Farbwerte nicht, aber andere Effekte und die Ausgabeoberfläche können die Werte klammern, wenn sie nicht hoch genug präzise sind.<br/> Der Typ ist BOOL.<br/> Der Standardwert ist FALSE.<br/> |



 

## <a name="scale-modes"></a>Skalierungsmodi



| Enumeration                                              | Beschreibung                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Stichprobenentnahme für den nächstgelegenen einzelnen Punkt und Verwendung dieses Punkts. Dieser Modus verbraucht weniger Verarbeitungszeit, gibt jedoch das Image mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR                | Verwendet eine Stichprobe mit vier Punkt und eine lineare Interpolation. Dieser Modus gibt ein Bild mit höherer Qualität aus als der nächste Nachbarmodus.                                                                              |
| D2D1 \_ CONVOLVEMATRIX SCALE \_ \_ MODE \_ KUBISCH                 | Verwendet einen kubischen 16-Beispielkernel für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Image mit höherer Qualität aus.                                                                        |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus ist gut für das herunterskalieren um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ ANISOTROPIC           | Verwendet die anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu beproben.                                                                                                     |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE MODE HIGH QUALITY \_ \_ \_ \_ KUBISCH  | Verwendet einen kubischen Kernel mit hoher Qualität in variabler Größe, um ein Vorabskalieren des Images durchzuführen, wenn eine Downskalierung an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf D2D1 \_ CONVOLVEMATRIX \_ SCALE MODE LINEAR \_ \_ festgelegt.

 

## <a name="border-modes"></a>Rahmenmodi



| Name                     | Beschreibung                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BORDER \_ MODE \_ SOFT | Der Effekt padt das Eingabebild mit transparenten schwarzen Pixeln für Stichproben außerhalb der Eingabegrenze, wenn der Konvolutionskernel angewendet wird. Dadurch wird eine weiche Kante für das Bild erstellt, und während des Prozesses wird die Ausgabebitmap um die Größe des Kernels erweitert.<br/> |
| D2D1– \_ \_ RAHMENMODUS \_ FEST | Der Effekt erweitert das Eingabebild um eine Rahmentransformation vom Spiegeltyp für Stichproben außerhalb der Eingabegrenze. Die Größe der Ausgabebitmap entspricht der Größe der Eingabebitmap.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabe des Effekts hängt von der Größe des Konvolutionskernels, dem Kerneloffset, der Länge der Kerneleinheit und der Rahmenmoduseinstellung ab.

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

 

