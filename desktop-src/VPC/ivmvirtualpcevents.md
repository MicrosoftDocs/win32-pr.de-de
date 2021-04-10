---
title: Ivmvirtualpcevents-Schnittstelle (vpccominterfaces. h)
description: Definiert die ausgehende Ereignis Schnittstelle für die ivmvirtualpc-Schnittstelle.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Ivmvirtualpcevents Interface Virtual PC
- Virtueller Computer für ivmvirtualpcevents Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040849"
---
# <a name="ivmvirtualpcevents-interface"></a><span data-ttu-id="e61ef-105">Ivmvirtualpcevents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e61ef-105">IVMVirtualPCEvents interface</span></span>

<span data-ttu-id="e61ef-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e61ef-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e61ef-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e61ef-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e61ef-108">Definiert die ausgehende Ereignis Schnittstelle für die [**ivmvirtualpc**](ivmvirtualpc.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e61ef-108">Defines the outgoing event interface for the [**IVMVirtualPC**](ivmvirtualpc.md) interface.</span></span> <span data-ttu-id="e61ef-109">Der Client implementiert diese Methoden, um von [**ivmvirtualpc**](ivmvirtualpc.md)gesendete Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e61ef-109">The client implements these methods to receive events sent from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="members"></a><span data-ttu-id="e61ef-110">Member</span><span class="sxs-lookup"><span data-stu-id="e61ef-110">Members</span></span>

<span data-ttu-id="e61ef-111">Die **ivmvirtualpcevents** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e61ef-111">The **IVMVirtualPCEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e61ef-112">**Ivmvirtualpcevents** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e61ef-112">**IVMVirtualPCEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="e61ef-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="e61ef-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e61ef-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="e61ef-114">Methods</span></span>

<span data-ttu-id="e61ef-115">Die **ivmvirtualpcevents** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e61ef-115">The **IVMVirtualPCEvents** interface has these methods.</span></span>



| <span data-ttu-id="e61ef-116">Methode</span><span class="sxs-lookup"><span data-stu-id="e61ef-116">Method</span></span>                                                        | <span data-ttu-id="e61ef-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e61ef-117">Description</span></span>                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="e61ef-118">**Oneventprotokolliert**</span><span class="sxs-lookup"><span data-stu-id="e61ef-118">**OnEventLogged**</span></span>](ivmvirtualpcevents-oneventlogged.md)     | <span data-ttu-id="e61ef-119">Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="e61ef-119">Receives notification that Windows Virtual PC logs an event.</span></span><br/>      |
| [<span data-ttu-id="e61ef-120">**Onvmstatechange**</span><span class="sxs-lookup"><span data-stu-id="e61ef-120">**OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md) | <span data-ttu-id="e61ef-121">Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e61ef-121">Receives notification that a virtual machine's state has changed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e61ef-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e61ef-122">Requirements</span></span>



| <span data-ttu-id="e61ef-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e61ef-123">Requirement</span></span> | <span data-ttu-id="e61ef-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e61ef-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e61ef-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e61ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e61ef-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e61ef-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e61ef-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e61ef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e61ef-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e61ef-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e61ef-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e61ef-129">End of client support</span></span><br/>    | <span data-ttu-id="e61ef-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e61ef-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e61ef-131">Produkt</span><span class="sxs-lookup"><span data-stu-id="e61ef-131">Product</span></span><br/>                  | <span data-ttu-id="e61ef-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e61ef-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e61ef-133">Header</span><span class="sxs-lookup"><span data-stu-id="e61ef-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e61ef-134"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e61ef-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e61ef-135">IID</span><span class="sxs-lookup"><span data-stu-id="e61ef-135">IID</span></span><br/>                      | <span data-ttu-id="e61ef-136">Diid \_ ivmvirtualpcevents ist als efed1ef1-3c09-41f7-a9c2-7e29fa286c9d definiert.</span><span class="sxs-lookup"><span data-stu-id="e61ef-136">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



 

