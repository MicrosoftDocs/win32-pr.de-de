---
title: Libraryconnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das libraryconnect-Ereignis tritt auf, wenn eine Bibliothek verfügbar wird.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Libraryconnect-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371720"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b1720-104">Libraryconnect-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="b1720-104">LibraryConnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b1720-105">Das libraryconnect-Ereignis tritt auf, wenn eine Bibliothek verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="b1720-105">The LibraryConnect event occurs when a library becomes available.</span></span>

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a><span data-ttu-id="b1720-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="b1720-106">Event Data</span></span>

<span data-ttu-id="b1720-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ libraryconnecteventhandler**.</span><span class="sxs-lookup"><span data-stu-id="b1720-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEventHandler**.</span></span> <span data-ttu-id="b1720-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ libraryconnectevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="b1720-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="b1720-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b1720-109">Property</span></span> | <span data-ttu-id="b1720-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1720-110">Description</span></span>                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1720-111">plibrary</span><span class="sxs-lookup"><span data-stu-id="b1720-111">pLibrary</span></span> | <span data-ttu-id="b1720-112">**WMPLib. iwmplibrary** Die-Schnittstelle, die die verbundene Bibliothek darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1720-112">**WMPLib.IWMPLibrary** The interface that represents the library that connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1720-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1720-113">Remarks</span></span>

<span data-ttu-id="b1720-114">Dieses Ereignis tritt nicht für die lokale Bibliothek auf.</span><span class="sxs-lookup"><span data-stu-id="b1720-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1720-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1720-115">Requirements</span></span>



| <span data-ttu-id="b1720-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1720-116">Requirement</span></span> | <span data-ttu-id="b1720-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b1720-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1720-118">Version</span><span class="sxs-lookup"><span data-stu-id="b1720-118">Version</span></span><br/>   | <span data-ttu-id="b1720-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="b1720-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="b1720-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1720-120">Namespace</span></span><br/> | <span data-ttu-id="b1720-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b1720-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b1720-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="b1720-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b1720-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b1720-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1720-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1720-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1720-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b1720-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b1720-126">**Iwmplibrary-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b1720-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





