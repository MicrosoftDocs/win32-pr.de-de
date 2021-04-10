---
title: Sättigungseffekt
description: Verwenden Sie diesen Effekt, um die Sättigung eines Bilds zu ändern.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- sättigungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040482"
---
# <a name="saturation-effect"></a>Sättigungseffekt

Verwenden Sie diesen Effekt, um die Sättigung eines Bilds zu ändern. Der sättigungseffekt ist eine Spezialisierung des [Farbmatrix](color-matrix.md) Effekts.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Saturation.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das Beispiel zeigt die Eingabe-und Ausgabe Bilder des Sättigungs Effekts mit einer Sättigung von 0%.



| Vorher                                                      |
|-------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)  |
| Nach                                                       |
| ![das Bild nach der Transformation.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



Der Effekt berechnet eine Farbmatrix basierend auf dem Sättigungswert (*s* in der Gleichung hier), den Sie mit der Eigenschaft "D2D1 \_ Sättigung Prop-Sättigung" angeben \_ \_ . Die Matrix Gleichung wird hier dargestellt.

![Formel zum Berechnen einer Sättigungs Matrix.](images/saturation-formula.png)

Die erstellte Matrix hängt nur vom Sättigungswert ab. Sie können den [Farbmatrix](color-matrix.md) Effekt verwenden, wenn Sie eine bestimmte Matrix benötigen.

Diese Auswirkung verarbeitet und gibt vorab multiplizierte Alpha Bilder aus. Der Effekt funktioniert nicht bei geraden Alpha Bildern, es sei denn, Sie sind vollständig undurchsichtig.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                  | Typ und Standardwert           | BESCHREIBUNG                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sättigung<br/> Sättigung der D2D1 \_ Sättigung \_ \_<br/> | GLEITKOMMAZAHL<br/> 0,5 f<br/> | Die Sättigung des Bilds. Sie können die Sättigung auf einen Wert zwischen 0 und 1 festlegen. Wenn Sie den Wert auf 1 festlegen, ist das Ausgabe Bild vollständig ausgelastet. Wenn Sie den Wert auf 0 festlegen, ist das Ausgabe Bild Monochrome. Der Sättigungswert ist unitless. |



 

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

 

