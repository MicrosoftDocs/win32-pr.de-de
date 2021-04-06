---
title: Linearer Übertragungs Effekt
description: Verwenden Sie den linearen Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer linearen Funktion zuzuordnen, die aus einer Liste von Werten erstellt wird, die Sie für jeden Kanal bereitstellen.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- linearer Übertragungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfedbb79f057ee871ce23cc086034afc3e6cdda0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743945"
---
# <a name="linear-transfer-effect"></a>Linearer Übertragungs Effekt

Verwenden Sie den linearen Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer linearen Funktion zuzuordnen, die aus einer Liste von Werten erstellt wird, die Sie für jeden Kanal bereitstellen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1LinearTransfer.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                          |
|-----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)      |
| Nach                                                           |
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



Die lineare Übertragungsfunktion wird basierend auf der Steigung und der y-Abfang Funktion für jeden von Ihnen angegebenen Kanal erstellt. Die Ausgabe Pixel Intensität C wird mit der Gleichung berechnet: c ' = MC + B, wobei m die Steigung der linearen Funktion und B das Y-Abfangen der linearen Funktion ist.

Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden. Der Effekt gibt prämultiplizierte Alpha Bitmaps aus.

## <a name="effect-properties"></a>Effekt Eigenschaften

> [!Note]  
> Für alle Kanäle der linearen Übertragungseigenschaften:
>
> -   Das Y-abfangen ist nicht begrenzt und ist unitless.
> -   Die Steigung ist nicht begrenzt und ist unitless.

 



| Anzeige Name und indexenumeration                                                    | Typ und Standardwert           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redyintercept<br/> D2D1 \_ Lineartransfer \_ ( \_ roter \_ Y- \_ abfangen)<br/>     | GLEITKOMMAZAHL<br/> 0,0 f<br/> | Das Y-Abfangen der linearen Funktion für den roten Kanal.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Redslope<br/> D2D1 \_ Lineartransfer \_ ( \_ Rote \_ Neigung)<br/>                 | GLEITKOMMAZAHL<br/> 1.0 f<br/> | Die Steigung der linearen Funktion für den roten Kanal.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Reddeaktiviert<br/> D2D1 \_ Lineartransfer- \_ Stütze \_ rot \_ Deaktivieren<br/>             | BOOL<br/> false<br/> | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wendet der Effekt die redlineartransfer-Funktion auf den roten Kanal an.                                                                                                                                                                                                                                                                    |
| Greenyintercept<br/> D2D1 \_ Lineartransfer \_ Prop \_ grünes \_ Y- \_ abfangen<br/> | GLEITKOMMAZAHL<br/> 0,0 f<br/> | Das Y-Abfangen der linearen Funktion für den grünen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                 |
| Greenslope<br/> D2D1 \_ Lineartransfer \_ - \_ grüne \_ Steigung<br/>             | GLEITKOMMAZAHL<br/> 1.0 f<br/> | Die Steigung der linearen Funktion für den grünen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                       |
| Greendeaktivieren<br/> D2D1 \_ Lineartransfer- \_ Prop- \_ grün \_ Deaktivieren<br/>         | BOOL<br/> false<br/> | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die greenlineartransfer-Funktion auf den grünen Kanal angewendet.                                                                                                                                                                                                                                                                      |
| Blueyintercept<br/> D2D1 \_ Lineartransfer \_ Prop \_ blaues \_ Y- \_ abfangen<br/>   | GLEITKOMMAZAHL<br/> 0,0 f<br/> | Das Y-Abfangen der linearen Funktion für den blauen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                  |
| Blueslope<br/> D2D1 \_ Lineartransfer \_ Prop ( \_ blaue \_ Steigung)<br/>               | GLEITKOMMAZAHL<br/> 1.0 f<br/> | Die Steigung der linearen Funktion für den blauen Kanal.                                                                                                                                                                                                                                                                                                                                                                                                        |
| Bluedeaktiviert<br/> D2D1 \_ Lineartransfer- \_ Stütze \_ blau \_ Deaktivieren<br/>           | BOOL<br/> false<br/> | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die bluelineartransfer-Funktion auf den blauen Kanal angewendet.                                                                                                                                                                                                                                                                         |
| Alphayintercept<br/> D2D1 \_ Lineartransfer \_ Prop \_ alpha \_ Y \_ abfangen<br/> | GLEITKOMMAZAHL<br/> 0,0 f<br/> | Das Y-Abfangen der linearen Funktion für den Alpha Kanal.                                                                                                                                                                                                                                                                                                                                                                                                 |
| Alpha aslope<br/> D2D1 \_ Lineartransfer \_ Prop \_ alpha \_ Steigung<br/>             | GLEITKOMMAZAHL<br/> 0,0 f<br/> | Die Steigung der linearen Funktion für den Alpha Kanal.                                                                                                                                                                                                                                                                                                                                                                                                       |
| Alphadeaktivieren<br/> D2D1 \_ Lineartransfer \_ Prop \_ alpha \_ Deaktivieren<br/>         | BOOL<br/> false<br/> | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den Alpha Kanal angewendet. Wenn Sie diese Einstellung auf false festlegen, wird die alphalineartransfer-Funktion auf den Alpha Kanal angewendet.                                                                                                                                                                                                                                                                      |
| Klamme Ausgabe<br/> D2D1 \_ Lineartransfer \_ Prop \_ - \_ Ausgabe<br/>           | BOOL<br/> false<br/> | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.<br/> Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert. Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.<br/> |



 

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

 

