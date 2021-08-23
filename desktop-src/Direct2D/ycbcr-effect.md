---
title: YCbCr Effect
description: Konvertiert planare und untersampelte JPEG-YCbCr-Daten in RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5302300cc539571fabb1c3d786686ffc514636133391e706fc5963002656764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636090"
---
# <a name="ycbcr-effect"></a>YCbCr Effect

Konvertiert planare und untersampelte JPEG YC<sub>b</sub>C<sub>r-Daten</sub> in RGB. Bei diesem Effekt wird davon ausgegangen, dass die YC<sub>b</sub>C<sub>r-Daten</sub> gemäß dem JPEG-Standard formatiert sind. Daten für die Eingaben können von IWICPlanarBitmapSourceTransform abgerufen werden. Der YC<sub>b</sub>C<sub>r-Effekt</sub> erfordert zwei Eingaben: Die erste muss eine DXGI \_ FORMAT \_ R8-Bitmap mit Lumadaten und die zweite eine DXGI \_ FORMAT \_ R8G8-Bitmap sein, die subsampled-Daten enthält. Weitere Informationen zur Verwendung dieses Effekts finden Sie unter [JPEG YCbCr Support](/windows/desktop/wic/jpeg-ycbcr-support).

Die CLSID für diesen Effekt ist CLSID \_ D2D1YCbCr.

-   [Effect-Eigenschaften](#effect-properties)
-   [Untersamplingmodi](#subsampling-modes)
-   [Interpolationsmodi](#interpolation-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                          | Beschreibung                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UmschlägeSubsampling<br/> D2D1 \_ YCBCR– \_ \_ ABONNEMENTSAMPLING<br/>    | Gibt die Untersampling des Eingabebilds an. <br/> Der Typ ist "D2D1 \_ YCBCR \_ NF \_ SUBSAMPLING".<br/> Der Standardwert ist D2D1 \_ YCBCR \_ NF \_ SUBSAMPLING \_ AUTO.<br/>                                                                                                |
| TransformMatrix <br/> D2D1 \_ YCBCR \_ PROP \_ TRANSFORM \_ MATRIX<br/> | Eine [3x2-Matrix,](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) die die an der Achse ausgerichtete affine Transformation des Bilds angibt. Zu den achsenbündig ausgerichteten Transformationen gehören Skalierung, Flips und Drehungen um 90 Grad. <br/> Der Typ ist D2D1 \_ MATRIX \_ 3X2 \_ F.<br/> Der Standardwert ist Matrix3x2F::Identity().<br/> |
| Interpolationmode<br/> D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE<br/>    | Der Interpolationsmodus.<br/> Der Typ ist D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE.<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Untersamplingmodi



| Enumeration                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCBCR– \_ \_ SUBSAMPLING \_ AUTO<br/> | In diesem Modus wird versucht, die Subsampling der -Subsampling aus den Grenzen der Eingabebilder abzuleitung. Wenn diese Option ausgewählt ist, wird die kleinere Ebene auf die Größe der größeren Ebene hochsampelt, und das Ausgaberechteck dieses Effekts ist die Schnittmenge der beiden Ebenen. Wenn Sie diesen Modus verwenden, sollten Sie beim Anwenden von Effekten auf die Eingabeebenen, die die Bildgrenzen ändern, wie z. B. die Rahmentransformation, sorgfältig vorgehen, damit das gewünschte Größenverhältnis zwischen den Ebenen beibehalten wird. <br/> |
| D2D1 \_ YCBCR– \_ \_ ABONNEMENTSAMPLING \_ 420<br/>  | Die Flächenebene wird horizontal von und vertikal durch subsampled subsampled von subsampled. Wenn diese Option ausgewählt ist, wird die Knotenebene horizontal und vertikal um 2x hochsampgt, und das Ausgaberechteck dieses Effekts ist die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                          |
| D2D1 \_ YCBCR– \_ \_ ABONNEMENTSAMPLING \_ 422<br/>  | Die Schnittebene wird horizontal von subsampled. Wenn diese Option ausgewählt ist, wird die Knotenebene horizontal um das Zweifache hochsampgt, und das Ausgaberechteck dieses Effekts ist die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                                                                        |
| D2D1 \_ YCBCR– \_ \_ ABONNEMENTSAMPLING \_ 444<br/>  | Die Flugzeugebene wird nicht untersampelt. Wenn diese Option ausgewählt ist, ist das Ausgaberechteck dieses Effekts die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                                                                                                                                            |
| D2D1 \_ YCBCR– \_ \_ ABONNEMENTSAMPLING \_ 440<br/>  | Die Flächenebene wird vertikal von subsampled. Wenn diese Option ausgewählt ist, wird die Knotenebene vertikal um das Zweifache hochsampgt, und das Ausgaberechteck dieses Effekts ist die Schnittmenge der beiden Ebenen.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Interpolationsmodi



| Enumeration                                             | Beschreibung                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus verwendet mehr Verarbeitungszeit als der nächste Nachbarmodus, gibt jedoch ein Bild höherer Qualität aus.                                           |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                                                                        |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus eignet sich gut für das Herunterskalierung um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ ANISOTROP           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap abzubilden.                                                                                                     |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE HIGH \_ \_ QUALITY \_ KUBISCH  | Verwendet einen kubischen Kernel variabler Größe, um das Bild vorab herunterzuskalieren, wenn die Transformationsmatrix eine Downskalierung umfasst. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabebitmap hängt von der Transformationsmatrix ab, die auf das Bild angewendet wird.

Der Effekt führt den Transformationsvorgang aus und wendet dann einen Begrenzungsfeld um das Ergebnis an. Die Ausgabebitmap ist die Größe des umgebenden Felds.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 8.1 Desktop-Apps \| Windows Store Apps\]            |
| Unterstützte Mindestversion (Server) | Windows Server 2012 \[R2-Desktop-Apps \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 1.h                                              |
| Bibliothek                  | d2d1.lib, dxguid.lib                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[JPEG-YCbCr-Unterstützung](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

