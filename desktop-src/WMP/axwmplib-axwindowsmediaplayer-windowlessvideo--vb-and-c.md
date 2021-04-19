---
title: AxWindowsMediaPlayer. windowlessvideo (Eigenschaft)
description: Mit der windowlessvideo-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- windowlessvideo-Eigenschaften Fenster Media Player
- windowlessvideo-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, windowlessvideo (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367218"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>AxWindowsMediaPlayer. windowlessvideo (Eigenschaft)

Mit der windowlessvideo-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein System. Boolean-Wert, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert. Der Standardwert ist „FALSE“.

## <a name="remarks"></a>Bemerkungen

Standardmäßig rendert ein eingebettetes Windows-Media Player-Steuerelement Videos in einem eigenen Fenster innerhalb des Client Bereichs. Wenn **windowlessvideo** auf "true" festgelegt ist, rendert das Windows-Media Player-Objekt Video direkt im Client Bereich, sodass Sie besondere Effekte anwenden oder das Video mit Text auf eine Ebene anwenden können.

In Windows Vista kann das Rendern von Videos im fensterlosen Modus die Leistung beeinträchtigen.

Das erhalten eines Werts für diese Eigenschaft wird für den Netscape-Navigator nicht unterstützt. Wenn Sie einen Wert für diese Eigenschaft in Netscape Navigator festlegen, kann dies zu unerwarteten Ergebnissen führen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





