---
title: Stringcollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert. | Stringcollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Stringcollectionchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352015"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="de8c2-105">Stringcollectionchange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="de8c2-105">StringCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="de8c2-106">Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert.</span><span class="sxs-lookup"><span data-stu-id="de8c2-106">The StringCollectionChange event occurs when a string collection changes.</span></span>

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="de8c2-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="de8c2-107">Event Data</span></span>

<span data-ttu-id="de8c2-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ stringcollectionchangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="de8c2-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEventHandler**.</span></span> <span data-ttu-id="de8c2-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ stringcollectionchangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="de8c2-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="de8c2-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="de8c2-110">Property</span></span>              | <span data-ttu-id="de8c2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de8c2-111">Description</span></span>                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de8c2-112">pdispstringcollection</span><span class="sxs-lookup"><span data-stu-id="de8c2-112">pdispStringCollection</span></span> | <span data-ttu-id="de8c2-113">System. objectdas Zeichen folgen Auflistungs Element, das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="de8c2-113">System.ObjectThe string collection item that changed.</span></span> <span data-ttu-id="de8c2-114">Sie können dies in eine iwmpstringcollection-Schnittstelle umwandeln, um darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="de8c2-114">You can cast this to an IWMPStringCollection interface to access it.</span></span><br/> |
| <span data-ttu-id="de8c2-115">lcollectionindex</span><span class="sxs-lookup"><span data-stu-id="de8c2-115">lCollectionIndex</span></span>      | <span data-ttu-id="de8c2-116">System. Int32The-Index des Elements der Zeichen folgen Auflistung, das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="de8c2-116">System.Int32The index of the string collection item that changed.</span></span><br/>                                                          |
| <span data-ttu-id="de8c2-117">change (Ändern)</span><span class="sxs-lookup"><span data-stu-id="de8c2-117">change</span></span>                | <span data-ttu-id="de8c2-118">WMPLib. wmpstringcollectionchangeeventtypea-Enumerationswert, der den Typ der aufgetretenen Änderung angibt.</span><span class="sxs-lookup"><span data-stu-id="de8c2-118">WMPLib.WMPStringCollectionChangeEventTypeAn enumeration value indicating the type of change that occurred.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="de8c2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de8c2-119">Requirements</span></span>



| <span data-ttu-id="de8c2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de8c2-120">Requirement</span></span> | <span data-ttu-id="de8c2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="de8c2-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de8c2-122">Version</span><span class="sxs-lookup"><span data-stu-id="de8c2-122">Version</span></span><br/>   | <span data-ttu-id="de8c2-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="de8c2-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="de8c2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="de8c2-124">Namespace</span></span><br/> | <span data-ttu-id="de8c2-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="de8c2-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="de8c2-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="de8c2-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="de8c2-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="de8c2-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de8c2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de8c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8c2-129">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="de8c2-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="de8c2-130">**Iwmpstringcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="de8c2-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="de8c2-131">**Wmpstringcollectionchangeeventtype**</span><span class="sxs-lookup"><span data-stu-id="de8c2-131">**WMPStringCollectionChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





