---
title: Folderscanstatechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das folderscanstatechange-Ereignis tritt auf, wenn sich der Status einer Ordner Überwachung ändert.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Folderscanstatechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371973"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="1d75b-104">Folderscanstatechange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="1d75b-104">FolderScanStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="1d75b-105">Das folderscanstatechange-Ereignis tritt auf, wenn sich der Status einer Ordner Überwachung ändert.</span><span class="sxs-lookup"><span data-stu-id="1d75b-105">The FolderScanStateChange event occurs when a folder monitoring operation changes state.</span></span>

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a><span data-ttu-id="1d75b-106">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="1d75b-106">Event Data</span></span>

<span data-ttu-id="1d75b-107">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ folderscanstatechangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="1d75b-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEventHandler**.</span></span> <span data-ttu-id="1d75b-108">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ folderscanstatechangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="1d75b-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="1d75b-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1d75b-109">Property</span></span> | <span data-ttu-id="1d75b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d75b-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d75b-111">wmpfss</span><span class="sxs-lookup"><span data-stu-id="1d75b-111">wmpfss</span></span>   | <span data-ttu-id="1d75b-112">WMPLib. wmpfolderscanstateder Enumerationswert, der den neuen Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="1d75b-112">WMPLib.WMPFolderScanStateThe enumeration value that indicates the new state.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1d75b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d75b-113">Requirements</span></span>



| <span data-ttu-id="1d75b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d75b-114">Requirement</span></span> | <span data-ttu-id="1d75b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1d75b-115">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d75b-116">Version</span><span class="sxs-lookup"><span data-stu-id="1d75b-116">Version</span></span><br/>   | <span data-ttu-id="1d75b-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="1d75b-117">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="1d75b-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d75b-118">Namespace</span></span><br/> | <span data-ttu-id="1d75b-119">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1d75b-119">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1d75b-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="1d75b-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d75b-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1d75b-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d75b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d75b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d75b-123">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="1d75b-123">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d75b-124">**Wmpfolderscanstate**</span><span class="sxs-lookup"><span data-stu-id="1d75b-124">**WMPFolderScanState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





