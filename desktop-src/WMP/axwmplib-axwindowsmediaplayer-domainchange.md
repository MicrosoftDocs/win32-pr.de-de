---
title: Domainchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das domainchange-Ereignis tritt auf, wenn die DVD-Domäne geändert wird. | Domainchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Das domainchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360979"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ec67b-105">Domainchange-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="ec67b-105">DomainChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ec67b-106">Das domainchange-Ereignis tritt auf, wenn die DVD-Domäne geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ec67b-106">The DomainChange event occurs when the DVD domain changes.</span></span>

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a><span data-ttu-id="ec67b-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="ec67b-107">Event Data</span></span>

<span data-ttu-id="ec67b-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ domainchangeeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="ec67b-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEventHandler**.</span></span> <span data-ttu-id="ec67b-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ domainchangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="ec67b-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="ec67b-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec67b-110">Property</span></span>  | <span data-ttu-id="ec67b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec67b-111">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec67b-112">Domäne</span><span class="sxs-lookup"><span data-stu-id="ec67b-112">strDomain</span></span> | <span data-ttu-id="ec67b-113">System. stringindikiert die neue Domäne.</span><span class="sxs-lookup"><span data-stu-id="ec67b-113">System.StringIndicates the new domain.</span></span> <span data-ttu-id="ec67b-114">Mögliche Werte finden Sie im Abschnitt „Hinweise“.</span><span class="sxs-lookup"><span data-stu-id="ec67b-114">For possible values, see the Remarks section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec67b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec67b-115">Remarks</span></span>

<span data-ttu-id="ec67b-116">In der folgenden Tabelle sind die möglichen Werte für die Eigenschaft "Eigenschaft" (Eigenschaft) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec67b-116">The following table shows the possible values for the strDomain property.</span></span>



| <span data-ttu-id="ec67b-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ec67b-117">String</span></span>            | <span data-ttu-id="ec67b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec67b-118">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="ec67b-119">FirstPlay</span><span class="sxs-lookup"><span data-stu-id="ec67b-119">firstPlay</span></span>         | <span data-ttu-id="ec67b-120">Die Standard Initialisierung einer DVD-CD wird durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec67b-120">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="ec67b-121">videomanagermenu</span><span class="sxs-lookup"><span data-stu-id="ec67b-121">videoManagerMenu</span></span>  | <span data-ttu-id="ec67b-122">Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "Root Menu" oder "topmenu" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ec67b-122">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="ec67b-123">videotitlesetmenu</span><span class="sxs-lookup"><span data-stu-id="ec67b-123">videoTitleSetMenu</span></span> | <span data-ttu-id="ec67b-124">Anzeigen von Menüs für den aktuellen Titel Satz.</span><span class="sxs-lookup"><span data-stu-id="ec67b-124">Displaying menus for current title set.</span></span> <span data-ttu-id="ec67b-125">Wird auch als titlemenu bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ec67b-125">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="ec67b-126">title</span><span class="sxs-lookup"><span data-stu-id="ec67b-126">title</span></span>             | <span data-ttu-id="ec67b-127">Anzeigen des aktuellen Titels.</span><span class="sxs-lookup"><span data-stu-id="ec67b-127">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="ec67b-128">stop</span><span class="sxs-lookup"><span data-stu-id="ec67b-128">stop</span></span>              | <span data-ttu-id="ec67b-129">Der DVD-Navigator befindet sich in der DVD-stoppdomäne.</span><span class="sxs-lookup"><span data-stu-id="ec67b-129">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

## <a name="requirements"></a><span data-ttu-id="ec67b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec67b-130">Requirements</span></span>



| <span data-ttu-id="ec67b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec67b-131">Requirement</span></span> | <span data-ttu-id="ec67b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ec67b-132">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec67b-133">Version</span><span class="sxs-lookup"><span data-stu-id="ec67b-133">Version</span></span><br/>   | <span data-ttu-id="ec67b-134">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ec67b-134">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ec67b-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec67b-135">Namespace</span></span><br/> | <span data-ttu-id="ec67b-136">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ec67b-136">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ec67b-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="ec67b-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ec67b-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ec67b-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec67b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec67b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec67b-140">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ec67b-140">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ec67b-141">**Iwmpdvd-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ec67b-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





