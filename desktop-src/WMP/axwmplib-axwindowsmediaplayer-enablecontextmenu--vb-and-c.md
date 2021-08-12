---
title: AxWindowsMediaPlayer.enableContextMenu-Eigenschaft
description: Die enableContextMenu-Eigenschaft ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird, oder legt diesen fest.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- enableContextMenu-Eigenschaft Windows Media Player
- enableContextMenu-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , enableContextMenu-Eigenschaft
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
ms.openlocfilehash: 5603762ec9823f7e9896c5c22c1dee33f2399bb02301921057f8502046bcc002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582339"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>AxWindowsMediaPlayer.enableContextMenu-Eigenschaft

Die enableContextMenu-Eigenschaft ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein System.Boolean-Wert, der angibt, ob das Kontextmenü aktiviert werden soll. Der Standardwert lautet „true“.

## <a name="remarks"></a>Hinweise

Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enableContextMenu** gleich false und **uiMode** gleich "none" ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player Serie 9 oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





