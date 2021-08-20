---
title: THEME.currentViewID
description: Das currentViewID-Attribut gibt die aktuell angezeigte VIEW-Eigenschaft an oder ruft sie ab.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME.currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21bf3027b0249286689862e53fc2d616d1d33b19eca562c886e981bffb7f0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117811"
---
# <a name="themecurrentviewid"></a>THEME.currentViewID

Das **currentViewID-Attribut** gibt die aktuell angezeigte **VIEW-Eigenschaft** an oder ruft sie ab.

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die die **ID** der aktuellen **VIEW angibt.** Er besitzt keinen Standardwert.

## <a name="remarks"></a>Hinweise

Wenn **Sie currentViewID** angeben, wird die vorhandene **currentView** (auf die durch das globale **View-Attribut** verwiesen wird) automatisch geschlossen, und die angegebene **VIEW** wird geöffnet.

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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**THEME-Element**](theme-element.md)
</dt> </dl>

 

 





