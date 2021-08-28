---
title: AxWindowsMediaPlayer.openPlayer-Methode
description: Die openPlayer-Methode wird Windows Media Player der angegebenen URL geöffnet. | AxWindowsMediaPlayer.openPlayer-Methode
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- openPlayer-Windows Media Player
- openPlayer-Methode Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , openPlayer-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a2ae5660969e78aeb165c5f9fd9420ea04c79a6aeec9a57c4627cd61d32ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764710"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>AxWindowsMediaPlayer.openPlayer-Methode

Die **openPlayer-Methode** wird Windows Media Player der angegebenen URL geöffnet.

## <a name="syntax"></a>Syntax


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrURL* 
</dt> <dd>

Die **System.String,die** die URL des medienelements ist, das wiedergibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode startet Windows Media Player, bei der die angegebene URL als aktuelles Medienelement festgelegt ist. Wenn der Player zuvor im Skinmodus geschlossen wurde, wird er mit der zuletzt vom Benutzer ausgewählten Skin geöffnet. Andernfalls wird der Player im Vollmodus geöffnet.

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

 

 





