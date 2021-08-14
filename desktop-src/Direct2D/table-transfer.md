---
title: Auswirkung der Tabellenübertragung
description: Verwenden Sie den Tabellenübertragungseffekt, um die Farbdichten eines Bilds mithilfe einer Übertragungsfunktion zuzuordnen, die aus der Interpolation einer liste von Ihnen angegebener Werte erstellt wurde.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- Auswirkung der Tabellenübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c533b55fd55c983b976633b766a6d8d273631d6111de9e2e36387f711f5f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665007"
---
# <a name="table-transfer-effect"></a>Auswirkung der Tabellenübertragung

Verwenden Sie den Tabellenübertragungseffekt, um die Farbdichten eines Bilds mithilfe einer Übertragungsfunktion zuzuordnen, die aus der Interpolation einer liste von Ihnen angegebener Werte erstellt wurde.

Die CLSID für diesen Effekt ist CLSID \_ D2D1TableTransfer.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Die Abbildung zeigt die Ein- und Ausgabe des Tabellenübertragungseffekts.



| Vorher                                                         |
|----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)     |
| Danach                                                          |
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



Die Übertragungsfunktion basiert auf einer Liste der Eingaben V=(V0,V1,V2,V3, V? , V<sub>N</sub>), wobei N die Anzahl der Elemente ist – 1.

Die Intensität des Eingabepixels wird als C dargestellt. Die Intensität des Ausgabepixels, C kann mit der Gleichung berechnet werden.

Wählen Sie für einen Wert C einen Wert k aus, sodass: k/N = C < (k+1)/N

Die Ausgabe C wird mithilfe der folgenden Gleichung berechnet: C' = V? + (C - k/N) \* N \* (V??? 1? - V?)

Dieser Effekt funktioniert bei geraden und prämultiplizierten Alphabildern. Der Effekt gibt prämultipliierte Alphabitmaps aus.

Das Diagramm der Tabellenübertragungsfunktion sieht wie folgt aus, wenn die Tabelleneigenschaft auf festgelegt `[0.0, 0.25, 1.0]` ist.

![Pixel-Intensitätsdiagramm für die Tabellenübertragungsfunktion.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Effect-Eigenschaften

> [!Note]  
> Die Werte aller Kanäle der Tabellenübertragungseigenschaften sind einheitenlos und weisen mindestens 0,0 und maximal 1,0 auf.

 



| Anzeigename und Indexenumeration                                           | Typ und Standardwert                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ RED \_ TABLE<br/>         | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den roten Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | Wenn Sie diese Einstellung auf TRUE festlegen, wendet der Effekt die Übertragungsfunktion nicht auf den roten Kanal an. Wenn Sie diese Einstellung auf FALSE festlegen, wird die RedTableTransfer-Funktion auf den Red-Kanal angewendet.                                                                                                                                                                                                                                                                             |
| GreenTable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ GREEN \_ TABLE<br/>     | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den grünen Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ GREEN \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Wenn Sie diese Einstellung auf TRUE festlegen, wendet der Effekt die Übertragungsfunktion nicht auf den grünen Kanal an. Wenn Sie diese Einstellung auf FALSE festlegen, wird die GreenTableTransfer-Funktion auf den grünen Kanal angewendet.                                                                                                                                                                                                                                                                       |
| BlueTable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ BLUE \_ TABLE<br/>       | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den blauen Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | Wenn Sie diese Einstellung auf TRUE festlegen, wendet der Effekt die Übertragungsfunktion nicht auf den blauen Kanal an. Wenn Sie diese Einstellung auf FALSE festlegen, wird die BlueTableTransfer-Funktion auf den Blue-Kanal angewendet.                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> D2D1 \_ TABLE \_ TRANSFER \_ PROP \_ ALPHA \_ TABLE<br/>   | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den Alphakanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Wenn Sie diese Einstellung auf TRUE festlegen, wendet der Effekt die Übertragungsfunktion nicht auf den Alphakanal an. Wenn Sie diese Einstellung auf FALSE festlegen, wird die AlphaTableTransfer-Funktion auf den Alphakanal angewendet.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> D2D1 \_ TABLETRANSFER \_ \_ PROP-KLAMMERAUSGABE \_<br/>   | BOOL<br/> FALSE<br/>             | Gibt an, ob der Effekt Farbwerte zwischen 0 und 1 zusammenbindet, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt klammert die Werte, bevor er das Alpha vormultipliziert.<br/> Wenn Sie diese Einstellung auf TRUE festlegen, werden die Werte durch den Effekt klammern. Wenn Sie diese Einstellung auf FALSE festlegen, bindet der Effekt die Farbwerte nicht, aber andere Effekte und die Ausgabeoberfläche können die Werte klammern, wenn sie nicht hoch genug präzise sind.<br/> |



 

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

 

