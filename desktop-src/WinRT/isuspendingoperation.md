---
description: Enthält Informationen über eine APP, die den Vorgang angehalten.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Isuspendingoperation-Schnittstelle (Windows. applicationmodel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526222"
---
# <a name="isuspendingoperation-interface"></a><span data-ttu-id="a25a8-103">Isuspendingoperation-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a25a8-103">ISuspendingOperation interface</span></span>

<span data-ttu-id="a25a8-104">Enthält Informationen über eine APP, die den Vorgang angehalten.</span><span class="sxs-lookup"><span data-stu-id="a25a8-104">Provides information about an app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="a25a8-105">Member</span><span class="sxs-lookup"><span data-stu-id="a25a8-105">Members</span></span>

<span data-ttu-id="a25a8-106">Die **isuspendingoperation** -Schnittstelle erbt von [**iinspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="a25a8-106">The **ISuspendingOperation** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="a25a8-107">**Isuspendingoperation** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a25a8-107">**ISuspendingOperation** also has these types of members:</span></span>

-   [<span data-ttu-id="a25a8-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="a25a8-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="a25a8-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a25a8-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a25a8-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="a25a8-110">Methods</span></span>

<span data-ttu-id="a25a8-111">Die **isuspendingoperation** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a25a8-111">The **ISuspendingOperation** interface has these methods.</span></span>



| <span data-ttu-id="a25a8-112">Methode</span><span class="sxs-lookup"><span data-stu-id="a25a8-112">Method</span></span>                                                  | <span data-ttu-id="a25a8-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a25a8-113">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="a25a8-114">**GetDeferral**</span><span class="sxs-lookup"><span data-stu-id="a25a8-114">**GetDeferral**</span></span>](isuspendingoperation-getdeferral.md) | <span data-ttu-id="a25a8-115">Fordert an, dass der Vorgang zum Anhalten der APP verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="a25a8-115">Requests that the app suspending operation be delayed.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a25a8-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a25a8-116">Properties</span></span>

<span data-ttu-id="a25a8-117">Die **isuspendingoperation** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a25a8-117">The **ISuspendingOperation** interface has these properties.</span></span>



| <span data-ttu-id="a25a8-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a25a8-118">Property</span></span>                                                     | <span data-ttu-id="a25a8-119">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a25a8-119">Access type</span></span>           | <span data-ttu-id="a25a8-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a25a8-120">Description</span></span>                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a25a8-121">**Stichtag**</span><span class="sxs-lookup"><span data-stu-id="a25a8-121">**Deadline**</span></span>](isuspendingoperation-deadline.md)<br/> | <span data-ttu-id="a25a8-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a25a8-122">Read/write</span></span><br/> | <span data-ttu-id="a25a8-123">Ruft die verbleibende Zeit ab, bevor eine verzögerte App angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="a25a8-123">Gets the time remaining before a delayed app suspending operation continues.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a25a8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a25a8-124">Requirements</span></span>



| <span data-ttu-id="a25a8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a25a8-125">Requirement</span></span> | <span data-ttu-id="a25a8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a25a8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a25a8-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a25a8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a25a8-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a25a8-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a25a8-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a25a8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a25a8-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a25a8-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a25a8-131">Header</span><span class="sxs-lookup"><span data-stu-id="a25a8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a25a8-132"><dt>Windows. applicationmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="a25a8-132"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="a25a8-133">IDL</span><span class="sxs-lookup"><span data-stu-id="a25a8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a25a8-134"><dt>Windows. applicationmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a25a8-134"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a25a8-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a25a8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a25a8-136">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="a25a8-136">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="a25a8-137">**Isuspendingdeferral**</span><span class="sxs-lookup"><span data-stu-id="a25a8-137">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> <dt>

[<span data-ttu-id="a25a8-138">**Isuspendingeventargs**</span><span class="sxs-lookup"><span data-stu-id="a25a8-138">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 
