---
title: IWMPPlaylist.Item (VB und C )
description: Die Item-Eigenschaft (die \_ Get Item-Methode in C\) ruft eine Schnittstelle zum Medienelement am angegebenen Index ab.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- IWMPPlaylist.Item (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b4c29b5f3821ad2ec3434fcad2defc2e4128e7f6e69c70940294ef0ff7f963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575417"
---
# <a name="iwmpplaylistitem-vb-and-c"></a>IWMPPlaylist.Item (VB und C#)

Die **Item-Eigenschaft** (die **Get \_ Item-Methode** in C#) ruft eine Schnittstelle zum Medienelement am angegebenen Index ab.


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a>Parameter

*Lindex*

Ein **System.Int32,** das der Index des Medienelements in der Wiedergabeliste ist.

## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib.IWMPMedia-Schnittstelle,** die Zugriff auf das Medienelement am angegebenen Index bereitstellt.

## <a name="remarks"></a>Hinweise

**IWMPPlaylist.Item** ist eine schreibgeschützte Eigenschaft in Visual Basic, die einen Parameter annimmt, während sie in C# als **IWMPPlaylist.get \_ Item-Methode** bezeichnet wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **Item-Eigenschaft** (die **\_ Get Item-Methode** in C#) verwendet, um ein Medienelement basierend auf einer Benutzerauswahl aus einer Wiedergabeliste abzurufen. Ein Listenfeld wurde mit dem Namen weblist erstellt und mit den Titeln aus der Wiedergabeliste namens audioPlaylist gefüllt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.insertItem (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.removeItem (VB und C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





