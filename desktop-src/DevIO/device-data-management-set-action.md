---
description: Definieren Sie den Satz von Aktionen für den ioctl-Speicher für den ioctl-Speicher, der die \_ \_ \_ \_ \_ Attribute des
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861104"
---
# <a name="device_data_management_set_action"></a><span data-ttu-id="39011-103">Aktion für Geräte \_ Daten- \_ Verwaltungs \_ Gruppe \_</span><span class="sxs-lookup"><span data-stu-id="39011-103">DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION</span></span>

<span data-ttu-id="39011-104">Bei den folgenden Konstanten Werten handelt es sich um den Satz möglicher Werte für den **\_ \_ \_ \_ Aktionstyp für die Gerätedaten Verwaltung** , der als **DWORD**-Typ definiert ist.</span><span class="sxs-lookup"><span data-stu-id="39011-104">The following constant values are the set of possible values for the **DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION** type, which is defined as type **DWORD**.</span></span>

<dl> <dt>

<span data-ttu-id="39011-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**Devicedsmaction \_ None**</span><span class="sxs-lookup"><span data-stu-id="39011-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction\_None**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-106">0</span><span class="sxs-lookup"><span data-stu-id="39011-106">0</span></span>
</dt> <dt>



<span data-ttu-id="39011-107">Es wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-107">No action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**Devicedsmaction \_ Trim**</span><span class="sxs-lookup"><span data-stu-id="39011-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction\_Trim**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-109">1</span><span class="sxs-lookup"><span data-stu-id="39011-109">1</span></span>
</dt> <dt>



<span data-ttu-id="39011-110">Eine Trim-Aktion wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-110">A trim action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**Devicedsmaction- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="39011-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction\_Notification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-112">2 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="39011-112">2 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000002)</span></span>
</dt> <dt>



<span data-ttu-id="39011-113">Eine Benachrichtigungs Aktion wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-113">A notification action is performed.</span></span> <span data-ttu-id="39011-114">Die Parameter sind in einer [**Geräte- \_ DSM- \_ Benachrichtigungs \_ Parameter**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="39011-114">The parameters are in a [**DEVICE\_DSM\_NOTIFICATION\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) structure.</span></span> <span data-ttu-id="39011-115">Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.</span><span class="sxs-lookup"><span data-stu-id="39011-115">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**Devicedsmaction \_ offloadread**</span><span class="sxs-lookup"><span data-stu-id="39011-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction\_OffloadRead**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-117">3 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="39011-117">3 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000003)</span></span>
</dt> <dt>



<span data-ttu-id="39011-118">Eine Auslagerungs Leseaktion wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-118">An offload read action is performed.</span></span> <span data-ttu-id="39011-119">Die Parameter befinden sich in einer Struktur der AD- [**\_ \_ \_ Auslagerungs Lese \_ Parameter für Geräte**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) .</span><span class="sxs-lookup"><span data-stu-id="39011-119">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_READ\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) structure.</span></span> <span data-ttu-id="39011-120">Die Ausgabe befindet sich in einer [**Speicher \_ \_ Auslastungs \_ Ausgabe**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) Struktur.</span><span class="sxs-lookup"><span data-stu-id="39011-120">The output is in a [**STORAGE\_OFFLOAD\_READ\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) structure.</span></span> <span data-ttu-id="39011-121">Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.</span><span class="sxs-lookup"><span data-stu-id="39011-121">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="39011-122">**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39011-122">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**Devicedsmaction \_ offloadwrite**</span><span class="sxs-lookup"><span data-stu-id="39011-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction\_OffloadWrite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-124">4</span><span class="sxs-lookup"><span data-stu-id="39011-124">4</span></span>
</dt> <dt>



<span data-ttu-id="39011-125">Eine Auslagerungs Schreibaktion wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-125">An offload write action is performed.</span></span> <span data-ttu-id="39011-126">Die Parameter befinden sich in einer [**Geräte- \_ DSM- \_ Offload- \_ Schreib \_ Parameter**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) Struktur.</span><span class="sxs-lookup"><span data-stu-id="39011-126">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_WRITE\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) structure.</span></span> <span data-ttu-id="39011-127">Die Ausgabe befindet sich in einer [**Speicher \_ Auslastungs- \_ Schreib \_ Ausgabe**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) Struktur.</span><span class="sxs-lookup"><span data-stu-id="39011-127">The output is in a [**STORAGE\_OFFLOAD\_WRITE\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) structure.</span></span>

<span data-ttu-id="39011-128">**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39011-128">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Devicedsmaction- \_ Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="39011-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction\_Allocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-130">5 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000005)</span><span class="sxs-lookup"><span data-stu-id="39011-130">5 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000005)</span></span>
</dt> <dt>



<span data-ttu-id="39011-131">Eine Zuordnungs Bitmap wird für den ersten Daten Satz Bereich zurückgegeben, der übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="39011-131">An allocation bitmap is returned for the first data set range passed in.</span></span> <span data-ttu-id="39011-132">Die Ausgabe befindet sich in [**einer \_ \_ \_ \_ Bereitstellungs \_ Zustands**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) Struktur für das Geräte Dataset lb.</span><span class="sxs-lookup"><span data-stu-id="39011-132">The output is in a [**DEVICE\_DATA\_SET\_LB\_PROVISIONING\_STATE**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) structure.</span></span> <span data-ttu-id="39011-133">Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.</span><span class="sxs-lookup"><span data-stu-id="39011-133">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="39011-134">**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39011-134">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**Devicedsmaction- \_ Reparatur**</span><span class="sxs-lookup"><span data-stu-id="39011-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction\_Repair**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-136">6 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000006)</span><span class="sxs-lookup"><span data-stu-id="39011-136">6 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000006)</span></span>
</dt> <dt>



<span data-ttu-id="39011-137">Eine Reparaturaktion wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-137">A repair action is performed.</span></span> <span data-ttu-id="39011-138">Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.</span><span class="sxs-lookup"><span data-stu-id="39011-138">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="39011-139">**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39011-139">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**Devicedsmaction-Bereinigung \_**</span><span class="sxs-lookup"><span data-stu-id="39011-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction\_Scrub**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-141">7 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000007)</span><span class="sxs-lookup"><span data-stu-id="39011-141">7 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000007)</span></span>
</dt> <dt>



<span data-ttu-id="39011-142">Eine Bereinigungsaktion wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-142">A scrub action is performed.</span></span> <span data-ttu-id="39011-143">Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.</span><span class="sxs-lookup"><span data-stu-id="39011-143">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="39011-144">**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39011-144">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39011-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Devicedsmaction- \_ Resilienz**</span><span class="sxs-lookup"><span data-stu-id="39011-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction\_Resiliency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39011-146">8 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000008)</span><span class="sxs-lookup"><span data-stu-id="39011-146">8 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000008)</span></span>
</dt> <dt>



<span data-ttu-id="39011-147">Eine resilienzaktion wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39011-147">A resiliency action is performed.</span></span> <span data-ttu-id="39011-148">Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.</span><span class="sxs-lookup"><span data-stu-id="39011-148">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="39011-149">**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39011-149">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39011-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39011-150">Requirements</span></span>



| <span data-ttu-id="39011-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39011-151">Requirement</span></span> | <span data-ttu-id="39011-152">Wert</span><span class="sxs-lookup"><span data-stu-id="39011-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39011-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39011-153">Minimum supported client</span></span><br/> | <span data-ttu-id="39011-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39011-154">Windows 7</span></span><br/>                                                                                      |
| <span data-ttu-id="39011-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39011-155">Minimum supported server</span></span><br/> | <span data-ttu-id="39011-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39011-156">Windows Server 2008 R2</span></span><br/>                                                                         |
| <span data-ttu-id="39011-157">Header</span><span class="sxs-lookup"><span data-stu-id="39011-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="39011-158"><dt>Winioctl. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39011-158"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



 

 




