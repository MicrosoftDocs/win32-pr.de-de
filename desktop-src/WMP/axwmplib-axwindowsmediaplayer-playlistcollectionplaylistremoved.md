---
title: Playlistcollectionplaylistrebewegungs-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistcollectionplaylistrebewegungs-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird. | Playlistcollectionplaylistrebewegungs-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Playlistcollectionplaylistrebewegungsereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361686"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="23faf-105">Playlistcollectionplaylistrebewegungs-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="23faf-105">PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="23faf-106">Das playlistcollectionplaylistrebewegungs-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="23faf-106">The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a><span data-ttu-id="23faf-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="23faf-107">Event Data</span></span>

<span data-ttu-id="23faf-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistremuvedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="23faf-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEventHandler**.</span></span> <span data-ttu-id="23faf-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistremuvedevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="23faf-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="23faf-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="23faf-110">Property</span></span>             | <span data-ttu-id="23faf-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23faf-111">Description</span></span>                                                                  |
|----------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="23faf-112">**bstrauplaylistname**</span><span class="sxs-lookup"><span data-stu-id="23faf-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="23faf-113">System. StringGibt den Namen der Wiedergabeliste an, die entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="23faf-113">System.StringSpecifies the name of the playlist that was removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="23faf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23faf-114">Requirements</span></span>



| <span data-ttu-id="23faf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23faf-115">Requirement</span></span> | <span data-ttu-id="23faf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="23faf-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23faf-117">Version</span><span class="sxs-lookup"><span data-stu-id="23faf-117">Version</span></span><br/>   | <span data-ttu-id="23faf-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="23faf-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="23faf-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="23faf-119">Namespace</span></span><br/> | <span data-ttu-id="23faf-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="23faf-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="23faf-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="23faf-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="23faf-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="23faf-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23faf-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23faf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23faf-124">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="23faf-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="23faf-125">**Iwmpplaylistcollection. getByName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="23faf-125">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





