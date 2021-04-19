---
title: Iwmpmedia ismembership of-Methode
description: Die ismembership of-Methode gibt einen Wert zurück, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- ismembership of-Methode, Windows-Media Player
- ismembership of-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, ismembership of-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358745"
---
# <a name="iwmpmediaismemberof-method"></a>Iwmpmedia:: ismembership of-Methode

Die **ismembership of** -Methode gibt einen Wert zurück, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pwiedergabe* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmpwiedergabe** -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Boolean** -Wert, der angibt, ob das Medien Element ein Member der Wiedergabeliste ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann die von der **iwmpmediacollection** -Schnittstelle abgerufenen Wiedergabelisten nicht überprüfen. Um zu testen, ob ein Medien Element ein Member einer bestimmten benannten Wiedergabeliste ist, rufen Sie die Wiedergabelisten Auflistung mit der Eigenschaft **AxWindowsMediaPlayer. playlistcollection** ab. Nachdem Sie die Auflistung abgerufen haben, rufen Sie die einzelne Wiedergabeliste durch Aufrufen der **iwmpplaylistcollection. getByName** -Methode ab.

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **ismembership of** verwendet, um zu testen, ob das aktuelle Medien Element ein Member der Wiedergabeliste mit dem Namen alle Musik ist. Wenn dies nicht der Fall ist, wird das aktuelle Medien Element an die Wiedergabeliste angehängt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer. playlistcollection (VB und c#)**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. getByName (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





