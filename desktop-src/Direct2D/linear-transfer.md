---
title: Linearer Übertragungseffekt
description: Verwenden Sie den linearen Übertragungseffekt, um die Farbstärken eines Bilds mithilfe einer linearen Funktion zu ordnen, die aus einer Liste von Werten erstellt wurde, die Sie für jeden Kanal bereitstellen.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- Linearer Übertragungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcb2bb688d1e8ebf4b1b1ebfdd531d900755b46840bada2bade49d957ed0f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385294"
---
# <a name="linear-transfer-effect"></a>Linearer Übertragungseffekt

Verwenden Sie den linearen Übertragungseffekt, um die Farbstärken eines Bilds mithilfe einer linearen Funktion zu ordnen, die aus einer Liste von Werten erstellt wurde, die Sie für jeden Kanal bereitstellen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1LinearTransfer.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                          |
|-----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)      |
| Danach                                                           |
| ![das Bild nach der Transformation.](images/13-lineartransfer.png) |



 


```C++
ComPtr<ID2D1Effect> linearTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LinearTransfer, &linearTransferEffect);

linearTransferEffect->SetInput(0, bitmap);

linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_SLOPE, 2.5f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, 5.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(linearTransferEffect.Get());
m_d2dContext->EndDraw();
```



Die lineare Übertragungsfunktion wird basierend auf der Steigung und dem y-Intercept für jeden von Ihnen angegebenen Kanal erstellt. Die Ausgabepixelstärke C wird mit der Gleichung C' = mC + B berechnet, wobei m die Steigung der linearen Funktion und B der Y-Schnittpunkt der linearen Funktion ist.

Dieser Effekt funktioniert bei geraden und prämultipliierten Alphabildern. Der Effekt gibt prämultipliierte Alphabitmaps aus.

## <a name="effect-properties"></a>Effect-Eigenschaften

> [!Note]  
> Für alle Kanäle der linearen Übertragungseigenschaften:
>
> -   Das Y-Intercept ist nicht gebunden und unitlos.
> -   Die Steigung ist nicht gebunden und unitlos.

 



| Anzeigename und Indexenumeration                                                    | Typ und Standardwert           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ Y \_ INTERCEPT<br/>     | GLEITKOMMAZAHL<br/> 0,0f<br/> | Das Y-Intercept der linearen Funktion für den roten Kanal.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSinnen<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ SLOPE<br/>                 | GLEITKOMMAZAHL<br/> 1.0f<br/> | Die Steigung der linearen Funktion für den roten Kanal.                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ DISABLE<br/>             | BOOL<br/> FALSE<br/> | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet. Wenn Sie dies auf FALSE festlegen, wird die RedLinearTransfer-Funktion auf den roten Kanal angewendet.                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ Y \_ INTERCEPT<br/> | GLEITKOMMAZAHL<br/> 0,0f<br/> | Das Y-Intercept der linearen Funktion für den grünen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlop<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ SLOPE<br/>             | GLEITKOMMAZAHL<br/> 1.0f<br/> | Die Steigung der linearen Funktion für den grünen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ DISABLE<br/>         | BOOL<br/> FALSE<br/> | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet. Wenn Sie dies auf FALSE festlegen, wird die GreenLinearTransfer-Funktion auf den Grünen Kanal angewendet.                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ Y \_ INTERCEPT<br/>   | GLEITKOMMAZAHL<br/> 0,0f<br/> | Das Y-Intercept der linearen Funktion für den blauen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueS blues<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ SLOPE<br/>               | GLEITKOMMAZAHL<br/> 1.0f<br/> | Die Steigung der linearen Funktion für den blauen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>           | BOOL<br/> FALSE<br/> | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet. Wenn Sie dies auf FALSE festlegen, wird die BlueLinearTransfer-Funktion auf den blauen Kanal angewendet.                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ Y \_ INTERCEPT<br/> | GLEITKOMMAZAHL<br/> 0,0f<br/> | Das Y-Intercept der linearen Funktion für den Alphakanal.                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlphaSinnen<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ SLOPE<br/>             | GLEITKOMMAZAHL<br/> 0,0f<br/> | Die Steigung der linearen Funktion für den Alphakanal.                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/>         | BOOL<br/> FALSE<br/> | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den Alphakanal angewendet. Wenn Sie dies auf FALSE festlegen, wird die AlphaLinearTransfer-Funktion auf den Alphakanal angewendet.                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ CLAMP \_ OUTPUT<br/>           | BOOL<br/> FALSE<br/> | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 klammert, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt klammert die Werte vor der Prämultiplierung des Alpha-.<br/> Wenn Sie dies auf TRUE festlegen, klammert der Effekt die Werte. Wenn Sie dies auf FALSE festlegen, klammert der Effekt die Farbwerte nicht, aber andere Effekte und die Ausgabeoberfläche können die Werte klammern, wenn sie nicht hoch genug sind.<br/> |



 

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

 

