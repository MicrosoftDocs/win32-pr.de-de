---
title: EndOf Stream-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das EndOf Stream-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Endobstream-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365897"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7c58a-104">EndOf Stream-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="7c58a-104">EndOfStream Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7c58a-105">Das EndOf Stream-Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7c58a-105">The EndOfStream event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a><span data-ttu-id="7c58a-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="7c58a-106">Event Data</span></span>

<span data-ttu-id="7c58a-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ EndOf streameventhandler**.</span><span class="sxs-lookup"><span data-stu-id="7c58a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEventHandler**.</span></span> <span data-ttu-id="7c58a-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ endofstreamevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="7c58a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7c58a-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c58a-109">Property</span></span> | <span data-ttu-id="7c58a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c58a-110">Description</span></span>                           |
|----------|---------------------------------------|
| <span data-ttu-id="7c58a-111">result</span><span class="sxs-lookup"><span data-stu-id="7c58a-111">result</span></span>   | <span data-ttu-id="7c58a-112">System. Int32Not wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c58a-112">System.Int32Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c58a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c58a-113">Remarks</span></span>

<span data-ttu-id="7c58a-114">Dieses Ereignis ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7c58a-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c58a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c58a-115">Requirements</span></span>



| <span data-ttu-id="7c58a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c58a-116">Requirement</span></span> | <span data-ttu-id="7c58a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7c58a-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c58a-118">Version</span><span class="sxs-lookup"><span data-stu-id="7c58a-118">Version</span></span><br/>   | <span data-ttu-id="7c58a-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="7c58a-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7c58a-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c58a-120">Namespace</span></span><br/> | <span data-ttu-id="7c58a-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7c58a-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7c58a-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="7c58a-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7c58a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7c58a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c58a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c58a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c58a-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7c58a-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





