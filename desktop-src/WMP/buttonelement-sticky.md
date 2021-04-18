---
title: ButtonElement. Kurznotiz
description: Das Attribut "Kurznotiz" gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob das Button Element eine UMSCHALT Fläche ist, d. h. ob es sich um eine Schaltfläche mit zwei Zuständen oder einem einzelnen Zustand handelt
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- ButtonElement. Sticky-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361548"
---
# <a name="buttonelementsticky"></a>ButtonElement. Kurznotiz

Das **Attribut "** Kurznotiz" gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob das Button **Element** eine UMSCHALT Fläche ist, d. h. ob es sich um eine Schaltfläche mit zwei Zuständen oder einem einzelnen Zustand handelt

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                               |
|-------|-------------------------------------------|
| true  | **ButtonElement** ist eine Kurznotiz.              |
| false | Standard. **ButtonElement** ist nicht Kurznotiz. |



 

## <a name="remarks"></a>Bemerkungen

Wenn das **Attribut "** Kurznotiz" auf "true" festgelegt ist, wechselt das Schaltflächen Element in den Zustand "nach unten" und verbleibt in diesem Zustand, bis er erneut geklickt wird. Wenn sich das Button-Element im Zustand "nach unten" befindet, ist das Attribut " **nach unten** " auf "true" festgelegt, und der entsprechende Teil der Schaltflächen Gruppe " **downImage** "

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonElement-Element**](buttonelement-element.md)
</dt> <dt>

[**ButtonElement. Down**](buttonelement-down.md)
</dt> <dt>

[**ButtonGroup. downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





