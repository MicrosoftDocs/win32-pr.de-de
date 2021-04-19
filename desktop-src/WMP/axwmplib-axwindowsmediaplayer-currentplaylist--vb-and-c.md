---
title: AxWindowsMediaPlayer. currentwiedergabe (Eigenschaft)
description: Die currentwiedergabe-Eigenschaft ruft die aktuelle iwmpwiedergabe-Schnittstelle ab, die eine einfache Möglichkeit zum organisieren und Bearbeiten von Medien Elementen in einer Liste bietet, oder legt diese fest.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- currentwiedergabe-Eigenschaft, Windows-Media Player
- currentwiedergabe-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, currentwiedergabe-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368636"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>AxWindowsMediaPlayer. currentwiedergabe (Eigenschaft)

Die currentwiedergabe-Eigenschaft ruft die aktuelle **iwmpwiedergabe** -Schnittstelle ab, die eine einfache Möglichkeit zum organisieren und Bearbeiten von Medien Elementen in einer Liste bietet, oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Eigenschaftswert

Die WMPLib. iwmpwiedergabe-Schnittstelle, die Zugriff auf die aktuelle Wiedergabeliste bereitstellt.

## <a name="remarks"></a>Bemerkungen

, Wenn die iwmpsettings. AutoStart-Eigenschaft (auch über AxWindowsMediaPlayer. Settings aufgerufen wird.**Autostart**) ist "true", wenn Sie " **currentwiedergabe**" festlegen, beginnt die Wiedergabe automatisch.

Diese Eigenschaft nimmt eine iwmpwiedergabe-Schnittstelle an, die auf verschiedene Weise abgerufen werden kann, z. b. durch das erhalten des Werts aus dem *iwmpplaylistarray*. **Element** oder *iwmpplaylistcollection*. **newwiedergabe** -Eigenschaften. Wenn Sie ein **Wiedergabe** Listenelement mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest, oder verwenden Sie AxWindowsMediaPlayer. **newwiedergabe**.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die erste Wiedergabeliste in der Bibliothek abgerufen und die currentwiedergabe-Eigenschaft verwendet, um die abgerufene Wiedergabeliste als aktuelle Wiedergabeliste festzulegen und deren Namen anzuzeigen. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. newwiedergabe (VB und c#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer. Settings (VB und c#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistarray. Item (VB und c#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. newwiedergabe (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. Autostart (VB und c#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





