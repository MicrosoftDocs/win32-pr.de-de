---
title: YCbCr-Effekt
description: Konvertiert planare-und Chroma-Subsampling-JPEG YCbCr-Daten in RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c581effbadecc19c39161d2a2ec4af051d4195d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040825"
---
# <a name="ycbcr-effect"></a>YCbCr-Effekt

Konvertiert planare-und Chroma-untergeordnete JPEG Yc<sub>b</sub>C<sub>r</sub> -Daten in RGB. Dieser Effekt setzt voraus, dass die Yc<sub>b</sub>C<sub>r</sub> -Daten gemäß dem JPEG-Standard formatiert sind. Daten für die Eingaben können von iwicplanarbitmapsourcetransform abgerufen werden. Der JC<sub>b</sub>c<sub>r</sub> -Effekt erfordert zwei Eingaben: der erste muss eine Bitmap im DXGI- \_ Format \_ R8 sein, die "Luma"-Daten enthält, und die zweite muss ein DXGI- \_ Format sein \_ R8G8 Bitmap mit unter Stichproben von Chroma-Daten. Weitere Informationen zur Verwendung dieses Effekts finden Sie [unter JPEG YCbCr-Unterstützung](/windows/desktop/wic/jpeg-ycbcr-support).

Die CLSID für diesen Effekt ist CLSID \_ D2D1YCbCr.

-   [Effekt Eigenschaften](#effect-properties)
-   [Unter Stichproben Modi](#subsampling-modes)
-   [Interpolations Modi](#interpolation-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chromasubsampling<br/> D2D1 \_ YCbCr \_ Chroma- \_ Unterstichprobe<br/>    | Gibt die Chroma-Unterstichprobe des Eingabe-Chroma-Bilds an. <br/> Der Typ ist D2D1 \_ YCbCr \_ Chroma \_ Subsampling.<br/> Der Standardwert ist D2D1 \_ YCbCr \_ Chroma \_ Subsampling \_ Auto.<br/>                                                                                                |
| TransformMatrix <br/> D2D1 \_ YCbCr- \_ Prop- \_ Transformations \_ Matrix<br/> | Eine [3 x 2-Matrix](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) , die die Achsen ausgerichtete affine Transformation des Bilds angibt. Zu den Achsen ausgerichteten Transformationen zählen Skalierungen, Flips und 90-Grad-Drehungen. <br/> Der Typ ist "D2D1 \_ Matrix \_ 3x2 \_ F".<br/> Der Standardwert ist Matrix3x2F:: Identity ().<br/> |
| InterpolationMode<br/> D2D1 \_ YCbCr- \_ Interpolations \_ Modus<br/>    | Der Interpolations Modus.<br/> Der Typ ist der D2D1 \_ YCbCr- \_ Interpolations \_ Modus.<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Unter Stichproben Modi



| Enumeration                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCbCr \_ Chroma \_ unter Stichproben \_ automatisch<br/> | Dieser Modus versucht, die Chroma-Unterstichprobe aus den Begrenzungen der Eingabe Bilder abzuleiten. Wenn diese Option ausgewählt ist, wird die kleinere Ebene auf die Größe der größeren Ebene hochskalieren, und dieses Ausgabe Rechteck ist die Schnittmenge der beiden Ebenen. Wenn Sie diesen Modus verwenden, sollten Sie sorgfältig vorgehen, wenn Sie Auswirkungen auf die Eingabe Ebenen anwenden, die die Bild Begrenzungen ändern, wie z. b. die Rahmen Transformation, damit das gewünschte Größenverhältnis zwischen den Ebenen beibehalten wird. <br/> |
| D2D1 \_ YCbCr \_ Chroma- \_ Unterstichprobe \_ 420<br/>  | Die Chroma-Ebene wird horizontal von Subsampling und vertikal von untersucht. Wenn diese Option ausgewählt ist, wird die Chroma-Ebene horizontal und vertikal um 2X erhöht, und dieses Ausgabe Rechteck ist die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                          |
| D2D1 \_ YCbCr \_ Chroma- \_ Unterstichprobe \_ 422<br/>  | Die Chroma-Ebene wird horizontal von untersucht. Wenn diese Option ausgewählt ist, wird die Chroma-Ebene horizontal um 2X hochskalierte, und dieses Ausgabe Rechteck ist die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                                                                        |
| D2D1 \_ YCbCr \_ Chroma- \_ Unterstichprobe \_ 444<br/>  | Die Chroma-Ebene wird nicht untersucht. Wenn diese Option aktiviert ist, ist das Ausgabe Rechteck des Effekts die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                                                                                                                                            |
| D2D1 \_ YCbCr \_ Chroma- \_ Unterstichprobe \_ 440<br/>  | Die Chroma-Ebene wird vertikal von Subsampling. Wenn diese Option ausgewählt ist, wird die Chroma-Ebene vertikal um 2X erhöht, und dieses Ausgabe Rechteck ist die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Interpolations Modi



| Enumeration                                             | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCbCr \_ Interpolations \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ YCbCr \_ Interpolations \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.                                           |
| D2D1 \_ YCbCr \_ Interpolations \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ YCbCr \_ Interpolations \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ YCbCr \_ Interpolations \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ YCbCr \_ Interpolations \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap hängt von der Transformationsmatrix ab, die auf das Bild angewendet wird.

Der Effekt führt den Transformations Vorgang aus und wendet dann ein Begrenzungs Rahmen um das Ergebnis an. Die Ausgabe Bitmap ist die Größe des umgebenden Felds.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[ \| Windows Store-Apps für Desktop-Apps Windows 8.1\]            |
| Unterstützte Mindestversion (Server) | Windows Server 2012 R2 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 1. h                                              |
| Bibliothek                  | d2d1. lib, dxguid. lib                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[JPEG YCbCr-Unterstützung](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**Iwicplanarbitmapsourcetransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

