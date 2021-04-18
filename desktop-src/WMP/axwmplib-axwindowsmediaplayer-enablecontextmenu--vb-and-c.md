---
title: AxWindowsMediaPlayer. enablecontextmenu (Eigenschaft)
description: Die enablecontextmenu-Eigenschaft ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das beim Klicken mit der rechten Maustaste angezeigt wird, oder legt diesen fest.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- enablecontextmenu-Eigenschaft, Windows-Media Player
- enablecontextmenu-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, enablecontextmenu (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365174"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>AxWindowsMediaPlayer. enablecontextmenu (Eigenschaft)

Die enablecontextmenu-Eigenschaft ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das beim Klicken mit der rechten Maustaste angezeigt wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein System. Boolean-Wert, der angibt, ob das Kontextmenü aktiviert werden soll. Der Standardwert lautet „true“.

## <a name="remarks"></a>Bemerkungen

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.

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

 

 





