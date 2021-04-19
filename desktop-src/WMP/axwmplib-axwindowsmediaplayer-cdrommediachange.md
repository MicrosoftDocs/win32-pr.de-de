---
title: Cdrommediachange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdrommediachange-Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird. | Cdrommediachange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Cdrommediachange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353415"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f4cb7-105">Cdrommediachange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="f4cb7-105">CdromMediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f4cb7-106">Das **cdrommediachange** -Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f4cb7-106">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a><span data-ttu-id="f4cb7-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="f4cb7-107">Event Data</span></span>

<span data-ttu-id="f4cb7-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdrommediachangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="f4cb7-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEventHandler**.</span></span> <span data-ttu-id="f4cb7-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdrommediachangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="f4cb7-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="f4cb7-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f4cb7-110">Property</span></span> | <span data-ttu-id="f4cb7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4cb7-111">Description</span></span>                                                        |
|----------|--------------------------------------------------------------------|
| <span data-ttu-id="f4cb7-112">Cdromnum</span><span class="sxs-lookup"><span data-stu-id="f4cb7-112">CdromNum</span></span> | <span data-ttu-id="f4cb7-113">System. Int32Specifies der Index des CD-oder DVD-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="f4cb7-113">System.Int32Specifies the index of the CD or DVD drive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4cb7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4cb7-114">Remarks</span></span>

<span data-ttu-id="f4cb7-115">Der Index des CD-Laufwerks entspricht dem Index einer iwmpcdrom-Schnittstelle, auf die über die iwmpcdromcollection-Schnittstelle zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4cb7-115">The index of the CD drive corresponds to the index of an IWMPCdrom interface accessible through the IWMPCdromCollection interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4cb7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4cb7-116">Requirements</span></span>



| <span data-ttu-id="f4cb7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4cb7-117">Requirement</span></span> | <span data-ttu-id="f4cb7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f4cb7-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cb7-119">Version</span><span class="sxs-lookup"><span data-stu-id="f4cb7-119">Version</span></span><br/>   | <span data-ttu-id="f4cb7-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="f4cb7-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f4cb7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4cb7-121">Namespace</span></span><br/> | <span data-ttu-id="f4cb7-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f4cb7-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f4cb7-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="f4cb7-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f4cb7-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f4cb7-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4cb7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4cb7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4cb7-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f4cb7-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4cb7-127">**Iwmpcdrom-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f4cb7-127">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4cb7-128">**Iwmpcdromcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f4cb7-128">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





