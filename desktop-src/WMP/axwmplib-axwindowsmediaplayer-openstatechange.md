---
title: OpenStateChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das OpenStateChange-Ereignis tritt auf, wenn die openstate-Eigenschaft den Wert ändert. | OpenStateChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- OpenStateChange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369547"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="96a51-105">OpenStateChange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="96a51-105">OpenStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="96a51-106">Das OpenStateChange-Ereignis tritt auf, wenn die **openstate** -Eigenschaft den Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="96a51-106">The OpenStateChange event occurs when the **openState** property changes value.</span></span>

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a><span data-ttu-id="96a51-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="96a51-107">Event Data</span></span>

<span data-ttu-id="96a51-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ openstatechangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="96a51-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEventHandler**.</span></span> <span data-ttu-id="96a51-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ openstatechangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="96a51-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="96a51-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="96a51-110">Property</span></span> | <span data-ttu-id="96a51-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96a51-111">Description</span></span>                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a51-112">NewState</span><span class="sxs-lookup"><span data-stu-id="96a51-112">NewState</span></span> | <span data-ttu-id="96a51-113">System. Int32Specifies der neue offene Zustand.</span><span class="sxs-lookup"><span data-stu-id="96a51-113">System.Int32Specifies the new open state.</span></span> <span data-ttu-id="96a51-114">Eine Tabelle mit Werten finden Sie unter [openstate](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="96a51-114">For a table of values, see [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96a51-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96a51-115">Remarks</span></span>

<span data-ttu-id="96a51-116">Windows-Media Player können mehrere offene Zustände durchlaufen, während versucht wird, eine Netzwerkdatei zu öffnen, z. b. das Auffinden des Servers, das Herstellen einer Verbindung mit dem Server und schließlich das Öffnen der Datei.</span><span class="sxs-lookup"><span data-stu-id="96a51-116">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="96a51-117">Dieses Ereignis wird jedes Mal ausgelöst, wenn sich der Status des geöffneten Zustands ändert.</span><span class="sxs-lookup"><span data-stu-id="96a51-117">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="96a51-118">Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="96a51-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="96a51-119">Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf.</span><span class="sxs-lookup"><span data-stu-id="96a51-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="96a51-120">Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="96a51-120">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a51-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96a51-121">Requirements</span></span>



| <span data-ttu-id="96a51-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96a51-122">Requirement</span></span> | <span data-ttu-id="96a51-123">Wert</span><span class="sxs-lookup"><span data-stu-id="96a51-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a51-124">Version</span><span class="sxs-lookup"><span data-stu-id="96a51-124">Version</span></span><br/>   | <span data-ttu-id="96a51-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="96a51-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="96a51-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="96a51-126">Namespace</span></span><br/> | <span data-ttu-id="96a51-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="96a51-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="96a51-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="96a51-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="96a51-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="96a51-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a51-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96a51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a51-131">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="96a51-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="96a51-132">**AxWindowsMediaPlayer. openstate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="96a51-132">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





