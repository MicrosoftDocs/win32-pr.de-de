---
title: Librarydisconnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das librarydisconnect-Ereignis tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Librarydisconnect-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373944"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="91b23-104">Librarydisconnect-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="91b23-104">LibraryDisconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="91b23-105">Das librarydisconnect-Ereignis tritt auf, wenn eine Bibliothek nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="91b23-105">The LibraryDisconnect event occurs when a library is no longer available.</span></span>

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a><span data-ttu-id="91b23-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="91b23-106">Event Data</span></span>

<span data-ttu-id="91b23-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ librarydisconnecteventhandler**.</span><span class="sxs-lookup"><span data-stu-id="91b23-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEventHandler**.</span></span> <span data-ttu-id="91b23-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ librarydisconnectevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="91b23-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="91b23-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="91b23-109">Property</span></span> | <span data-ttu-id="91b23-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91b23-110">Description</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b23-111">plibrary</span><span class="sxs-lookup"><span data-stu-id="91b23-111">pLibrary</span></span> | <span data-ttu-id="91b23-112">**WMPLib. iwmplibrary** Die-Schnittstelle, die die getrennte Bibliothek darstellt.</span><span class="sxs-lookup"><span data-stu-id="91b23-112">**WMPLib.IWMPLibrary** The interface that represents the library that disconnected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91b23-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91b23-113">Remarks</span></span>

<span data-ttu-id="91b23-114">Dieses Ereignis tritt nicht für die lokale Bibliothek auf.</span><span class="sxs-lookup"><span data-stu-id="91b23-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="91b23-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91b23-115">Requirements</span></span>



| <span data-ttu-id="91b23-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91b23-116">Requirement</span></span> | <span data-ttu-id="91b23-117">Wert</span><span class="sxs-lookup"><span data-stu-id="91b23-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b23-118">Version</span><span class="sxs-lookup"><span data-stu-id="91b23-118">Version</span></span><br/>   | <span data-ttu-id="91b23-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="91b23-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="91b23-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="91b23-120">Namespace</span></span><br/> | <span data-ttu-id="91b23-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="91b23-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="91b23-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="91b23-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="91b23-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="91b23-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b23-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91b23-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b23-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="91b23-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="91b23-126">**Iwmplibrary-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="91b23-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





