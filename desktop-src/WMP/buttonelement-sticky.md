---
title: BUTTONELEMENT.sticky
description: Das sticky-Attribut gibt einen Wert an oder ruft einen Wert ab, der angibt, ob buttonelement ein Umschalter ist, d.&a; ob es sich um eine Schaltfläche mit zwei oder einem Zustand handelt.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT.sticky Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc8a709fc28f0d1529c58725db5856931195a66cc370559dd9d14af61e869db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120036"
---
# <a name="buttonelementsticky"></a>BUTTONELEMENT.sticky

The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                               |
|-------|-------------------------------------------|
| true  | **BUTTONELEMENT** ist sticky.              |
| false | Standard. **BUTTONELEMENT** ist nicht sticky. |



 

## <a name="remarks"></a>Hinweise

Wenn das **sticky-Attribut** auf TRUE festgelegt ist, ändert sich das Schaltflächenelement in den Zustand "Down", wenn darauf geklickt wird, und verbleibt in diesem Zustand, bis es erneut angeklickt wird. Wenn sich das Schaltflächenelement im Down-Zustand befindet, ist das **down-Attribut** true, und der entsprechende Teil der Schaltflächengruppe **downImage** wird angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTONELEMENT-Element**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.down**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





