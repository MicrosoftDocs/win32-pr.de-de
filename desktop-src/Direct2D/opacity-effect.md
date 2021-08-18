---
title: Deckkrafteffekt
description: Dieser Effekt passt die Deckkraft eines Bilds an, indem der Alphakanal der Eingabe mit dem angegebenen Deckkraftwert multipliziert wird. Sie verfügt über eine einzelne Eingabe.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58073e3b692b45f86f57c61571d81f5add47427c8a1a801ac43121b37aa43a67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636230"
---
# <a name="opacity-effect"></a>Deckkrafteffekt

Dieser Effekt passt die Deckkraft eines Bilds an, indem der Alphakanal der Eingabe mit dem angegebenen Deckkraftwert multipliziert wird. Sie verfügt über eine einzelne Eingabe.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration              | Typ und Standardwert | Beschreibung                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Deckkraft D2D1 \_ OPACITY \_ PROP \_ OPACITY<br/> | FLOAT1.0f<br/>   | Der Multiplikator zum Alphakanal des Eingabebilds. Der Mindestwert ist 0,0f, und der Höchstwert ist 1,0f. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
