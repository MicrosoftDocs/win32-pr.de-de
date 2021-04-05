---
title: Auswirkung der dpi-Kompensation
description: Verwenden Sie den dpi-Kompensierungs Effekt, um eine Eingabe Bitmap automatisch an den dpi-Kontext des Kontexts anzupassen. Dies ist nützlich für Situationen, in denen eine Bitmap auf einem anderen dpi-Wert als der Bildschirm erstellt oder geladen wird.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859319"
---
# <a name="dpi-compensation-effect"></a>Auswirkung der dpi-Kompensation

Verwenden Sie den dpi-Kompensierungs Effekt, um eine Eingabe Bitmap automatisch an den dpi-Kontext des Kontexts anzupassen. Dies ist nützlich für Situationen, in denen eine Bitmap auf einem anderen dpi-Wert als der Bildschirm erstellt oder geladen wird.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                       | BESCHREIBUNG                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> D2D1 \_ dpicompensation- \_ Prop- \_ Interpolations \_ Modus<br/> | Der Interpolations Modus, den der Effekt zum Skalieren des Bilds verwendet.<br/> Der Typ ist der D2D1 \_ dpicompensation- \_ Interpolations \_ Modus.<br/> Der Standardwert ist D2D1 \_ dpicompensation \_ Interpolations \_ Mode \_ linear.<br/>                  |
| Bordermode<br/> D2D1 \_ dpicompensation-Prop-Rahmen \_ \_ \_ Modus<br/>               | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter [Border Modes](https://www.bing.com/search?q=Border+modes) . <br/> Der Typ ist "D2D1 \_ Border \_ Mode".<br/> Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.<br/> |
| Inputdpi<br/> D2D1 \_ dpicompensation- \_ Prop- \_ Eingabe \_ dpi<br/>                   | Der dpi-Eintrag des Eingabe Bilds.<br/> Der Typ ist "float".<br/> Der Standardwert ist 96.0 f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Interpolations Modi



| Enumeration                                                       | Beschreibung                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ Nächster \_ Nachbar     | Verwendet den nächsten einzelnen Punkt und verwendet diesen. Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.                                                                           |
| D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ linear                | Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung. Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.                                           |
| D2D1 \_ dpicompensation \_ Interpolations \_ Modus ( \_ kubisch)                 | Verwendet einen 16-beispielkubischen Kernel für Interpolationen. In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.                                                                        |
| D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ \_ Multisample \_ linear | Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing. Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.                                              |
| D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ anisotrope           | Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.                                                                                                     |
| D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ High \_ Quality \_ kubisch  | Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist. Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe. |



 

> [!Note]  
> Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ dpicompensstion \_ Interpolations \_ Modus linear festgelegt \_ .

 

## <a name="border-modes"></a>Rahmen Modi



| Name                     | BESCHREIBUNG                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Border \_ Mode \_ Soft | Pixel außerhalb der Eingabe Grenzen werden vom [Spiegelungs Rahmen Effekt](border.md)generiert. <br/> |
| D2D1 \_ Rahmen \_ Modus \_ hart | Pixel außerhalb der Eingabe Grenzen sind transparent schwarz.<br/>                                    |



 

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

 

