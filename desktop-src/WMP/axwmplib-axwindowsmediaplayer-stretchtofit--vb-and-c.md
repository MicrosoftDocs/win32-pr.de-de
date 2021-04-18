---
title: AxWindowsMediaPlayer. stretchdefit (Eigenschaft)
description: Mit der Eigenschaft stretchdefit wird ein Wert abgerufen oder festgelegt, der angibt, ob die Größe des Videos, das vom Windows Media Player-Steuerelement angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Eigenschaften Fenster für stretchdefit-Eigenschaft Media Player
- stretchdefit-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, stretchdefit (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354675"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>AxWindowsMediaPlayer. stretchdefit (Eigenschaft)

Mit der Eigenschaft stretchdefit wird ein Wert abgerufen oder festgelegt, der angibt, ob die Größe des Videos, das vom Windows Media Player-Steuerelement angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Der System. Boolean-Wert, der angibt, ob das Video so gestreckt wird, dass es an das Fenster angepasst wird. Der Standardwert ist „FALSE“.

## <a name="remarks"></a>Bemerkungen

Wenn **stretchdefit** auf true festgelegt ist, wird das ursprüngliche Seitenverhältnis des Videos vom Windows Media Player-Steuerelement beibehalten. Wenn das Seitenverhältnis des Videos nicht mit dem Seitenverhältnis des Videofensters identisch ist, können schwarze Masken Bereiche entweder am oberen und unteren Rand des Video Bilds angezeigt werden.

Diese Eigenschaft gilt nur für das Windows Media Player-Steuerelement, wenn es in eine Webseite eingebettet ist.

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

 

 





