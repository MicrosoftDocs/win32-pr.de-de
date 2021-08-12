---
title: AxWindowsMediaPlayer.windowlessVideo (Eigenschaft)
description: Die windowlessVideo-Eigenschaft ruft einen Wert ab, der angibt, ob das Windows Media Player Video im fensterlosen Modus rendert, oder legt einen Wert fest.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- windowlessVideo-Windows Media Player
- windowlessVideo-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , windowlessVideo-Eigenschaft
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
ms.openlocfilehash: 3a63a7246e730f73bd6d6f27111112a3db2029e3b53c80569e2e013771da6708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581520"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>AxWindowsMediaPlayer.windowlessVideo (Eigenschaft)

Die windowlessVideo-Eigenschaft ruft einen Wert ab, der angibt, ob das Windows Media Player Video im fensterlosen Modus rendert, oder legt einen Wert fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Ein boolescher System.Boolean-Wert, der angibt, ob das Windows Media Player-Steuerelement Video im fensterlosen Modus rendert. Der Standardwert ist „FALSE“.

## <a name="remarks"></a>Hinweise

Standardmäßig rendert ein eingebettetes Windows Media Player Video in einem eigenen Fenster innerhalb des Clientbereichs. Wenn **windowlessVideo** auf TRUE festgelegt ist, rendert das Windows Media Player-Objekt Video direkt im Clientbereich, sodass Sie Sondereffekte anwenden oder das Video mit Text über ebenen können.

In Windows Vista kann das Rendern von Videos im fensterlosen Modus die Leistung beeinträchtigen.

Das Abrufen eines Werts für diese Eigenschaft wird für Netscape Navigator. Das Festlegen eines Werts für diese Eigenschaft in Netscape Navigator zu unerwarteten Ergebnissen führen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





