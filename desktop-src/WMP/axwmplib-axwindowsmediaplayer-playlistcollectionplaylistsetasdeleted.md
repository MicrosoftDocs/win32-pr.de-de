---
title: Playlistcollectionplaylistsetasdeleted-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistcollectionplaylisteintasdeleted-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Playlistcollectionplaylistsetasdeleted-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358741"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c13b3-104">Playlistcollectionplaylistsetasdeleted-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="c13b3-104">PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c13b3-105">Das playlistcollectionplaylisteintasdeleted-Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="c13b3-105">The PlaylistCollectionPlaylistSetAsDeleted event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a><span data-ttu-id="c13b3-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="c13b3-106">Event Data</span></span>

<span data-ttu-id="c13b3-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistentasdeletedeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="c13b3-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span></span> <span data-ttu-id="c13b3-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistentasdeletedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c13b3-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="c13b3-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c13b3-109">Property</span></span>         | <span data-ttu-id="c13b3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c13b3-110">Description</span></span>                                 |
|------------------|---------------------------------------------|
| <span data-ttu-id="c13b3-111">bstrauplaylistname</span><span class="sxs-lookup"><span data-stu-id="c13b3-111">bstrPlaylistName</span></span> | <span data-ttu-id="c13b3-112">**System. String** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c13b3-112">**System.String** Not supported.</span></span><br/>  |
| <span data-ttu-id="c13b3-113">varfisdeleted</span><span class="sxs-lookup"><span data-stu-id="c13b3-113">varfIsDeleted</span></span>    | <span data-ttu-id="c13b3-114">**System. Boolean** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c13b3-114">**System.Boolean** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c13b3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c13b3-115">Remarks</span></span>

<span data-ttu-id="c13b3-116">Dieses Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="c13b3-116">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="c13b3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c13b3-117">Requirements</span></span>



| <span data-ttu-id="c13b3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c13b3-118">Requirement</span></span> | <span data-ttu-id="c13b3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c13b3-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c13b3-120">Version</span><span class="sxs-lookup"><span data-stu-id="c13b3-120">Version</span></span><br/>   | <span data-ttu-id="c13b3-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c13b3-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c13b3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c13b3-122">Namespace</span></span><br/> | <span data-ttu-id="c13b3-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c13b3-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c13b3-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="c13b3-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c13b3-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c13b3-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c13b3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c13b3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13b3-127">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c13b3-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





