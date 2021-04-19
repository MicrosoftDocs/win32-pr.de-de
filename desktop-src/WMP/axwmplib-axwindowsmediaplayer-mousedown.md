---
title: MouseDown-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MouseDown-Ereignis tritt auf, wenn der Benutzer eine Maustaste drückt. | MouseDown-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 3dfbd034-67d4-4b7e-88d8-a77d301c5df7
keywords:
- MouseDown-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MouseDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0779df27f406691903a0362c9eb3a1df993f595f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370293"
---
# <a name="mousedown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="1db6f-105">MouseDown-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="1db6f-105">MouseDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="1db6f-106">Das MouseDown-Ereignis tritt auf, wenn der Benutzer eine Maustaste drückt.</span><span class="sxs-lookup"><span data-stu-id="1db6f-106">The MouseDown event occurs when the user presses a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseDownEvent(
  object sender,
  _WMPOCXEvents_MouseDownEvent e
)

[Visual Basic]
Private Sub player_MouseDownEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseDownEvent
) Handles player.MouseDownEvent
```

## <a name="event-data"></a><span data-ttu-id="1db6f-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="1db6f-107">Event Data</span></span>

<span data-ttu-id="1db6f-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mousdownetventhandler**.</span><span class="sxs-lookup"><span data-stu-id="1db6f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEventHandler**.</span></span> <span data-ttu-id="1db6f-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ moussdowmavent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1db6f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="1db6f-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1db6f-110">Property</span></span>    | <span data-ttu-id="1db6f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1db6f-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db6f-112">nschaltfläche</span><span class="sxs-lookup"><span data-stu-id="1db6f-112">nButton</span></span>     | <span data-ttu-id="1db6f-113">System. Int16A Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1db6f-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="1db6f-114">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="1db6f-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1db6f-115">Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="1db6f-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="1db6f-116">nshiftstate</span><span class="sxs-lookup"><span data-stu-id="1db6f-116">nShiftState</span></span> | <span data-ttu-id="1db6f-117">System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1db6f-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="1db6f-118">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="1db6f-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1db6f-119">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="1db6f-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="1db6f-120">Designer</span><span class="sxs-lookup"><span data-stu-id="1db6f-120">fX</span></span>          | <span data-ttu-id="1db6f-121">System. Int32The x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="1db6f-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="1db6f-122">herrlichen</span><span class="sxs-lookup"><span data-stu-id="1db6f-122">fY</span></span>          | <span data-ttu-id="1db6f-123">System. Int32The y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="1db6f-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="1db6f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1db6f-124">Requirements</span></span>



| <span data-ttu-id="1db6f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1db6f-125">Requirement</span></span> | <span data-ttu-id="1db6f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1db6f-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db6f-127">Version</span><span class="sxs-lookup"><span data-stu-id="1db6f-127">Version</span></span><br/>   | <span data-ttu-id="1db6f-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="1db6f-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1db6f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1db6f-129">Namespace</span></span><br/> | <span data-ttu-id="1db6f-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1db6f-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1db6f-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="1db6f-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1db6f-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1db6f-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1db6f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1db6f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db6f-134">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1db6f-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





