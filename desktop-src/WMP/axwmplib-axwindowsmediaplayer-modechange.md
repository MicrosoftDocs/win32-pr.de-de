---
title: Modechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das modechange-Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird. | Modechange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Modechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358635"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="0b46b-105">Modechange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="0b46b-105">ModeChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="0b46b-106">Das modechange-Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0b46b-106">The ModeChange event occurs when a mode of Windows Media Player is changed.</span></span>

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a><span data-ttu-id="0b46b-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="0b46b-107">Event Data</span></span>

<span data-ttu-id="0b46b-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ modechangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="0b46b-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEventHandler**.</span></span> <span data-ttu-id="0b46b-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ modechangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0b46b-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="0b46b-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0b46b-110">Property</span></span> | <span data-ttu-id="0b46b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b46b-111">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b46b-112">"Name"</span><span class="sxs-lookup"><span data-stu-id="0b46b-112">modeName</span></span> | <span data-ttu-id="0b46b-113">System. stringindikiert den Modus, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0b46b-113">System.StringIndicates the mode that was changed.</span></span> <span data-ttu-id="0b46b-114">Mögliche Werte finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="0b46b-114">For possible values, see Remarks.</span></span><br/> |
| <span data-ttu-id="0b46b-115">newValue</span><span class="sxs-lookup"><span data-stu-id="0b46b-115">newValue</span></span> | <span data-ttu-id="0b46b-116">System. booleangibt den neuen Zustand des angegebenen Modus an.</span><span class="sxs-lookup"><span data-stu-id="0b46b-116">System.BooleanIndicates the new state of the specified mode.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="0b46b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b46b-117">Remarks</span></span>

<span data-ttu-id="0b46b-118">In der folgenden Tabelle werden die möglichen Werte für die Eigenschaft "mudename" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b46b-118">The following table shows the possible values for the modeName property.</span></span>



| <span data-ttu-id="0b46b-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b46b-119">String</span></span>  | <span data-ttu-id="0b46b-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b46b-120">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="0b46b-121">Shuffle</span><span class="sxs-lookup"><span data-stu-id="0b46b-121">shuffle</span></span> | <span data-ttu-id="0b46b-122">Spuren werden in zufälliger Reihenfolge wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="0b46b-122">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="0b46b-123">loop</span><span class="sxs-lookup"><span data-stu-id="0b46b-123">loop</span></span>    | <span data-ttu-id="0b46b-124">Die gesamte Sequenz von Spuren wird wiederholt wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="0b46b-124">The entire sequence of tracks is played repeatedly.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0b46b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b46b-125">Requirements</span></span>



| <span data-ttu-id="0b46b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b46b-126">Requirement</span></span> | <span data-ttu-id="0b46b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0b46b-127">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b46b-128">Version</span><span class="sxs-lookup"><span data-stu-id="0b46b-128">Version</span></span><br/>   | <span data-ttu-id="0b46b-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0b46b-129">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0b46b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b46b-130">Namespace</span></span><br/> | <span data-ttu-id="0b46b-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0b46b-131">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0b46b-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="0b46b-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0b46b-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0b46b-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b46b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b46b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b46b-135">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0b46b-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b46b-136">**Iwmpsettings. getMode (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0b46b-136">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b46b-137">**Iwmpsettings. SetMode (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0b46b-137">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





