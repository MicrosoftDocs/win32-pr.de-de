---
title: BUTTON.sticky
description: Das Sticky-Attribut gibt einen Wert an oder ruft einen Wert ab, der angibt, ob button ein Umschalter ist, d. h. ob es sich um eine SCHALTFLÄCHE mit zwei oder einem einzelnen Zustand handelt.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BUTTON.sticky Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9c6a2cf1523cf2384142bd6ffd47cb5e42e7851dc96b6e236343c5ba670aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342746"
---
# <a name="buttonsticky"></a>BUTTON.sticky

Das **Sticky-Attribut** gibt einen Wert an oder ruft einen Wert ab, der angibt, ob es sich bei **BUTTON** um eine Umschaltfläche handelt, d. h. ob es sich um eine **SCHALTFLÄCHE** mit zwei oder einem einzelnen Zustand handelt.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                        |
|-------|------------------------------------|
| true  | **BUTTON** ist sticky.              |
| false | Standard. **BUTTON** ist nicht sticky. |



 

## <a name="remarks"></a>Hinweise

Wenn **sticky** auf TRUE festgelegt ist, wechselt die **SCHALTFLÄCHE** beim Klicken in den Abwärtszustand und verbleibt in diesem Zustand, bis sie erneut angeklickt wird. Wenn **sich** button im Zustand "Down" befindet, ist das **Down-Attribut** true, und **downImage** wird angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> </dl>

 

 





