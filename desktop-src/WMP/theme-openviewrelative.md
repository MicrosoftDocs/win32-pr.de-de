---
title: THEME.openViewRelative
description: Die openViewRelative-Methode öffnet eine VIEW in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEME.openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a26040bb8f47d85be99f0d8df602bdd69835cfa648ac6d5898f786e4518acdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117774"
---
# <a name="themeopenviewrelative"></a>THEME.openViewRelative

Die **openViewRelative-Methode** öffnet eine **VIEW** in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*ansehen*
</dt> <dd>

Eine **Zeichenfolge,** die die **ID der** zu **öffnenden VIEW-Datei** angibt.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*Links*
</dt> <dd>

Eine **Zahl** (**long**), die den anfänglichen Abstand des linken Rahmens der **VIEW** vom linken Rand der Skin in Pixel an gibt. Ein negativer Wert gibt eine Anfangsposition links vom Skin-Rahmen an.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*Nach oben*
</dt> <dd>

Eine **Zahl** (**long**), die die Anfangsposition des oberen Rahmens der **VIEW** relativ zum oberen Rahmen der Skin an gibt. Ein negativer Wert gibt eine Anfangsposition über dem Skin-Rahmen an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die für view angegebene **Position** wird beim ersten Aufrufen dieser Methode verwendet, nach der der Benutzer **view** an eine andere Position ziehen kann. Die neue Position wird gespeichert, und bei nachfolgenden Aufrufen wird die letzte Position verwendet.

## <a name="examples"></a>Beispiele


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**THEME-Element**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





