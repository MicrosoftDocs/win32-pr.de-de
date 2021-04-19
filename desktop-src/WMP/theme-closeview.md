---
title: Design. CloseView
description: Die CloseView-Methode schließt eine geöffnete Ansicht.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- Design. CloseView-Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371081"
---
# <a name="themecloseview"></a>Design. CloseView

Die **CloseView** -Methode schließt eine geöffnete **Ansicht**.

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*der Ansicht*
</dt> <dd>

Eine **Zeichenfolge** , die die **ID** der **Sicht** angibt, die geschlossen werden soll.

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
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Design-Element**](theme-element.md)
</dt> <dt>

[**Design. OpenView**](theme-openview.md)
</dt> </dl>

 

 





