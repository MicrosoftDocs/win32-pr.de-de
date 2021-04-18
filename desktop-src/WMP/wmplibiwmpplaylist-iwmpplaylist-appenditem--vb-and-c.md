---
title: Iwmpwiedergabe appendItem-Methode
description: Mit der appendItem-Methode wird am Ende einer Wiedergabeliste ein Medien Element hinzugefügt.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- appendItem-Methode, Windows Media Player
- appendItem-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, appendItem-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354753"
---
# <a name="iwmpplaylistappenditem-method"></a>Iwmpwiedergabe:: appendItem-Methode

Mit der **appendItem** -Methode wird am Ende einer Wiedergabeliste ein Medien Element hinzugefügt.

## <a name="syntax"></a>Syntax


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*piwmpmedia* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmpmedia** -Schnittstelle, die das anzufügende Medien Element darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **appendItem** verwendet, um der Wiedergabeliste das aktuelle Medien Element mit dem Namen "threelist" hinzuzufügen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





