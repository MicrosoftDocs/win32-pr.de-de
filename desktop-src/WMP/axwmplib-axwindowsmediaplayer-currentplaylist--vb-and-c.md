---
title: AxWindowsMediaPlayer.currentPlaylist-Eigenschaft
description: Die currentPlaylist-Eigenschaft ruft die aktuelle IWMPPlaylist-Schnittstelle ab, die eine einfache Möglichkeit zum Organisieren und Bearbeiten von Medienelementen in einer Liste bietet, oder legt sie fest.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- currentPlaylist-Eigenschaft Windows Media Player
- currentPlaylist-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , currentPlaylist-Eigenschaft
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
ms.openlocfilehash: f976084773a333e40c0a278878e9a35ed913e5911ec732c0dccfe6525e5f45a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765261"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>AxWindowsMediaPlayer.currentPlaylist-Eigenschaft

Die currentPlaylist-Eigenschaft ruft die aktuelle **IWMPPlaylist-Schnittstelle** ab, die eine einfache Möglichkeit zum Organisieren und Bearbeiten von Medienelementen in einer Liste bietet, oder legt sie fest.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Eigenschaftswert

Die WMPLib.IWMPPlaylist-Schnittstelle, die Zugriff auf die aktuelle Wiedergabeliste bietet.

## <a name="remarks"></a>Hinweise

Wenn die IWMPSettings.autoStart-Eigenschaft (auch über AxWindowsMediaPlayer.settings zugegriffen wird).**autoStart**) ist true, die Wiedergabe beginnt automatisch, sobald Sie **currentPlaylist** festlegen.

Diese Eigenschaft nimmt eine IWMPPlaylist-Schnittstelle an, die auf verschiedene Weise erworben werden kann, z. B. durch Abrufen des Werts aus dem *IWMPPlaylistArray.* **Item** oder *IWMPPlaylistCollection*. **newPlaylist-Eigenschaften.** Um ein **Wiedergabelistenelement** mit einem Dateinamen zu laden, legen Sie die URL-Eigenschaft fest, oder verwenden Sie AxWindowsMediaPlayer. **newPlaylist**.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die erste Wiedergabeliste in der Bibliothek abgerufen und die currentPlaylist-Eigenschaft verwendet, um die abgerufene Wiedergabeliste als aktuelle Wiedergabeliste festzulegen und ihren Namen anzuzeigen. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.newPlaylist (VB und C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer.settings (VB und C#)**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.Item (VB und C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB und C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB und C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





