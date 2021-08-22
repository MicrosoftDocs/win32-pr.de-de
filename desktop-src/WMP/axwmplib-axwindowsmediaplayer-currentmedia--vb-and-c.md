---
title: AxWindowsMediaPlayer.currentMedia-Eigenschaft
description: Die currentMedia-Eigenschaft ruft die IWMPMedia-Schnittstelle ab, die dem aktuellen Medienelement entspricht, oder legt sie fest.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- currentMedia-Eigenschaft Windows Media Player
- currentMedia-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , currentMedia-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027949872b2ff988fcfcad5a8464d9a48ed69d3389ddbca0ad4f91b2d9e3c8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098840"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>AxWindowsMediaPlayer.currentMedia-Eigenschaft

Die currentMedia-Eigenschaft ruft die IWMPMedia-Schnittstelle ab, die dem aktuellen Medienelement entspricht, oder legt sie fest.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>Eigenschaftswert

Die WMPLib.IWMPMedia-Schnittstelle, die Zugriff auf das aktuelle Medienelement bereitstellt.

## <a name="remarks"></a>Hinweise

Wenn axWindowsMediaPlayer.settings. **Die autoStart-Eigenschaft** ist true, die Wiedergabe beginnt automatisch, sobald Sie **currentMedia** festlegen.

Sie können eine IWMPMedia-Schnittstelle für ein bestimmtes Medienelement über die IWMPPlaylist.Item-Eigenschaft (die IWMPPlaylist.get \_ Item-Methode in C#) abrufen. Um ein Medienelement mit einem Dateinamen zu laden, legen Sie die URL-Eigenschaft fest, oder verwenden Sie newMedia.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das erste Medienelement in der Bibliothek abgerufen und die currentMedia-Eigenschaft verwendet, um das abgerufene Medienelement als aktuelles Medienelement festzulegen und dessen Namen anzuzeigen. Das AxWMPLib.AxWindowsMediaPlayer-Objekt wird durch die Variable player dargestellt.


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
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

[**AxWindowsMediaPlayer.newMedia (VB und C#)**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB und C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Item (VB und C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.autoStart (VB und C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





