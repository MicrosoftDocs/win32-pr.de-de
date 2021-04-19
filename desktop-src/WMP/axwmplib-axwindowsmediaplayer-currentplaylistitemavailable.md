---
title: Currentplaylistitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das currentplaylistitemavailable-Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird. | Currentplaylistitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Currentplaylistitemavailable-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350755"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3c954-105">Currentplaylistitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="3c954-105">CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3c954-106">Das currentplaylistitemavailable-Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="3c954-106">The CurrentPlaylistItemAvailable event occurs when the current playlist becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="3c954-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="3c954-107">Event Data</span></span>

<span data-ttu-id="3c954-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistitemavailableeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="3c954-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEventHandler**.</span></span> <span data-ttu-id="3c954-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistitemavailableevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="3c954-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3c954-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3c954-110">Property</span></span>         | <span data-ttu-id="3c954-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c954-111">Description</span></span>                                                    |
|------------------|----------------------------------------------------------------|
| <span data-ttu-id="3c954-112">**bstritemname**</span><span class="sxs-lookup"><span data-stu-id="3c954-112">**bstrItemName**</span></span> | <span data-ttu-id="3c954-113">System. stringder Name des aktuellen Wiedergabelisten Elements.</span><span class="sxs-lookup"><span data-stu-id="3c954-113">System.StringThe name of the current playlist item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c954-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c954-114">Remarks</span></span>

<span data-ttu-id="3c954-115">Der Name der aktuellen Wiedergabeliste kann verwendet werden, um die entsprechende **iwmpwiedergabe** -Schnittstelle von der iwmpplaylistarray-Schnittstelle abzurufen, die von der iwmpplaylistcollection. getByName-Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3c954-115">The name of the current playlist can be used to retrieve the corresponding **IWMPPlaylist** interface from the IWMPPlaylistArray interface that is returned from the IWMPPlaylistCollection.getByName method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c954-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c954-116">Requirements</span></span>



| <span data-ttu-id="3c954-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c954-117">Requirement</span></span> | <span data-ttu-id="3c954-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3c954-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c954-119">Version</span><span class="sxs-lookup"><span data-stu-id="3c954-119">Version</span></span><br/>   | <span data-ttu-id="3c954-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="3c954-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3c954-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c954-121">Namespace</span></span><br/> | <span data-ttu-id="3c954-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3c954-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3c954-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="3c954-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3c954-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3c954-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c954-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c954-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c954-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3c954-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c954-127">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3c954-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c954-128">**Iwmpplaylistarray-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3c954-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c954-129">**Iwmpplaylistcollection. getByName (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3c954-129">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





