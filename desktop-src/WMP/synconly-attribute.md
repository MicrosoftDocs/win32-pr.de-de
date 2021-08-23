---
title: SyncOnly-Attribut
description: Das SyncOnly-Attribut ist eine Zeichenfolgendarstellung eines booleschen Werts, der Windows Media Player verwendet, um zu bestimmen, ob eine Wiedergabeliste nur für die Synchronisierung verfügbar ist.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- SyncOnly-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77fe67fe3cb943ad210f4d9beb58cfea8f32da87e6ee15955b578f07a608f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134733"
---
# <a name="synconly-attribute"></a>SyncOnly-Attribut

Das **SyncOnly-Attribut** ist eine **Zeichenfolgendarstellung eines booleschen Werts,** der Windows Media Player verwendet, um zu bestimmen, ob eine Wiedergabeliste nur für die Synchronisierung verfügbar ist.

## <a name="applies-to"></a>Gilt für

-   [Wiedergabelisten](playlist-attributes-ref.md)

## <a name="remarks"></a>Hinweise

Der Wert 1 gibt an, dass die Wiedergabeliste nur für die Synchronisierung verfügbar ist und nicht im Knoten **Automatische Wiedergabeliste** angezeigt werden kann. Der Wert 0 (null) gibt an, dass die Wiedergabeliste im Knoten **Automatische Wiedergabeliste** angezeigt werden kann.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





