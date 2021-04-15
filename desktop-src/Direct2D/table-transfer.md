---
title: Tabellen Übertragungs Effekt
description: Verwenden Sie den Tabellen Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Übertragungsfunktion zuzuordnen, die aus der Interpolation einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- Tabellen Übertragungs Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476752"
---
# <a name="table-transfer-effect"></a>Tabellen Übertragungs Effekt

Verwenden Sie den Tabellen Übertragungs Effekt, um die Farb Intensitäten eines Bilds mithilfe einer Übertragungsfunktion zuzuordnen, die aus der Interpolation einer Liste mit von Ihnen bereitgestellten Werten erstellt wurde.

Die CLSID für diesen Effekt ist CLSID \_ D2D1TableTransfer.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das Bild hier zeigt die Eingabe und die Ausgabe des Tabellen Übertragungs Effekts.



| Vorher                                                         |
|----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)     |
| Nach                                                          |
| ![das Bild nach der Transformation.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



Die Übertragungsfunktion basiert auf einer Liste von Eingaben V = (v0, v1, v2, v3, V? , V<sub>N</sub>), wobei N die Anzahl der Elemente-1 ist.

Die Eingabe Pixel Intensität wird als C dargestellt. Die Ausgabe Pixel Intensität C kann mit der Gleichung berechnet werden.

Wählen Sie für einen Wert C einen Wert k aus, z. b.: k/N = C < (k + 1)/N

Die Ausgabe c wird mithilfe der folgenden Gleichung berechnet: c ' = V? + (C-k/n) \* N \* (V??? 1? -V?)

Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden. Der Effekt gibt prämultiplizierte Alpha Bitmaps aus.

So sieht das Diagramm der Tabellen Übertragungsfunktion aus, wenn die Table-Eigenschaft auf festgelegt ist `[0.0, 0.25, 1.0]` .

![Pixel Intensität des Diagramms für die Tabellen Übertragungsfunktion.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Effekt Eigenschaften

> [!Note]  
> Die Werte aller Kanäle der Tabellen Übertragungseigenschaften sind unitless und haben mindestens 0,0 und einen maximalen Wert von 1,0.

 



| Anzeige Name und indexenumeration                                           | Typ und Standardwert                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redtable<br/> D2D1 \_ tabletransfer \_ Prop ( \_ Rote \_ Tabelle)<br/>         | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den roten Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                  |
| Reddeaktiviert<br/> D2D1 \_ tabletransfer \_ Prop \_ rot \_ Deaktivieren<br/>     | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die redtabletransfer-Funktion auf den roten Kanal angewendet.                                                                                                                                                                                                                                                                             |
| Abbrechbar<br/> D2D1 \_ tabletransfer \_ Prop ( \_ grüne \_ Tabelle)<br/>     | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den grünen Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                |
| Greendeaktivieren<br/> D2D1 \_ tabletransfer \_ Prop \_ grün \_ Deaktivieren<br/> | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die greentabletransfer-Funktion auf den grünen Kanal angewendet.                                                                                                                                                                                                                                                                       |
| Bluetable<br/> D2D1 \_ tabletransfer \_ Prop ( \_ blaue \_ Tabelle)<br/>       | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den blauen Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                 |
| Bluedeaktiviert<br/> D2D1 \_ tabletransfer \_ Prop \_ blau \_ Deaktivieren<br/>   | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die bluetabletransfer-Funktion auf den blauen Kanal angewendet.                                                                                                                                                                                                                                                                          |
| Alpha kompatibel<br/> D2D1 \_ Table \_ Transfer \_ Prop- \_ alpha \_ Tabelle<br/>   | Hafen\[\]<br/> {0,0 f, 1.0 f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den Alpha Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                |
| Alphadeaktivieren<br/> D2D1 \_ tabletransfer \_ Prop \_ alpha \_ Deaktivieren<br/> | BOOL<br/> false<br/>             | Wenn Sie diese Einstellung auf "true" festlegen, wird die Übertragungsfunktion nicht auf den Alpha Kanal angewendet. Wenn Sie diese Einstellung auf "false" festlegen, wird die Alpha atabletransfer-Funktion auf den Alpha Kanal angewendet.                                                                                                                                                                                                                                                                       |
| Klamme Ausgabe<br/> D2D1 \_ tabletransfer \_ Prop \_ - \_ Ausgabe<br/>   | BOOL<br/> false<br/>             | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.<br/> Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert. Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.<br/> |



 

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

 

