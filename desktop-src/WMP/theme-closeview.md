---
title: THEME.closeView
description: Die closeView-Methode schließt eine geöffnete VIEW-Ansicht.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- THEME.closeView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e66a0c56ab2f5fc3d5d6a27d996d8b3f3cf7834c61e62113a40af3c42aeb4d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932545"
---
# <a name="themecloseview"></a>THEME.closeView

Die **closeView-Methode** schließt eine geöffnete **VIEW -Methode.**

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*
</dt> <dd>

Eine **Zeichenfolge,** die die **ID** **der** ansicht angibt, die geschlossen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**THEME-Element**](theme-element.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





