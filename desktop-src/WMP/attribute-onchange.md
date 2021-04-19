---
title: attribute_onchange
description: Wenn ein Skin-Attribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann. Der Name des Ereignis Handlers ist der Name des Attributs, gefolgt von einem Unterstrich und \ 0034; OnChange \ 0034;, z. b. \ 0034; Value \_ OnChange \ 0034;.
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
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370236"
---
# <a name="attribute_onchange"></a>Attribut \_ OnChange

Wenn ein Skin-Attribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann. Der Name des Ereignis Handlers ist der Name des Attributs, gefolgt von einem Unterstrich und "OnChange", z. b. "Value \_ OnChange".

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
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Ereignishandler**](ambient-event-handlers.md)
</dt> </dl>

 

 





