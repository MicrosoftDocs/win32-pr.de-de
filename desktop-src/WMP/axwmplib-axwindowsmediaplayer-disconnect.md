---
title: Disconnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Disconnect-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Disconnect-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358275"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="5babd-104">Disconnect-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="5babd-104">Disconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="5babd-105">Das Disconnect-Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5babd-105">The Disconnect event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a><span data-ttu-id="5babd-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="5babd-106">Event Data</span></span>

<span data-ttu-id="5babd-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ disconnecteventhandler**.</span><span class="sxs-lookup"><span data-stu-id="5babd-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEventHandler**.</span></span> <span data-ttu-id="5babd-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ disconnectevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="5babd-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="5babd-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5babd-109">Property</span></span> | <span data-ttu-id="5babd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5babd-110">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="5babd-111">result</span><span class="sxs-lookup"><span data-stu-id="5babd-111">result</span></span>   | <span data-ttu-id="5babd-112">**System. Int32** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5babd-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5babd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5babd-113">Remarks</span></span>

<span data-ttu-id="5babd-114">Dieses Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5babd-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="5babd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5babd-115">Requirements</span></span>



| <span data-ttu-id="5babd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5babd-116">Requirement</span></span> | <span data-ttu-id="5babd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5babd-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5babd-118">Version</span><span class="sxs-lookup"><span data-stu-id="5babd-118">Version</span></span><br/>   | <span data-ttu-id="5babd-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="5babd-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5babd-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="5babd-120">Namespace</span></span><br/> | <span data-ttu-id="5babd-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="5babd-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5babd-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="5babd-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5babd-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5babd-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5babd-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5babd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5babd-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="5babd-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





