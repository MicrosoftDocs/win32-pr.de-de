---
title: Playlistcollectionplaylistadded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistcollectionplaylistadded-Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird. | Playlistcollectionplaylistadded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Playlistcollectionplaylistadded-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352103"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="af4c8-105">Playlistcollectionplaylistadded-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="af4c8-105">PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="af4c8-106">Das playlistcollectionplaylistadded-Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="af4c8-106">The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a><span data-ttu-id="af4c8-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="af4c8-107">Event Data</span></span>

<span data-ttu-id="af4c8-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistaddedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="af4c8-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEventHandler**.</span></span> <span data-ttu-id="af4c8-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistaddedevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="af4c8-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="af4c8-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af4c8-110">Property</span></span>             | <span data-ttu-id="af4c8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af4c8-111">Description</span></span>                                                                |
|----------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="af4c8-112">**bstrauplaylistname**</span><span class="sxs-lookup"><span data-stu-id="af4c8-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="af4c8-113">System. StringGibt den Namen der hinzugefügten Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="af4c8-113">System.StringSpecifies the name of the playlist that was added.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af4c8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af4c8-114">Remarks</span></span>

<span data-ttu-id="af4c8-115">Der Name der hinzugefügten Wiedergabeliste kann verwendet werden, um die entsprechende Wiedergabeliste mithilfe von iwmpplaylistcollection abzurufen. **getByName** -Methode.</span><span class="sxs-lookup"><span data-stu-id="af4c8-115">The name of the playlist that was added can be used to retrieve the corresponding playlist by using the IWMPPlaylistCollection.**getByName** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="af4c8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af4c8-116">Requirements</span></span>



| <span data-ttu-id="af4c8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af4c8-117">Requirement</span></span> | <span data-ttu-id="af4c8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="af4c8-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af4c8-119">Version</span><span class="sxs-lookup"><span data-stu-id="af4c8-119">Version</span></span><br/>   | <span data-ttu-id="af4c8-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="af4c8-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="af4c8-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="af4c8-121">Namespace</span></span><br/> | <span data-ttu-id="af4c8-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="af4c8-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="af4c8-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="af4c8-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="af4c8-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="af4c8-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af4c8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af4c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af4c8-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="af4c8-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af4c8-127">**Iwmpplaylistcollection. getByName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="af4c8-127">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





