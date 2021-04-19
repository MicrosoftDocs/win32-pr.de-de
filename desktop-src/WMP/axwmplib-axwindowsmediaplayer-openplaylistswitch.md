---
title: Openplaylistswitch-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das openplaylistswitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt. | Openplaylistswitch-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Openplaylistswitch-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367589"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a0a37-105">Openplaylistswitch-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="a0a37-105">OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a0a37-106">Das openplaylistswitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.</span><span class="sxs-lookup"><span data-stu-id="a0a37-106">The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.</span></span>

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a><span data-ttu-id="a0a37-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="a0a37-107">Event Data</span></span>

<span data-ttu-id="a0a37-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ openplaylistswitcheventhandler**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEventHandler**.</span></span> <span data-ttu-id="a0a37-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ openplaylistswitchevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="a0a37-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a0a37-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a0a37-110">Property</span></span>  | <span data-ttu-id="a0a37-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0a37-111">Description</span></span>                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a37-112">**pitem**</span><span class="sxs-lookup"><span data-stu-id="a0a37-112">**pItem**</span></span> | <span data-ttu-id="a0a37-113">System. objectobject, das den Titel darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0a37-113">System.ObjectObject representing the title.</span></span> <span data-ttu-id="a0a37-114">Sie können dies in eine iwmpwiedergabe-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a0a37-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0a37-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0a37-115">Requirements</span></span>



| <span data-ttu-id="a0a37-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0a37-116">Requirement</span></span> | <span data-ttu-id="a0a37-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a0a37-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a37-118">Version</span><span class="sxs-lookup"><span data-stu-id="a0a37-118">Version</span></span><br/>   | <span data-ttu-id="a0a37-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a0a37-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a0a37-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0a37-120">Namespace</span></span><br/> | <span data-ttu-id="a0a37-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a0a37-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a0a37-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a0a37-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a0a37-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a0a37-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a37-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0a37-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a37-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a0a37-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a0a37-126">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a0a37-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





