---
title: Playlistchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistchange-Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird. | Playlistchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Playlistchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356062"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="21e16-105">Playlistchange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="21e16-105">PlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="21e16-106">Das playlistchange-Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="21e16-106">The PlaylistChange event occurs when a playlist changes.</span></span>

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="21e16-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="21e16-107">Event Data</span></span>

<span data-ttu-id="21e16-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistchangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="21e16-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEventHandler**.</span></span> <span data-ttu-id="21e16-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistchangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="21e16-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="21e16-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="21e16-110">Property</span></span>     | <span data-ttu-id="21e16-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21e16-111">Description</span></span>                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21e16-112">**Abspielen**</span><span class="sxs-lookup"><span data-stu-id="21e16-112">**playlist**</span></span> | <span data-ttu-id="21e16-113">System. objectdas Objekt, das sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="21e16-113">System.ObjectThe object which changed.</span></span> <span data-ttu-id="21e16-114">Sie können dies in eine iwmpwiedergabe-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="21e16-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/>                |
| <span data-ttu-id="21e16-115">**change**</span><span class="sxs-lookup"><span data-stu-id="21e16-115">**change**</span></span>   | <span data-ttu-id="21e16-116">WMPLib. wmpplaylistchangeeventtypea-Enumerationswert, der den Typ der Änderung angibt, die für die Wiedergabeliste aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="21e16-116">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21e16-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21e16-117">Requirements</span></span>



| <span data-ttu-id="21e16-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21e16-118">Requirement</span></span> | <span data-ttu-id="21e16-119">Wert</span><span class="sxs-lookup"><span data-stu-id="21e16-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21e16-120">Version</span><span class="sxs-lookup"><span data-stu-id="21e16-120">Version</span></span><br/>   | <span data-ttu-id="21e16-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="21e16-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="21e16-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="21e16-122">Namespace</span></span><br/> | <span data-ttu-id="21e16-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="21e16-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="21e16-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="21e16-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="21e16-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="21e16-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e16-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21e16-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e16-127">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="21e16-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="21e16-128">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="21e16-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





