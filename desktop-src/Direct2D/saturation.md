---
title: Sättigungseffekt
description: Verwenden Sie diesen Effekt, um die Sättigung eines Bilds zu ändern.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- Sättigungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5f9a4bff56ed47a0ca182dab855899d98022252c6f20c250aef693451df4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665037"
---
# <a name="saturation-effect"></a>Sättigungseffekt

Verwenden Sie diesen Effekt, um die Sättigung eines Bilds zu ändern. Der Sättigungseffekt ist eine Spezialisierung des [Farbmatrixeffekts.](color-matrix.md)

Die CLSID für diesen Effekt ist CLSID \_ D2D1Saturation.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das hier gezeigte Beispiel zeigt die Ein- und Ausgabebilder des Sättigungseffekts mit einer Sättigung von 0 %.



| Vorher                                                      |
|-------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)  |
| Danach                                                       |
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



Der Effekt berechnet eine Farbmatrix basierend auf dem Sättigungswert (*s* in der Gleichung hier), den Sie mit der D2D1-Eigenschaft \_ SÄTTIGUNG \_ PROP SATURATION \_ angeben. Die Matrixgleichung wird hier gezeigt.

![Formel zum Berechnen einer Sättigungsmatrix.](images/saturation-formula.png)

Die erstellte Matrix hängt nur vom Sättigungswert ab. Sie können den [Farbmatrixeffekt verwenden,](color-matrix.md) wenn Sie eine bestimmte Matrix benötigen.

Dieser Effekt verwendet und gibt prämultipliierte Alphabilder aus. Der Effekt funktioniert nur bei geraden Alphabildern, wenn sie vollständig deckend sind.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                  | Typ und Standardwert           | Beschreibung                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sättigung<br/> D2D1- \_ SÄTTIGUNG \_ \_ PROP-SÄTTIGUNG<br/> | GLEITKOMMAZAHL<br/> 0,5f<br/> | Die Sättigung des Bilds. Sie können die Sättigung auf einen Wert zwischen 0 und 1 festlegen. Wenn Sie dies auf 1 festlegen, ist das Ausgabebild vollständig ausgesättigt. Wenn Sie dies auf 0 festlegen, ist das Ausgabebild monofarbig. Der Sättigungswert ist unitlos. |



 

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

 

