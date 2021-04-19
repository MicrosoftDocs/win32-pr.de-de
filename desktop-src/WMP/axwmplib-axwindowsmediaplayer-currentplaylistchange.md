---
title: Currentplaylistchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das currentplaylistchange-Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert. | Currentplaylistchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 1f9c99a4-7d10-48bf-b5ff-b1c1d6753b20
keywords:
- Currentplaylistchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99f34f0e02d03352a61bbfca6767295d63d59a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367419"
---
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a>Currentplaylistchange-Ereignis des AxWindowsMediaPlayer-Objekts

Das currentplaylistchange-Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.

``` syntax
[C#]
private void player_CurrentPlaylistChange(
  object sender,
  _WMPOCXEvents_CurrentPlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistChangeEvent
) Handles player.CurrentPlaylistChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistchangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistchangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| change (Ändern)   | WMPLib. wmpplaylistchangeeventtypea-Enumerationswert, der den Typ der Änderung angibt, die für die Wiedergabeliste aufgetreten ist.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt nicht auf, wenn eine andere Wiedergabeliste zur aktuellen Wiedergabeliste wird. Sie tritt nur auf, wenn eine Änderung innerhalb der aktuellen Wiedergabeliste stattfindet, z. b. ein Medien Element, das an die Wiedergabeliste angehängt wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden die Namen aller Medienelemente in der aktuellen Wiedergabeliste als Reaktion auf das currentplaylistchange-Ereignis angezeigt. Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// Add a delegate for the CurrentPlaylistChange event.
player.CurrentPlaylistChange += new AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEventHandler(player_CurrentPlaylistChange);  


private void player_CurrentPlaylistChange(object sender, AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent e)
{
    switch(e.change)
    {
        // Only update the list for the move, delete, insert, and append event types.
        case WMPLib.WMPPlaylistChangeEventType.wmplcMove:    // Value = 3
        case WMPLib.WMPPlaylistChangeEventType.wmplcDelete:  // Value = 4
        case WMPLib.WMPPlaylistChangeEventType.wmplcInsert:  // Value = 5
        case WMPLib.WMPPlaylistChangeEventType.wmplcAppend:  // Value = 6

        // Create a string array large enough to hold all of the media item names.
        int count = player.currentPlaylist.count;
        string[] mediaItems = new string[count];

        // Clear any previous contents of the text box.
        playlistItems.Clear();

        // Loop through the playlist and store each media item name.
        for (int i = 0; i < count; i++)
        {
            mediaItems[i] = player.currentPlaylist.get_Item(i).name;
        }

        // Display the media item names.
        playlistItems.Lines = mediaItems;
        break;
      
        default:
            break;
    }
}
```


```VB

Public Sub player_CurrentPlaylistChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent) Handles player.CurrentPlaylistChange

    Select Case e.change

        &#39; Only update the list for the move, delete, insert, and append event types.
        Case WMPLib.WMPPlaylistChangeEventType.wmplcMove   &#39; Value = 3
        Case WMPLib.WMPPlaylistChangeEventType.wmplcDelete &#39; Value = 4
        Case WMPLib.WMPPlaylistChangeEventType.wmplcInsert &#39; Value = 5
        Case WMPLib.WMPPlaylistChangeEventType.wmplcAppend &#39; Value = 6

            &#39; Create a string array large enough to hold all of the media item names.
            Dim count As Integer = player.currentPlaylist.count
            Dim mediaItems(count) As String

            &#39; Clear any previous contents of the text box.
            playlistItems.Clear()

            &#39; Loop through the playlist and store each media item name.
            For i As Integer = 0 To (count - 1)

                mediaItems(i) = player.currentPlaylist.Item(i).name

            Next i

            &#39; Display the media item names.
            playlistItems.Lines = mediaItems
    End Select

End Sub
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

[**AxWindowsMediaPlayer. currentwiedergabe (VB und c#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. playlistchange-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[**Wmpplaylistchangeeventtype**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





