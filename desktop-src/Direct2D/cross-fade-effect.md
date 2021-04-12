---
title: Cross-Fade-Effekt
description: Dieser Effekt kombiniert zwei Bilder, indem gewichtete Pixel aus Eingabe Bildern hinzugefügt werden. Sie verfügt über zwei Eingaben, die als Ziel und Quelle bezeichnet werden.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517729"
---
# <a name="cross-fade-effect"></a>Cross-Fade-Effekt

Dieser Effekt kombiniert zwei Bilder, indem gewichtete Pixel aus Eingabe Bildern hinzugefügt werden. Sie verfügt über zwei Eingaben, die als Ziel und Quelle bezeichnet werden.

Die Cross-Fade-Formel lautet **Output = Weight \* Destination + (1-Weight) \* Source**.

Die CLSID für diesen Effekt ist CLSID \_ D2D1CrossFade.

## <a name="effect-properties"></a>Effekt Eigenschaften

| Anzeige Name und indexenumeration             | Typ und Standardwert | BESCHREIBUNG                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WeightD2D1 \_ Crossfade- \_ Prop- \_ Gewichtung<br/> | Float 0,5 f<br/>   | Gibt an, wie viel die Farbwerte des Quell Bilds im Vergleich zum Zielbild abgewogen werden. Der Minimalwert ist 0,0 f (verwendet ausschließlich das Zielbild, um die Ausgabe zu bestimmen), und der Höchstwert ist 1.0 f (verwendet ausschließlich das Quell Image zum Ermitteln der Ausgabe). |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
