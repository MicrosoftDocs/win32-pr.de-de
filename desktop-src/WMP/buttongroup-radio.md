---
title: BUTTONGROUP.radio
description: Das Optionsattribut gibt einen Wert an, der angibt, ob buttongroup aus Optionsfeldern besteht, oder ruft einen Wert ab.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP.radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a8a9f85a3dce5ef070519f436c28ec157f7aa467a9115bcd8e2ccefa6444f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997770"
---
# <a name="buttongroupradio"></a>BUTTONGROUP.radio

Das  Optionsattribut gibt einen Wert an, der angibt, ob **buttongroup** aus Optionsfeldern besteht, oder ruft einen Wert ab.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                                      |
|-------|--------------------------------------------------|
| true  | **BUTTONGROUP** ist ein Optionsfeldformat.              |
| false | Standard. **BUTTONGROUP** ist kein Optionsfeldformat. |



 

## <a name="remarks"></a>Hinweise

Wenn **das Optionsfeld** auf TRUE festgelegt ist, sind alle **BUTTONELEMENT-Elemente** in **buttongroup** sticky, aber nur jeweils eine Schaltfläche befindet sich im Zustand "Down".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTONELEMENT.sticky**](buttonelement-sticky.md)
</dt> <dt>

[**BUTTONGROUP-Element**](buttongroup-element.md)
</dt> </dl>

 

 





