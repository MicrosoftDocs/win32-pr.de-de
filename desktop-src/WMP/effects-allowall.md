---
title: EFFECTS.allowAll
description: Das attribut allowAll gibt einen Wert an, der angibt, ob alle Visualisierungen, die sich in der Registrierung befinden, eingeschlossen werden sollen, oder ruft diesen ab.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTS.allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a87aa8336e3961b31716c8d6bbfaa6aee71374a0f3c6e17b644a47136df550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996845"
---
# <a name="effectsallowall"></a>EFFECTS.allowAll

Das **attribut allowAll** gibt einen Wert an, der angibt, ob alle Visualisierungen in die Registrierung eingeschlossen werden sollen, oder ruft diesen ab.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                                                         |
|-------|---------------------------------------------------------------------|
| true  | Standard. Ermöglicht das Durchlaufen aller Visualisierungen im System des Benutzers. |
| false | Schränkt das Durchlaufen von Visualisierungen ein, die in **EFFECTS-Tags** angezeigt werden. |



 

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut auf FALSE festgelegt ist, können nur die Visualisierungen, die in **EFFECTS-Tags** angezeigt werden, mithilfe von previous/next durchlaufen werden. Wenn sie auf TRUE festgelegt ist, können alle Visualisierungen, die auf dem System des Benutzers registriert sind, durchlaufen werden. Wenn sie auf TRUE festgelegt ist und Sie visualisierungen in **EFFECTS-Tags** angeben, werden die in diesen Tags angegebenen Attribute auf alle Visualisierungen im System des Benutzers angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EFFECTS-Element**](effects-element.md)
</dt> </dl>

 

 





