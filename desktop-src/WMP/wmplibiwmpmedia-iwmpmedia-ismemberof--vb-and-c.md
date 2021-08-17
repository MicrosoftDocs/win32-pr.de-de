---
title: IWMPMedia isMemberOf-Methode
description: Die isMemberOf-Methode gibt einen Wert zurück, der angibt, ob das angegebene Medienelement ein Member der angegebenen Wiedergabeliste ist.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- isMemberOf-Methode Windows Media Player
- isMemberOf-Methode Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , isMemberOf-Methode
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
ms.openlocfilehash: 485121f0ac9c4c441ff90e34b90ef5c9475c22995565b018d3f0e00dc5d94740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746015"
---
# <a name="iwmpmediaismemberof-method"></a>IWMPMedia::isMemberOf-Methode

Die **isMemberOf-Methode** gibt einen Wert zurück, der angibt, ob das angegebene Medienelement ein Member der angegebenen Wiedergabeliste ist.

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

*pPlaylist* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPPlaylist-Schnittstelle.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Boolean-Wert,** der angibt, ob das Medienelement Mitglied der Wiedergabeliste ist.

## <a name="remarks"></a>Hinweise

Diese Methode kann keine Wiedergabelisten überprüfen, die über die **IWMPMediaCollection-Schnittstelle** abgerufen wurden. Um zu testen, ob ein Medienelement Mitglied einer bestimmten benannten Wiedergabeliste ist, rufen Sie die Wiedergabelistensammlung mit der **AxWindowsMediaPlayer.playlistCollection-Eigenschaft** ab. Rufen Sie nach dem Abrufen der Sammlung die einzelne Wiedergabeliste ab, indem Sie die **IWMPPlaylistCollection.getByName-Methode** aufrufen.

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **isMemberOf** verwendet, um zu testen, ob das aktuelle Medienelement mitglied der Wiedergabeliste mit dem Namen All Musik ist. Wenn dies nicht dere ist, wird das aktuelle Medienelement an die Wiedergabeliste angefügt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer.playlistCollection (VB und C#)**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB und C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





