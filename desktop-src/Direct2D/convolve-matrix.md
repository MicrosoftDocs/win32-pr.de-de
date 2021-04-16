---
title: Faltungsmatrixeffekt
description: Verwenden Sie den kovolve Matrix Effekt, um einen beliebigen 2D-Kernel auf ein Bild anzuwenden. Sie können diesen Effekt verwenden, um Kanten zu verwischen, Kanten zu erkennen oder ein Bild zu schärfen.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- konstanter Matrix Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27951f5b9145dc46188e6b3112892d1a61856236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104564025"
---
# <a name="convolve-matrix-effect"></a>Faltungsmatrixeffekt

Verwenden Sie den kovolve Matrix Effekt, um einen beliebigen 2D-Kernel auf ein Bild anzuwenden. Sie können diesen Effekt verwenden, um Kanten zu verwischen, Kanten zu erkennen oder ein Bild zu schärfen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1ConvolveMatrix.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Skalierungs Modi](#scale-modes)
-   [Rahmen Modi](#border-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das folgende Beispiel zeigt die Eingabe und die Ausgabe des Effekts der Matrix mit einem 3 x 3-Kernel.



| Vorher                                                         |
|----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)     |
| Nach                                                          |
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



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kernelunitlength<br/> D2D1 \_ \_ \_ -Länge der Kernel \_ Einheits \_ Länge<br/> | Die Größe einer Einheit im Kernel. Die Einheiten befinden sich in (Dips/Kernel Unit), wobei eine Kernel Einheit die Größe des Elements im zuordnungskernel ist. Der Wert 1 (DIP/Kernel Unit) entspricht einem Pixel in einem Bild bei 96 dpi.<br/> Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                   |
| Skalemode<br/> D2D1-konstanter \_ \_ \_ Skalierungs \_ Modus<br/>                 | Der Interpolations Modus, mit dem das Bild auf die entsprechende Kernel Einheitslänge skaliert wird. Es gibt sechs Skalierungs Modi mit hoher Qualität und Geschwindigkeit.<br/> Der Typ ist der D2D1-Modus für die \_ konvolvematrix- \_ Skalierung \_ .<br/> Der Standardwert ist "D2D1" \_ \_ \_ \_ .<br/>                                                                                                                                                                                                                     |
| Kernelsizex<br/> D2D1 \_ \_ \_ -Kernel \_ Größe \_ X<br/>           | Die Breite der Kernel Matrix. Die Einheiten werden in Kernel Einheiten angegeben. Der Typ ist "UInt32".<br/> Der Standardwert ist 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| Kernelsizey<br/> D2D1 \_ \_ \_ -kernelgröße für die-Kernel \_ Größe \_ Y<br/>           | Die Höhe der Kernel Matrix. Die Einheiten werden in Kernel Einheiten angegeben. Der Typ ist "UInt32".<br/> Der Standardwert ist 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| Kernelmatrix<br/> D2D1 \_ \_ \_ - \_ kernelmatrix<br/>           | Die Kernel Matrix, die auf das Bild angewendet werden soll. Die Kernel Elemente sind nicht gebunden und werden als Gleit Komma Zahlen angegeben.<br/> Der erste Satz von *kernelsizex* -Zahlen im float \[ \] -Wert entspricht der ersten Zeile im Kernel. Der zweite Satz von *kernelsizex* -Zahlen entspricht der zweiten Zeile usw. bis zu *kernelsizey* -Zeilen.<br/> Der Typ ist "float" \[ \] .<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f, 0,0 f, 1.0 f, 0,0 f, 0,0 f, 0,0 f, 0,0 f}.<br/>                                                       |
| Divisor<br/> D2D1-Konstante \_ \_ dividivematrix \_<br/>                       | Die Kernel Matrix wird auf ein Pixel angewendet, und dann wird das Ergebnis durch diesen Wert dividiert. <br/> 0 verhält sich als Wert von float Epsilon.<br/> Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                           |
| Verzerrung (Bias)<br/> D2D1 \_ -Konstante \_ \_<br/>                             | Der Effekt wendet die Kernel Matrix und den Divisor an, und dann wird der Bias dem Ergebnis hinzugefügt. Die Verschiebung ist unbegrenzt und unischlos. Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                              |
| Kerneloffset<br/> D2D1 \_ \_ \_ -Kernel \_ Offset für "Konstante Konstante"<br/>           | Verschiebt den Konfigurations-Kernel von einer zentrierten Position auf dem Ausgabe Pixel in eine von Ihnen angegebene Position nach links/rechts und nach oben/unten. Der Offset wird in Kernel Einheiten definiert.<br/> Bei einigen Offsets und Kernel Größen landen die Beispiele für die Zusammenführung von Kernels nicht in einem Pixel Image Center. Die Pixelwerte für das Kernel Beispiel werden durch bilineare Interpolationen berechnet.<br/> Der Typ ist "D2D1 \_ Vector \_ 2F".<br/> Der Standardwert ist {0,0 f, 0,0 f}.<br/>                                                          |
| Preservealpha<br/> D2D1-Konstante " \_ konvolvematrix \_ prop" \_ beibehalten \_<br/>         | Gibt an, ob der Konfigurations-Kernel auf den Alphakanal oder nur auf die farbchannels angewendet wird.<br/> Wenn Sie diese Einstellung auf " **true** " festlegen, wird der-Konfigurations-Kernel nur auf die Farbkanäle angewendet.<br/> Wenn Sie diese Einstellung auf " **false** " festlegen, wird der zulassungkernel auf alle Kanäle angewendet.<br/> Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/>                                                                                                                                               |
| Bordermode<br/> D2D1-Rahmen \_ \_ \_ \_ Modus<br/>               | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter [Border Modes](https://www.bing.com/search?q=Border+modes) .<br/> Der Typ ist "D2D1 \_ Border \_ Mode".<br/> Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.<br/>                                                                                                                                                                                                                                                                                     |
| Klamme Ausgabe<br/> D2D1 config- \_ \_ \_ \_ Ausgabe<br/>             | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.<br/> Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert. Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.<br/> Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/> |



 

## <a name="scale-modes"></a>Skalierungs Modi



| Enumeration                                              | Beschreibung                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1- \_ \_ Skalierungs \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1- \_ \_ Skalierungs \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. In diesem Modus wird ein Image mit höherer Qualität als nächster Nachbar Modus ausgegeben.                                                                              |
| D2D1- \_ \_ Skalierungs \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1- \_ \_ Skalierungs \_ Modus ( \_ \_ Multisample \_ linear) | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ convolvematrix \_ Scale \_ Mode \_ anisotrov           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1- \_ \_ Skalierungs \_ Modus mit \_ hoher \_ Qualität \_  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1-Modus für die Konstante \_ \_ Skalierungs \_ Modus linear festgelegt \_ .

 

## <a name="border-modes"></a>Rahmen Modi



| Name                     | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Border \_ Mode \_ Soft | Der Effekt füllt das Eingabebild mit transparenten schwarzen Pixeln für Stichproben außerhalb der Eingabe Grenzen auf, wenn es den zuordnerkerntyp anwendet. Dadurch wird ein weicher Edge für das Bild erstellt, und im Prozess wird die Ausgabe Bitmap um die Größe des Kernels erweitert.<br/> |
| D2D1 \_ Rahmen \_ Modus \_ hart | Die Auswirkung erweitert das Eingabebild durch eine Spiegelungs Typen-Rahmen Transformation für Beispiele außerhalb der Eingabe Grenzen. Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe des Effekts hängt von der Größe des zuordnungskernels, dem Kernel Offset, der Länge der Kernel Einheit und der rahmenmoduseinstellung ab.

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

 

