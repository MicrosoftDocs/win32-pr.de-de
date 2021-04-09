---
description: Wendet eine Momentaufnahme des virtuellen Computers auf den virtuellen Computer an, auf dem Sie erstellt wurde.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Applysnapshot-Methode der Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865223"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="321d6-103">Applysnapshot-Methode der MSVM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="321d6-103">ApplySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="321d6-104">Wendet eine Momentaufnahme des virtuellen Computers auf den virtuellen Computer an, auf dem Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="321d6-104">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="321d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="321d6-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="321d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="321d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="321d6-107">*Momentaufnahme* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="321d6-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="321d6-108">Ein Verweis auf eine von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) abgeleitete Klasse, die die anzuwendende Momentaufnahme des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="321d6-108">A reference to a class derived from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) that represents the virtual machine snapshot to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="321d6-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="321d6-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="321d6-110">Dieser Vorgang wird immer asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="321d6-110">This operation is always performed asynchronously.</span></span> <span data-ttu-id="321d6-111">Diese Methode gibt 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="321d6-111">This method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="321d6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="321d6-112">Return value</span></span>

<span data-ttu-id="321d6-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="321d6-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="321d6-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="321d6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="321d6-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="321d6-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="321d6-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="321d6-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="321d6-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-120">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="321d6-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="321d6-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="321d6-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-123">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="321d6-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="321d6-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-125">**Ungültiger Status** (32775)</span><span class="sxs-lookup"><span data-stu-id="321d6-125">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-126">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="321d6-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="321d6-127">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="321d6-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="321d6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="321d6-128">Requirements</span></span>



| <span data-ttu-id="321d6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="321d6-129">Requirement</span></span> | <span data-ttu-id="321d6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="321d6-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321d6-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="321d6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="321d6-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="321d6-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="321d6-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="321d6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="321d6-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="321d6-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="321d6-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="321d6-135">Namespace</span></span><br/>                | <span data-ttu-id="321d6-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="321d6-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="321d6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="321d6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="321d6-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="321d6-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="321d6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="321d6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="321d6-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="321d6-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="321d6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="321d6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321d6-142">**MSVM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="321d6-142">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="321d6-143">**Applyvirtualsystemsnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="321d6-143">**ApplyVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="321d6-144">**Applyvirtualsystemsnapshotex (v1)**</span><span class="sxs-lookup"><span data-stu-id="321d6-144">**ApplyVirtualSystemSnapshotEx (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

