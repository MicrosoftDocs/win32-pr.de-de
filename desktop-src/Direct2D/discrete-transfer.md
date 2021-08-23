---
title: Diskreter Übertragungseffekt
description: Verwenden Sie den diskreten Übertragungseffekt, um die Farbstärken eines Bilds mithilfe einer Schrittübertragungsfunktion zu zuordnen, die aus einer Liste der von Ihnen angegebenen Werte erstellt wurde.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- Diskreter Übertragungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c977e6d2b03a3496bfa9be84209a32f57094c8514f6760746f9ec967c2ff8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431403"
---
# <a name="discrete-transfer-effect"></a>Diskreter Übertragungseffekt

Verwenden Sie den diskreten Übertragungseffekt, um die Farbstärken eines Bilds mithilfe einer Schrittübertragungsfunktion zu zuordnen, die aus einer Liste der von Ihnen angegebenen Werte erstellt wurde.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DiscreteTransfer.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Die Abbildung zeigt die Ein- und Ausgabe des diskreten Übertragungseffekts.



| Vorher                                                            |
|-------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)        |
| Danach                                                             |
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



Die Übertragungsfunktion basiert auf der Liste der Eingaben: V=(V0, V1, V2, V3, V? ,V<sub>N</sub>), wobei N die Anzahl der Elemente ist – 1.

Die Intensität des Eingabepixels wird als C dargestellt. Die Ausgabepixelstärke C wird mit der Gleichung berechnet:

Wählen Sie für einen Wert C einen Wert k aus, damit:

![Formel für den Prozess.](images/discrete-transfer1.png)

Die Ausgabe C kann mit der folgenden Gleichung berechnet werden: C' = V?

Dieser Effekt funktioniert bei geraden und prämultipliierten Alphabildern. Der Effekt gibt prämultipliierte Alphabitmaps aus.

So sieht das Diagramm der diskreten Übertragungsfunktion aus, wenn die Eingaben `[0.25, 0.5, 0.75, 1.0]` sind.

![Pixel-Intensitätsdiagramm für die diskrete Übertragungsfunktion.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Effect-Eigenschaften

> [!Note]  
> Die Werte aller Kanäle der diskreten Übertragungseigenschaften sind einheitslos und haben mindestens 0,0 und maximal 1,0.

 



| Anzeigename und Indexenumeration                                              | Typ und Standardwert                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ RED \_ TABLE<br/>         | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die zum Definieren der Übertragungsfunktion für den roten Kanal verwendet werden.                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den roten Kanal angewendet. Wenn Sie dies auf FALSE festlegen, wird die RedDiscreteTransfer-Funktion auf den roten Kanal angewendet.                                                                                                                                                                                                                                                                 |
| GreenTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ GREEN \_ TABLE<br/>     | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die die Übertragungsfunktion für den grünen Kanal definieren.                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ GREEN \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den grünen Kanal angewendet. Wenn Sie dies auf FALSE festlegen, wendet der Effekt die GreenDiscreteTransfer-Funktion auf den Green-Kanal an.                                                                                                                                                                                                                                                           |
| BlueTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ BLUE \_ TABLE<br/>       | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die die Übertragungsfunktion für den blauen Kanal definieren.                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den blauen Kanal angewendet. Wenn Sie dies auf FALSE festlegen, wendet der Effekt die BlueDiscreteTransfer-Funktion auf den blauen Kanal an.                                                                                                                                                                                                                                                              |
| AlphaTable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ ALPHA \_ TABLE<br/>     | schweben\[\]<br/> {0.0f, 1.0f}<br/> | Die Liste der Werte, die die Übertragungsfunktion für den Alphakanal definieren.                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Wenn Sie dies auf TRUE festlegen, wird die Übertragungsfunktion nicht auf den Alphakanal angewendet. Wenn Sie dies auf FALSE festlegen, wendet der Effekt die AlphaDiscreteTransfer-Funktion auf den Alphakanal an.                                                                                                                                                                                                                                                           |
| ClampOutput<br/> D2D1 \_ DISCRETETRANSFER \_ \_ PROP-KLAMMERAUSGABE \_<br/>   | BOOL<br/> FALSE<br/>             | Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 klammert, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt. Der Effekt klammert die Werte, bevor er das Alpha prämultipliert.<br/> Wenn Sie dies auf TRUE festlegen, klammert der Effekt die Werte. Wenn Sie dies auf FALSE festlegen, klammert der Effekt die Farbwerte nicht, aber andere Effekte und die Ausgabeoberfläche können die Werte klammern, wenn sie nicht hoch genug sind.<br/> |



 

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

 

