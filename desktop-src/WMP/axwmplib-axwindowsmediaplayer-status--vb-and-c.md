---
title: AxWindowsMediaPlayer.status-Eigenschaft
description: Die status-Eigenschaft ruft einen Wert ab, der den Status der Windows Media Player.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Statuseigenschafts-Windows Media Player
- status-eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , Statuseigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac46eeef411e1d728994d829d95727cdaf4020c2ef1b7511391b6ca0d2e31ff7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864560"
---
# <a name="axwindowsmediaplayerstatus-property"></a>AxWindowsMediaPlayer.status-Eigenschaft

Die status-Eigenschaft ruft einen Wert ab, der den Status der Windows Media Player.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die System.String, die den Status aufgibt.

## <a name="remarks"></a>Hinweise

Die in dieser Eigenschaft enthaltenen Werte können jederzeit geändert werden und sollten nur zu Anzeigezwecken verwendet werden.

Der AxWindowsMediaPlayer. **Das StatusChange-Ereignis** wird ausgelöst, wenn diese Eigenschaft den Wert ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.StatusChange-Ereignis (VB und C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





