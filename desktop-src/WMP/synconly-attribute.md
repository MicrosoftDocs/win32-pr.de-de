---
title: Synkonstante-Attribut
description: Das synkonstante-Attribut ist eine Zeichen folgen Darstellung eines booleschen Werts, den Windows Media Player verwendet, um zu bestimmen, ob eine Wiedergabeliste nur für die Synchronisierung verfügbar ist.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Synkonforme Attribute (Windows Media Player)
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364839"
---
# <a name="synconly-attribute"></a>Synkonstante-Attribut

Das **synkonstante** -Attribut ist eine Zeichen folgen Darstellung eines **booleschen** Werts, den Windows Media Player verwendet, um zu bestimmen, ob eine Wiedergabeliste nur für die Synchronisierung verfügbar ist.

## <a name="applies-to"></a>Gilt für

-   [Wiedergabelisten](playlist-attributes-ref.md)

## <a name="remarks"></a>Bemerkungen

Der Wert 1 gibt an, dass die Wiedergabeliste nur für die Synchronisierung verfügbar ist und nicht im Knoten " **automatische Wiedergabeliste** " angezeigt werden kann. Der Wert 0 (null) gibt an, dass die Wiedergabeliste im Knoten **automatische Wiedergabeliste** angezeigt werden kann.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





