---
title: AxWindowsMediaPlayer. openplayer-Methode
description: Die openplayer-Methode öffnet Windows Media Player unter Verwendung der angegebenen URL. | AxWindowsMediaPlayer. openplayer-Methode
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- openplayer-Methode, Windows-Media Player
- openplayer-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, openplayer-Methode
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
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358291"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>AxWindowsMediaPlayer. openplayer-Methode

Die **openplayer** -Methode öffnet Windows Media Player unter Verwendung der angegebenen URL.

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

Die **System. String** -URL, die die URL des wieder zugebende Medien Elements ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird Windows Media Player gestartet, wobei der angegebene URL als Aktuelles Medien Element festgelegt ist. Wenn der Spieler zuvor im Skin-Modus geschlossen wurde, wird er mithilfe der Skin geöffnet, die zuletzt vom Benutzer ausgewählt wurde. Andernfalls wird der Spieler im vollständigen Modus geöffnet.

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

 

 





