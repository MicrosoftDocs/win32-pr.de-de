---
title: attribute_onchange
description: Wenn ein Skinattribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann. Der Name des Ereignishandlers ist der Name des Attributs, gefolgt von einem Unterstrich und \0034;onchange \ 0034;, z. B. \0034;value \_ onchange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c707b04587b6e975f81c8a0d0918b14c8e193d303f82c61b5220796bb6975b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573760"
---
# <a name="attribute_onchange"></a>Attribut \_ onchange

Wenn ein Skinattribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann. Der Name des Ereignishandlers ist der Name des Attributs, gefolgt von einem Unterstrich und "onchange", z. B. "value \_ onchange".

``` syntax
        attribute_onchange
```

## <a name="examples"></a>Beispiele


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Ereignishandler**](ambient-event-handlers.md)
</dt> </dl>

 

 





