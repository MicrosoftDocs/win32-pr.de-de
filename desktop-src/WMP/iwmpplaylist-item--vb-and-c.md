---
title: Iwmpwiedergabe. Item (VB und C)
description: Die Item-Eigenschaft (die get \_ Item-Methode in C \) Ruft eine Schnittstelle zum Medien Element am angegebenen Index ab.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- Iwmpwiedergabe. Item (VB und C) Windows Media Player
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
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364413"
---
# <a name="iwmpplaylistitem-vb-and-c"></a>Iwmpwiedergabe. Item (VB und c#)

Die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) Ruft eine Schnittstelle zum Medien Element am angegebenen Index ab.


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

Ein **System. Int32** -Wert, der den Index des Medien Elements in der Wiedergabeliste ist.

## <a name="property-value"></a>Eigenschaftswert

Eine **WMPLib. iwmpmedia** -Schnittstelle, die Zugriff auf das Medien Element am angegebenen Index bereitstellt.

## <a name="remarks"></a>Bemerkungen

**Iwmpwiedergabe. Item** ist eine schreibgeschützte Eigenschaft in Visual Basic, die einen-Parameter annimmt, während in c# als **iwmpwiedergabe. get- \_ Element** Methode bezeichnet wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) zum Abrufen eines Medien Elements aus einer Wiedergabeliste basierend auf einer Benutzer Auswahl verwendet. Ein Listenfeld mit dem Namen weblist wurde erstellt und mit den Titeln der Wiedergabeliste mit dem Namen audioplaylist gefüllt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. InsertItem (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Iwmpwiedergabe. RemoveItem (VB und c#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





