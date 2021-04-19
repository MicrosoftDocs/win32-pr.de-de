---
title: Design. OpenView
description: Die OpenView-Methode öffnet eine Ansicht in einem neuen Fenster.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- Design. OpenView-Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373770"
---
# <a name="themeopenview"></a>Design. OpenView

Die **OpenView** -Methode öffnet eine **Ansicht** in einem neuen Fenster.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Anschauung*
</dt> <dd>

Eine **Zeichenfolge** , die die **ID** der zu öffnenden **Ansicht** angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele


```JScript
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

[**Design. CloseView**](theme-closeview.md)
</dt> <dt>

[**Design. openviewrelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





