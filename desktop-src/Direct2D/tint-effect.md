---
title: Farbtoneffekt
description: Dieser Effekt tönt das Quellbild, indem das Quellbild mit der angegebenen Farbe multipliziert wird. Sie verfügt über eine einzelne Eingabe.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61734e9e060da4609927c9db46eee50dab1bef1e6328f304fdfb2436529289cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384910"
---
# <a name="tint-effect"></a>Farbtoneffekt

Dieser Effekt tönt das Quellbild, indem das Quellbild mit der angegebenen Farbe multipliziert wird. Sie verfügt über eine einzelne Eingabe.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                    | Typ und Standardwert                              | BESCHREIBUNG                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| ColorD2D1– \_ \_ \_ FARBTONPROP-FARBE<br/>               | D2D1 \_ VECTOR \_ 4F(1.0f, 1.0f, 1.0f, 1.0f)<br/> | Farben aus dem Quellbild werden mit diesem Wert multipliziert.       |
| ClampOutputD2D1– AUSGABE DER \_ \_ \_ PROP-KLAMMER \_<br/> | BORAFFERALSE<br/>                                | Gibt an, ob die Ausgabewerte an den Bereich \[ 0, 1 klammern werden sollen \] oder nicht. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |



 ## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
