---
title: Gamma-Übertragungs Effekt
description: Verwenden Sie den Gamma-Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Gamma Funktion zuzuordnen, die mit einer Amplitude, einem Exponent und einem Offset erstellt wurde, die Sie für jeden Kanal bereitstellen.
ms.assetid: 0E0455CA-CFCA-4C4F-9DFA-1DB6A5205F6A
keywords:
- Gamma-Übertragungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b806ac8f59efe1b3fad3b61edc7f88f72b143f9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859086"
---
# <a name="gamma-transfer-effect"></a>Gamma-Übertragungs Effekt

Verwenden Sie den Gamma-Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Gamma Funktion zuzuordnen, die mit einer Amplitude, einem Exponent und einem Offset erstellt wurde, die Sie für jeden Kanal bereitstellen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1GammaTransfer. Um diesen Effekt zu verwenden, fügen Sie dxguid. lib den Linker-Abhängigkeiten hinzu.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                         |
|----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)     |
| Nach                                                          |
| ![das Bild nach der Transformation.](images/14-gammatransfer.png) |



 


```C++
ComPtr<ID2D1Effect> gammaTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GammaTransfer, &gammaTransferEffect);

gammaTransferEffect->SetInput(0, bitmap);

gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, 0.25f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gammaTransferEffect.Get());
m_d2dContext->EndDraw();
```



Dieser Effekt wendet eine Gamma Transfer-Funktion an, die auf der Gleichung basiert.

Die Eingabe Pixel Intensität wird als c und die Ausgabe Pixel Intensität als c ' dargestellt. C ' = Amplitude \* C<sup>Exponent</sup> + Offset

Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden. Der Effekt gibt prämultiplizierte Alpha Bitmaps aus.

## <a name="effect-properties"></a>Effekt Eigenschaften

> [!Note]  
> Für alle Kanäle der Gamma Transfer-Eigenschaften:
>
> -   Der Amplitude-Wert ist nicht gebunden und ist unitless.
> -   Der Exponent-Wert ist nicht gebunden und ist unitless.
> -   Der Offset Wert ist nicht gebunden und ist unitless.

 



| Anzeige Name und indexenumeration                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redamplitude<br/> D2D1 \_ gammatransfer \_ Stütze \_ Rote \_ Amplitude<br/>     | Die Amplitude der Gamma Übertragungsfunktion für den roten Kanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| Redexponent<br/> D2D1 \_ gammatransfer \_ Prop \_ roter \_ Exponent<br/>       | Der Exponent der Gamma Übertragungsfunktion für den roten Kanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| RedOffset<br/> D2D1 \_ gammatransfer- \_ Prop ( \_ roter \_ Offset)<br/>           | Der Offset der Gamma Übertragungsfunktion für den roten Kanal. Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| Reddeaktiviert<br/> D2D1 \_ gammatransfer \_ Stütze \_ Rote \_ Deaktivieren<br/>         | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet. Eine Funktion zur Identitäts Übertragung wird verwendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die Gamma Transfer-Funktion auf den roten Kanal angewendet. Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/>                                                                                                                                                                                                                                                |
| Greenamplitude<br/> D2D1 \_ gammatransfer- \_ Prop- \_ grüne \_ Amplitude<br/> | Die Amplitude der Gamma Übertragungsfunktion für den grünen Kanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| Greenexponent<br/> D2D1 \_ gammatransfer- \_ Prop- \_ grüner \_ Exponent<br/>   | Der Exponent der Gamma Übertragungsfunktion für den grünen Kanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| GreenOffset<br/> D2D1 \_ gammatransfer- \_ Prop- \_ grüner \_ Offset<br/>       | Der Offset der Gamma Übertragungsfunktion für den grünen Kanal. Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| Greendeaktivieren<br/> D2D1 \_ gammatransfer- \_ Prop- \_ grün \_ Deaktivieren<br/>     | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet. Eine Funktion zur Identitäts Übertragung wird verwendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die Gamma Transfer-Funktion auf den grünen Kanal angewendet. Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/>                                                                                                                                                                                                                                            |
| Blueamplitude<br/> D2D1 \_ gammatransfer- \_ Prop- \_ blaue \_ Amplitude<br/>   | Die Amplitude der Gamma Übertragungsfunktion für den blauen Kanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| Blueexponent<br/> D2D1 \_ gammatransfer- \_ Prop- \_ blauer \_ Exponent<br/>     | Der Exponent der Gamma Übertragungsfunktion für den blauen Kanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| BlueOffset<br/> D2D1 \_ gammatransfer- \_ Prop ( \_ blauer \_ Offset)<br/>         | Der Offset der Gamma Übertragungsfunktion für den blauen Kanal. Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| Bluedeaktiviert<br/> D2D1 \_ gammatransfer- \_ Prop- \_ blau \_ Deaktivieren<br/>       | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet. Eine Funktion zur Identitäts Übertragung wird verwendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die Gamma Transfer-Funktion auf den blauen Kanal angewendet. Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/>                                                                                                                                                                                                                                              |
| Alphaamplitude<br/> D2D1 \_ gammatransfer- \_ Prop \_ alpha \_ Amplitude<br/> | Die Amplitude der Gamma Übertragungsfunktion für den Alphakanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| Alphaexponent<br/> D2D1 \_ gammatransfer \_ Prop \_ alpha \_ Exponent<br/>   | Der Exponent der Gamma Übertragungsfunktion für den Alphakanal. Der Typ ist "float".<br/> Der Standardwert ist 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| AlphaOffset<br/> D2D1 \_ gammatransfer- \_ Prop- \_ alpha \_ Offset<br/>       | Der Offset der Gamma Übertragungsfunktion für den Alphakanal. Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| Alphadeaktivieren<br/> D2D1 \_ gammatransfer- \_ Prop- \_ alpha \_ Deaktivieren<br/>     | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den Alphakanal angewendet. Eine Funktion zur Identitäts Übertragung wird verwendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die Gamma Transfer-Funktion auf den Alphakanal angewendet. Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/>                                                                                                                                                                                                                                            |
| Klamme Ausgabe<br/> D2D1 \_ gammatransfer- \_ Prop- \_ Klemm \_ Ausgabe<br/>       | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.<br/> Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert. Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.<br/> Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/> |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.

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

 

