---
title: Design. currentViewID
description: Das currentViewID-Attribut gibt die aktuell angezeigte Ansicht an oder ruft Sie ab.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- Design. currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372408"
---
# <a name="themecurrentviewid"></a>Design. currentViewID

Das **currentViewID** -Attribut gibt die aktuell angezeigte **Ansicht** an oder ruft Sie ab.

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzeichenfolge, die die **ID** der aktuellen **Ansicht** angibt.  Er besitzt keinen Standardwert.

## <a name="remarks"></a>Bemerkungen

Durch Angeben von **currentViewID** wird die vorhandene **CurrentView** (auf die durch das **View** Global-Attribut verwiesen wird) automatisch geschlossen, und die angegebene **Ansicht** wird geöffnet.

## <a name="examples"></a>Beispiele


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Design-Element**](theme-element.md)
</dt> </dl>

 

 





