---
title: Deckkraft Effekt
description: Dadurch wird die Deckkraft eines Bilds angepasst, indem der Alphakanal der Eingabe mit dem angegebenen Deckkraft Wert multipliziert wird. Sie verfügt über eine einzelne Eingabe.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341404"
---
# <a name="opacity-effect"></a>Deckkraft Effekt

Dadurch wird die Deckkraft eines Bilds angepasst, indem der Alphakanal der Eingabe mit dem angegebenen Deckkraft Wert multipliziert wird. Sie verfügt über eine einzelne Eingabe.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration              | Typ und Standardwert | BESCHREIBUNG                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Deckkraft D2D1 \_ Deckkraft \_ \_<br/> | Float 1.0 f<br/>   | Der Multiplikator des Alphakanals des Eingabe Bilds. Der Minimalwert ist 0,0 f, und der Höchstwert ist 1.0 f. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
