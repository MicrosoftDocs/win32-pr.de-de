---
title: Ivmaccountant-Schnittstelle (vpccominterfaces. h)
description: Ermöglicht den Zugriff auf Buchhaltungs bezogene Informationen für einen virtuellen Computer.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Ivmaccountant Interface Virtual PC
- Ivmaccountant Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743473"
---
# <a name="ivmaccountant-interface"></a><span data-ttu-id="f372b-105">Ivmaccountant-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f372b-105">IVMAccountant interface</span></span>

<span data-ttu-id="f372b-106">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f372b-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f372b-107">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f372b-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f372b-108">Ermöglicht den Zugriff auf Buchhaltungs bezogene Informationen für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f372b-108">Provides access to accounting-related information for a virtual machine.</span></span> <span data-ttu-id="f372b-109">Zum Abrufen des **ivmaccountant** für eine virtuelle Maschine verwenden Sie die [**ivmvirtualmachine:: Accountant**](ivmvirtualmachine-accountant.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f372b-109">To retrieve the **IVMAccountant** for a virtual machine, use the [**IVMVirtualMachine::Accountant**](ivmvirtualmachine-accountant.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="f372b-110">Member</span><span class="sxs-lookup"><span data-stu-id="f372b-110">Members</span></span>

<span data-ttu-id="f372b-111">Die **ivmaccountant** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f372b-111">The **IVMAccountant** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f372b-112">**Ivmaccountant** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f372b-112">**IVMAccountant** also has these types of members:</span></span>

-   [<span data-ttu-id="f372b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f372b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f372b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f372b-114">Properties</span></span>

<span data-ttu-id="f372b-115">Die **ivmaccountant** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f372b-115">The **IVMAccountant** interface has these properties.</span></span>



| <span data-ttu-id="f372b-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f372b-116">Property</span></span>                                                                        | <span data-ttu-id="f372b-117">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="f372b-117">Access type</span></span>          | <span data-ttu-id="f372b-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f372b-118">Description</span></span>                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f372b-119">**CPU**</span><span class="sxs-lookup"><span data-stu-id="f372b-119">**CPUUtilization**</span></span>](ivmaccountant-cpuutilization.md)<br/>               | <span data-ttu-id="f372b-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f372b-120">Read-only</span></span><br/> | <span data-ttu-id="f372b-121">Der Prozentsatz der aktuellen CPU-Auslastung für diese virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="f372b-121">The percentage of current CPU utilization for this virtual machine.</span></span><br/>                          |
| [<span data-ttu-id="f372b-122">**Cpuutilizationhistory**</span><span class="sxs-lookup"><span data-stu-id="f372b-122">**CPUUtilizationHistory**</span></span>](ivmaccountant-cpuutilizationhistory.md)<br/> | <span data-ttu-id="f372b-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f372b-123">Read-only</span></span><br/> | <span data-ttu-id="f372b-124">Die aktuelle CPU-Auslastung dieses virtuellen Computers (als Array von Prozentwerten).</span><span class="sxs-lookup"><span data-stu-id="f372b-124">The recent CPU utilization of this virtual machine (as an array of percentage values).</span></span><br/>       |
| [<span data-ttu-id="f372b-125">**Diskbytesread**</span><span class="sxs-lookup"><span data-stu-id="f372b-125">**DiskBytesRead**</span></span>](ivmaccountant-diskbytesread.md)<br/>                 | <span data-ttu-id="f372b-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f372b-126">Read-only</span></span><br/> | <span data-ttu-id="f372b-127">Die Gesamtanzahl der von allen Speicher Controllern für diesen virtuellen Computer gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="f372b-127">The total number of bytes read by all storage controllers for this virtual machine.</span></span><br/>          |
| [<span data-ttu-id="f372b-128">**Diskbytesgeschrieben**</span><span class="sxs-lookup"><span data-stu-id="f372b-128">**DiskBytesWritten**</span></span>](ivmaccountant-diskbyteswritten.md)<br/>           | <span data-ttu-id="f372b-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f372b-129">Read-only</span></span><br/> | <span data-ttu-id="f372b-130">Die Gesamtanzahl der Bytes, die von allen Speicher Controllern für diesen virtuellen Computer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="f372b-130">The total number of bytes written by all storage controllers for this virtual machine.</span></span><br/>       |
| [<span data-ttu-id="f372b-131">**Networkbytesempfangene**</span><span class="sxs-lookup"><span data-stu-id="f372b-131">**NetworkBytesReceived**</span></span>](ivmaccountant-networkbytesreceived.md)<br/>   | <span data-ttu-id="f372b-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f372b-132">Read-only</span></span><br/> | <span data-ttu-id="f372b-133">Die Gesamtanzahl der Bytes, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="f372b-133">The total number of bytes received by all virtual network adapters for this virtual machine.</span></span><br/> |
| [<span data-ttu-id="f372b-134">**Network bytess**</span><span class="sxs-lookup"><span data-stu-id="f372b-134">**NetworkBytesSent**</span></span>](ivmaccountant-networkbytessent.md)<br/>           | <span data-ttu-id="f372b-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f372b-135">Read-only</span></span><br/> | <span data-ttu-id="f372b-136">Die Gesamtanzahl der Bytes, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f372b-136">The total number of bytes sent by all virtual network adapters for this virtual machine.</span></span><br/>     |
| [<span data-ttu-id="f372b-137">**Betriebszeit**</span><span class="sxs-lookup"><span data-stu-id="f372b-137">**UpTime**</span></span>](ivmaccountant-uptime.md)<br/>                               | <span data-ttu-id="f372b-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f372b-138">Read-only</span></span><br/> | <span data-ttu-id="f372b-139">Die Anzahl der Sekunden, die der virtuelle Computer ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f372b-139">The number of seconds that the virtual machine has been running.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="f372b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f372b-140">Requirements</span></span>



| <span data-ttu-id="f372b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f372b-141">Requirement</span></span> | <span data-ttu-id="f372b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="f372b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f372b-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f372b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f372b-144">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f372b-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f372b-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f372b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f372b-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f372b-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f372b-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f372b-147">End of client support</span></span><br/>    | <span data-ttu-id="f372b-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f372b-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f372b-149">Produkt</span><span class="sxs-lookup"><span data-stu-id="f372b-149">Product</span></span><br/>                  | <span data-ttu-id="f372b-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f372b-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f372b-151">Header</span><span class="sxs-lookup"><span data-stu-id="f372b-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f372b-152"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f372b-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f372b-153">IID</span><span class="sxs-lookup"><span data-stu-id="f372b-153">IID</span></span><br/>                      | <span data-ttu-id="f372b-154">IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.</span><span class="sxs-lookup"><span data-stu-id="f372b-154">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



 

