---
title: Tint-Effekt
description: Dieser Effekt zeigt das Quell Bild, indem das Quell Bild mit der angegebenen Farbe multipliziert wird. Sie verfügt über eine einzelne Eingabe.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949807"
---
# <a name="tint-effect"></a>Tint-Effekt

Dieser Effekt zeigt das Quell Bild, indem das Quell Bild mit der angegebenen Farbe multipliziert wird. Sie verfügt über eine einzelne Eingabe.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                    | Typ und Standardwert                              | BESCHREIBUNG                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| ColorD2D1 \_ tint- \_ Prop- \_ Farbe<br/>               | D2D1 \_ Vector \_ 4f (1.0 f, 1.0 f, 1.0 f, 1.0 f)<br/> | Farben aus dem Quell Bild werden mit diesem Wert multipliziert.       |
| ClampOutputD2D1 \_ tint- \_ Prop- \_ \_ Ausgabe<br/> | Boolfalse<br/>                                | Gibt an, ob die Ausgabewerte mit dem Bereich \[ 0, 1, fixiert werden \] . |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |



 ## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
