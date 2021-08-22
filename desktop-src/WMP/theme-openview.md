---
title: THEME.openView
description: Die openView-Methode öffnet eine VIEW-Ansicht in einem neuen Fenster.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- THEME.openView-Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e5dd33760cb86ef1f85f7efd8a3ff38cb36f0408076555e2fe8732ffb53779a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466610"
---
# <a name="themeopenview"></a>THEME.openView

Die **openView-Methode** öffnet eine **VIEW-Ansicht** in einem neuen Fenster.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*ansehen*
</dt> <dd>

Eine **Zeichenfolge,** die die **ID** der zu öffnenden **ANSICHT** angibt.

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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**THEME-Element**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





