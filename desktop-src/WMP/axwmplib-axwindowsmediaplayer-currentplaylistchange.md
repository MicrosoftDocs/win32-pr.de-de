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
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b2868-105">Currentplaylistchange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="b2868-105">CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b2868-106">Das currentplaylistchange-Ereignis tritt auf, wenn sich etwas innerhalb der aktuellen Wiedergabeliste ändert.</span><span class="sxs-lookup"><span data-stu-id="b2868-106">The CurrentPlaylistChange event occurs when something changes within the current playlist.</span></span>

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

## <a name="event-data"></a><span data-ttu-id="b2868-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="b2868-107">Event Data</span></span>

<span data-ttu-id="b2868-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistchangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="b2868-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEventHandler**.</span></span> <span data-ttu-id="b2868-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistchangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="b2868-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="b2868-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2868-110">Property</span></span> | <span data-ttu-id="b2868-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2868-111">Description</span></span>                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2868-112">change (Ändern)</span><span class="sxs-lookup"><span data-stu-id="b2868-112">change</span></span>   | <span data-ttu-id="b2868-113">WMPLib. wmpplaylistchangeeventtypea-Enumerationswert, der den Typ der Änderung angibt, die für die Wiedergabeliste aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b2868-113">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2868-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2868-114">Remarks</span></span>

<span data-ttu-id="b2868-115">Dieses Ereignis tritt nicht auf, wenn eine andere Wiedergabeliste zur aktuellen Wiedergabeliste wird.</span><span class="sxs-lookup"><span data-stu-id="b2868-115">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="b2868-116">Sie tritt nur auf, wenn eine Änderung innerhalb der aktuellen Wiedergabeliste stattfindet, z. b. ein Medien Element, das an die Wiedergabeliste angehängt wird.</span><span class="sxs-lookup"><span data-stu-id="b2868-116">It occurs only when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="b2868-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2868-117">Examples</span></span>

<span data-ttu-id="b2868-118">Im folgenden Beispiel werden die Namen aller Medienelemente in der aktuellen Wiedergabeliste als Reaktion auf das currentplaylistchange-Ereignis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2868-118">The following example displays the names of all the media items in the current playlist in response to the CurrentPlaylistChange Event.</span></span> <span data-ttu-id="b2868-119">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b2868-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


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





## <a name="requirements"></a><span data-ttu-id="b2868-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2868-120">Requirements</span></span>



| <span data-ttu-id="b2868-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2868-121">Requirement</span></span> | <span data-ttu-id="b2868-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b2868-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2868-123">Version</span><span class="sxs-lookup"><span data-stu-id="b2868-123">Version</span></span><br/>   | <span data-ttu-id="b2868-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b2868-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b2868-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2868-125">Namespace</span></span><br/> | <span data-ttu-id="b2868-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b2868-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b2868-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="b2868-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b2868-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b2868-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2868-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2868-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2868-130">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b2868-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b2868-131">**AxWindowsMediaPlayer. currentwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b2868-131">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b2868-132">**AxWindowsMediaPlayer. playlistchange-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b2868-132">**AxWindowsMediaPlayer.PlaylistChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[<span data-ttu-id="b2868-133">**Wmpplaylistchangeeventtype**</span><span class="sxs-lookup"><span data-stu-id="b2868-133">**WMPPlaylistChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





