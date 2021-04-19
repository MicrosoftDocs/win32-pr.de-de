---
title: Design. openviewrelative
description: Die openviewrelative-Methode öffnet eine Ansicht in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- Design. openviewrelative Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368546"
---
# <a name="themeopenviewrelative"></a>Design. openviewrelative

Die **openviewrelative** -Methode öffnet eine **Ansicht** in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Anschauung*
</dt> <dd>

Eine **Zeichenfolge** , die die **ID** der zu öffnenden **Ansicht** angibt.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*linken*
</dt> <dd>

Eine **Zahl** (**Long**), die den anfänglichen Abstand des linken Rahmens der **Ansicht** vom linken Rand der Skin in Pixel angibt. Ein negativer Wert gibt eine anfängliche Position links vom Skin-Rahmen an.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*Nach oben*
</dt> <dd>

Eine **Zahl** (**Long**), die die ursprüngliche Position des oberen Rahmens der **Ansicht** relativ zum oberen Rand der Skin angibt. Ein negativer Wert gibt eine Ausgangsposition oberhalb des Skin-Rahmens an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die für die **Ansicht** angegebene Position wird verwendet, wenn diese Methode zum ersten Mal aufgerufen wird, nach der der Benutzer die **Ansicht** an eine andere Position ziehen kann. Die neue Position wird gespeichert, und bei nachfolgenden Aufrufen wird die aktuelle Position verwendet.

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

[**Design-Element**](theme-element.md)
</dt> <dt>

[**Design. CloseView**](theme-closeview.md)
</dt> <dt>

[**Design. OpenView**](theme-openview.md)
</dt> </dl>

 

 





