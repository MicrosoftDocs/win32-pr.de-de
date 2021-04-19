---
title: MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MouseUp-Ereignis tritt auf, wenn der Benutzer eine Maustaste loslässt. | MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- Das MouseUp-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361555"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c5714-105">MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="c5714-105">MouseUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c5714-106">Das MouseUp-Ereignis tritt auf, wenn der Benutzer eine Maustaste loslässt.</span><span class="sxs-lookup"><span data-stu-id="c5714-106">The MouseUp event occurs when the user releases a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a><span data-ttu-id="c5714-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="c5714-107">Event Data</span></span>

<span data-ttu-id="c5714-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mouseupeer-thandler**.</span><span class="sxs-lookup"><span data-stu-id="c5714-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEventHandler**.</span></span> <span data-ttu-id="c5714-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mouseupeer Vent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c5714-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="c5714-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5714-110">Property</span></span>    | <span data-ttu-id="c5714-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5714-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5714-112">nschaltfläche</span><span class="sxs-lookup"><span data-stu-id="c5714-112">nButton</span></span>     | <span data-ttu-id="c5714-113">System. Int16A Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c5714-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="c5714-114">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="c5714-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="c5714-115">Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="c5714-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="c5714-116">nshiftstate</span><span class="sxs-lookup"><span data-stu-id="c5714-116">nShiftState</span></span> | <span data-ttu-id="c5714-117">System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c5714-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="c5714-118">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="c5714-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="c5714-119">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="c5714-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="c5714-120">Designer</span><span class="sxs-lookup"><span data-stu-id="c5714-120">fX</span></span>          | <span data-ttu-id="c5714-121">System. Int32The x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c5714-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="c5714-122">herrlichen</span><span class="sxs-lookup"><span data-stu-id="c5714-122">fY</span></span>          | <span data-ttu-id="c5714-123">System. Int32The y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c5714-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="c5714-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5714-124">Requirements</span></span>



| <span data-ttu-id="c5714-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5714-125">Requirement</span></span> | <span data-ttu-id="c5714-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c5714-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5714-127">Version</span><span class="sxs-lookup"><span data-stu-id="c5714-127">Version</span></span><br/>   | <span data-ttu-id="c5714-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c5714-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c5714-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5714-129">Namespace</span></span><br/> | <span data-ttu-id="c5714-130">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c5714-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c5714-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="c5714-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c5714-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c5714-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5714-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5714-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5714-134">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c5714-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





