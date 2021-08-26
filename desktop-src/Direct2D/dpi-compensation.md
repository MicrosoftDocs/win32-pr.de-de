---
title: DPI-Kompensationseffekt
description: Verwenden Sie den DPI-Kompensationseffekt, um eine Eingabebitmap automatisch an den DPI des Kontexts anzupassen. Dies ist nützlich für Situationen, in denen eine Bitmap mit einem anderen DPI als dem Bildschirm erstellt oder geladen wird.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f1390825087cabb9ee1bec65f2708990757ff25f08e71140be5be0fc6ae11e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967114"
---
# <a name="dpi-compensation-effect"></a>DPI-Kompensationseffekt

Verwenden Sie den DPI-Kompensationseffekt, um eine Eingabebitmap automatisch an den DPI des Kontexts anzupassen. Dies ist nützlich für Situationen, in denen eine Bitmap mit einem anderen DPI als dem Bildschirm erstellt oder geladen wird.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                       | BESCHREIBUNG                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interpolationmode<br/> D2D1 \_ DPICOMPENSATION \_ PROP \_ INTERPOLATION \_ MODE<br/> | Der Interpolationsmodus, den der Effekt zum Skalieren des Bilds verwendet.<br/> Der Typ ist D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE.<br/> Der Standardwert ist D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE LINEAR \_ .<br/>                  |
| BorderMode<br/> D2D1 \_ DPICOMPENSATION \_ PROP \_ BORDER \_ MODE<br/>               | Der Modus, der zum Berechnen des Rahmens des Bilds verwendet wird( soft oder hard). Weitere Informationen finden Sie unter [Border modes (Rahmenmodi).](https://www.bing.com/search?q=Border+modes) <br/> Der Typ ist D2D1 \_ BORDER \_ MODE.<br/> Der Standardwert ist D2D1 \_ BORDER \_ MODE \_ SOFT.<br/> |
| InputDpi<br/> D2D1 \_ DPICOMPENSATION \_ PROP \_ INPUT \_ DPI<br/>                   | Der DPI des Eingabebilds.<br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 96,0f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Interpolationsmodi



| Enumeration                                                       | Beschreibung                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Probieren Sie den nächstgelegenen einzelnen Punkt aus, und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das Bild mit der niedrigsten Qualität aus.                                                                           |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ LINEAR                | Verwendet eine Vier-Punkt-Stichprobe und lineare Interpolation. Dieser Modus verwendet mehr Verarbeitungszeit als der nächste Nachbarmodus, gibt jedoch ein Bild höherer Qualität aus.                                           |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ KUBISCH                 | Verwendet einen kubischen Kernel mit 16 Beispielen für die Interpolation. Dieser Modus verwendet die meiste Verarbeitungszeit, gibt jedoch ein Bild höherer Qualität aus.                                                                        |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für ein gutes Edge-Antialiasing. Dieser Modus eignet sich gut für das Herunterskalierung um kleine Mengen auf Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ ANISOTROP           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap abzubilden.                                                                                                     |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE HIGH \_ \_ QUALITY \_ KUBISCH  | Verwendet einen kubischen Kernel variabler Größe, um das Bild vorab herunterzuskalieren, wenn die Transformationsmatrix eine Downskalierung umfasst. Verwendet dann den kubischen Interpolationsmodus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird standardmäßig D2D1 \_ DPICOMPENSTION \_ INTERPOLATION \_ MODE LINEAR \_ verwendet.

 

## <a name="border-modes"></a>Rahmenmodi



| Name                     | BESCHREIBUNG                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BORDER \_ MODE \_ SOFT | Pixel außerhalb der Eingabegrenzen werden vom [Spiegelrahmeneffekt](border.md)generiert. <br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | Pixel außerhalb der Eingabegrenzen sind transparent schwarz.<br/>                                    |



 

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

 

