---
title: Diskreter Übertragungs Effekt
description: Verwenden Sie den diskreten Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Schritt Übertragungsfunktion zuzuordnen, die aus einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- diskreter Übertragungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104567575"
---
# <a name="discrete-transfer-effect"></a>Diskreter Übertragungs Effekt

Verwenden Sie den diskreten Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Schritt Übertragungsfunktion zuzuordnen, die aus einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DiscreteTransfer.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das Bild hier zeigt die Eingabe und die Ausgabe des diskreten Übertragungs Effekts.



| Vorher                                                            |
|-------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)        |
| Nach                                                             |
| ![das Bild nach der Transformation.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



Die Übertragungsfunktion basiert auf der Liste der Eingaben: V = (v0, v1, v2, v3, V? , V<sub>N</sub>), wobei N die Anzahl der Elemente-1 ist.

Die Eingabe Pixel Intensität wird als C dargestellt. Die Ausgabe Pixel Intensität, C wird mit der Gleichung berechnet:

Wählen Sie für einen Wert C den Wert k aus, um Folgendes zu erhalten:

![die Formel für den Prozess.](images/discrete-transfer1.png)

Die Ausgabe c kann mit der Gleichung berechnet werden: c ' = V?

Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden. Der Effekt gibt prämultiplizierte Alpha Bitmaps aus.

So sieht das Diagramm der diskreten Übertragungsfunktion aus, wenn die Eingaben sind `[0.25, 0.5, 0.75, 1.0]` .

![Pixel Intensität des Diagramms für die diskrete Übertragungsfunktion.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Effekt Eigenschaften

> [!Note]  
> Die Werte aller Kanäle der diskreten Übertragungseigenschaften sind unitless und haben mindestens 0,0 und einen maximalen Wert von 1,0.

 



| Anzeige Name und indexenumeration                                              | Typ und Standardwert                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redtable<br/> D2D1 \_ diskretetransfer \_ ( \_ Rote \_ Tabelle)<br/>         | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den roten Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                 |
| Reddeaktiviert<br/> D2D1 \_ diskretetransfer-unter \_ Stützung \_ rot \_ Deaktivieren<br/>     | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wendet der Effekt die reddiskretetransfer-Funktion auf den roten Kanal an.                                                                                                                                                                                                                                                                 |
| Abbrechbar<br/> D2D1 \_ diskretetransfer-unter \_ Stützung für \_ grüne \_ Tabelle<br/>     | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die die Übertragungsfunktion für den grünen Kanal definieren.                                                                                                                                                                                                                                                                                                                                                                                  |
| Greendeaktivieren<br/> D2D1 \_ diskretetransfer- \_ Prop \_ grün \_ Deaktivieren<br/> | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wendet der Effekt die greendiskretetransfer-Funktion auf den grünen Kanal an.                                                                                                                                                                                                                                                           |
| Bluetable<br/> D2D1 \_ diskretetransfer- \_ Prop ( \_ blaue \_ Tabelle)<br/>       | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die die Übertragungsfunktion für den blauen Kanal definieren.                                                                                                                                                                                                                                                                                                                                                                                   |
| Bluedeaktiviert<br/> D2D1 \_ diskretetransfer- \_ Prop \_ blau \_ Deaktivieren<br/>   | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die bluediskretetransfer-Funktion auf den blauen Kanal angewendet.                                                                                                                                                                                                                                                              |
| Alpha kompatibel<br/> D2D1 \_ diskretetransfer- \_ Prop- \_ alpha \_ Tabelle<br/>     | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die die Übertragungsfunktion für den Alpha Kanal definieren.                                                                                                                                                                                                                                                                                                                                                                                  |
| Alphadeaktivieren<br/> D2D1 \_ diskretetransfer- \_ Prop- \_ alpha \_ Deaktivieren<br/> | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den Alpha Kanal angewendet. Wenn Sie diese Einstellung auf false festlegen, wird die alphadiskretetransfer-Funktion auf den Alpha Kanal angewendet.                                                                                                                                                                                                                                                           |
| Klamme Ausgabe<br/> D2D1 \_ diskretetransfer- \_ Prop- \_ Klemm \_ Ausgabe<br/>   | BOOL<br/> false<br/>             | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.<br/> Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert. Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.<br/> |



 

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

 

