---
description: Verwaltet einen verzögerten Vorgang zum Anhalten der app.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Isuspendingdeferral-Schnittstelle (Windows. applicationmodel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348184"
---
# <a name="isuspendingdeferral-interface"></a><span data-ttu-id="5d1ea-103">Isuspendingdeferral-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5d1ea-103">ISuspendingDeferral interface</span></span>

<span data-ttu-id="5d1ea-104">Verwaltet einen verzögerten Vorgang zum Anhalten der app.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-104">Manages a delayed app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="5d1ea-105">Member</span><span class="sxs-lookup"><span data-stu-id="5d1ea-105">Members</span></span>

<span data-ttu-id="5d1ea-106">Die **isuspendingdeferral** -Schnittstelle erbt von [**iinspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="5d1ea-106">The **ISuspendingDeferral** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="5d1ea-107">**Isuspendingdeferral** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5d1ea-107">**ISuspendingDeferral** also has these types of members:</span></span>

-   [<span data-ttu-id="5d1ea-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="5d1ea-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d1ea-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="5d1ea-109">Methods</span></span>

<span data-ttu-id="5d1ea-110">Die **isuspendingdeferral** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-110">The **ISuspendingDeferral** interface has these methods.</span></span>



| <span data-ttu-id="5d1ea-111">Methode</span><span class="sxs-lookup"><span data-stu-id="5d1ea-111">Method</span></span>                                           | <span data-ttu-id="5d1ea-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d1ea-112">Description</span></span>                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d1ea-113">**Abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="5d1ea-113">**Complete**</span></span>](isuspendingdeferral-complete.md) | <span data-ttu-id="5d1ea-114">Benachrichtigt das System, dass die APP Ihre Daten gespeichert hat und bereit ist, angehalten zu werden.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-114">Notifies the system that the app has saved its data and is ready to be suspended.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d1ea-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d1ea-115">Requirements</span></span>



| <span data-ttu-id="5d1ea-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d1ea-116">Requirement</span></span> | <span data-ttu-id="5d1ea-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5d1ea-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d1ea-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d1ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d1ea-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d1ea-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5d1ea-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d1ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d1ea-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d1ea-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d1ea-122">Header</span><span class="sxs-lookup"><span data-stu-id="5d1ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d1ea-123"><dt>Windows. applicationmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d1ea-123"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d1ea-124">IDL</span><span class="sxs-lookup"><span data-stu-id="5d1ea-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d1ea-125"><dt>Windows. applicationmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d1ea-125"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d1ea-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d1ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d1ea-127">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="5d1ea-127">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="5d1ea-128">**Isuspendingeventargs**</span><span class="sxs-lookup"><span data-stu-id="5d1ea-128">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> <dt>

[<span data-ttu-id="5d1ea-129">**Isuspendingoperation**</span><span class="sxs-lookup"><span data-stu-id="5d1ea-129">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 
