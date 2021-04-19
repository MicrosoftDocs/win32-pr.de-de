---
title: Cdromripmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdromripmediaerror-Ereignis tritt auf, wenn ein Fehler auftritt, während ein einzelner Track-Vorgang von einer CD durchgeführt wird.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Cdromripmediaerror-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367510"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="21139-104">Cdromripmediaerror-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="21139-104">CdromRipMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="21139-105">Das cdromripmediaerror-Ereignis tritt auf, wenn ein Fehler auftritt, während ein einzelner Track-Vorgang von einer CD durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21139-105">The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.</span></span>

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a><span data-ttu-id="21139-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="21139-106">Event Data</span></span>

<span data-ttu-id="21139-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripmediaerroreventhandler**.</span><span class="sxs-lookup"><span data-stu-id="21139-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEventHandler**.</span></span> <span data-ttu-id="21139-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdromripmediaerrorevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="21139-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="21139-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="21139-109">Property</span></span>  | <span data-ttu-id="21139-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21139-110">Description</span></span>                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21139-111">pcdromrip</span><span class="sxs-lookup"><span data-stu-id="21139-111">pCdromRip</span></span> | <span data-ttu-id="21139-112">WMPLib. iwmpcdromripdie Schnittstelle, die den einreißen-Vorgang darstellt, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="21139-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/>                |
| <span data-ttu-id="21139-113">pmedia</span><span class="sxs-lookup"><span data-stu-id="21139-113">pMedia</span></span>    | <span data-ttu-id="21139-114">System. objectdas Medien Element, das den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="21139-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="21139-115">Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="21139-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21139-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21139-116">Requirements</span></span>



| <span data-ttu-id="21139-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21139-117">Requirement</span></span> | <span data-ttu-id="21139-118">Wert</span><span class="sxs-lookup"><span data-stu-id="21139-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21139-119">Version</span><span class="sxs-lookup"><span data-stu-id="21139-119">Version</span></span><br/>   | <span data-ttu-id="21139-120">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="21139-120">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="21139-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="21139-121">Namespace</span></span><br/> | <span data-ttu-id="21139-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="21139-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="21139-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="21139-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="21139-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="21139-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21139-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21139-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21139-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="21139-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="21139-127">**Iwmpcdromrip-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="21139-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="21139-128">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="21139-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





