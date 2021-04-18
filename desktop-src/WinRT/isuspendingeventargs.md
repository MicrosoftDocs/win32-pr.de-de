---
description: Stellt Daten für ein Ereignis zum Anhalten der APP bereit.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Isuspendingeventargs-Schnittstelle (Windows. applicationmodel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345725"
---
# <a name="isuspendingeventargs-interface"></a><span data-ttu-id="38323-103">Isuspendingeventargs-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="38323-103">ISuspendingEventArgs interface</span></span>

<span data-ttu-id="38323-104">Stellt Daten für ein Ereignis zum Anhalten der APP bereit.</span><span class="sxs-lookup"><span data-stu-id="38323-104">Provides data for an app suspending event.</span></span>

## <a name="members"></a><span data-ttu-id="38323-105">Member</span><span class="sxs-lookup"><span data-stu-id="38323-105">Members</span></span>

<span data-ttu-id="38323-106">Die **isuspendingeventargs** -Schnittstelle erbt von [**iinspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="38323-106">The **ISuspendingEventArgs** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="38323-107">**Isuspendingeventargs** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="38323-107">**ISuspendingEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="38323-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38323-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38323-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="38323-109">Properties</span></span>

<span data-ttu-id="38323-110">Die **isuspendingeventargs** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="38323-110">The **ISuspendingEventArgs** interface has these properties.</span></span>



| <span data-ttu-id="38323-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38323-111">Property</span></span>                                                                           | <span data-ttu-id="38323-112">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="38323-112">Access type</span></span>           | <span data-ttu-id="38323-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38323-113">Description</span></span>                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="38323-114">**Suspendingoperation**</span><span class="sxs-lookup"><span data-stu-id="38323-114">**SuspendingOperation**</span></span>](isuspendingeventargs-suspendingoperation.md)<br/> | <span data-ttu-id="38323-115">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="38323-115">Read/write</span></span><br/> | <span data-ttu-id="38323-116">Ruft den Vorgang zum Anhalten der App ab.</span><span class="sxs-lookup"><span data-stu-id="38323-116">Gets the app suspending operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38323-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38323-117">Remarks</span></span>

<span data-ttu-id="38323-118">Auf dieses Objekt wird zugegriffen, wenn Sie Ereignishandler wie [**suspendingeventhandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**suspendingeventhandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)implementieren und anhalten [**Hinzufügen \_**](/previous-versions//hh438376(v=vs.85)) , um auf App-anhalteereignisse zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="38323-118">This object is accessed when you implement event handlers like [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), and [**add\_Suspending**](/previous-versions//hh438376(v=vs.85)) to respond to app suspending events.</span></span>

## <a name="requirements"></a><span data-ttu-id="38323-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38323-119">Requirements</span></span>



| <span data-ttu-id="38323-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38323-120">Requirement</span></span> | <span data-ttu-id="38323-121">Wert</span><span class="sxs-lookup"><span data-stu-id="38323-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38323-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38323-122">Minimum supported client</span></span><br/> | <span data-ttu-id="38323-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38323-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="38323-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38323-124">Minimum supported server</span></span><br/> | <span data-ttu-id="38323-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38323-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="38323-126">Header</span><span class="sxs-lookup"><span data-stu-id="38323-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="38323-127"><dt>Windows. applicationmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="38323-127"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="38323-128">IDL</span><span class="sxs-lookup"><span data-stu-id="38323-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38323-129"><dt>Windows. applicationmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38323-129"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38323-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38323-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38323-131">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="38323-131">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="38323-132">**Isuspendingoperation**</span><span class="sxs-lookup"><span data-stu-id="38323-132">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> <dt>

[<span data-ttu-id="38323-133">**Isuspendingdeferral**</span><span class="sxs-lookup"><span data-stu-id="38323-133">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 
