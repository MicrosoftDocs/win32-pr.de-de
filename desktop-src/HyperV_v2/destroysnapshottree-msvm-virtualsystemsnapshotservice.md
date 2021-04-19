---
description: Entfernt eine vorhandene Momentaufnahme und alle untergeordneten Elemente eines virtuellen Computers.
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Destroysnapshottree-Methode der Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5658e954766531765c47f8bef80d5509f2ad27c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362373"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="c862d-103">Destroysnapshottree-Methode der MSVM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="c862d-103">DestroySnapshotTree method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="c862d-104">Entfernt eine vorhandene Momentaufnahme und alle untergeordneten Elemente eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c862d-104">Removes an existing snapshot, and all its children, of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c862d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c862d-105">Syntax</span></span>


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c862d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c862d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c862d-107">*Snapshotsettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c862d-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c862d-108">Ein [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Verweis, der die zu löschender Momentaufnahme Struktur des virtuellen Computers darstellt.</span><span class="sxs-lookup"><span data-stu-id="c862d-108">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot tree to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="c862d-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c862d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c862d-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c862d-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c862d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c862d-111">Return value</span></span>

<span data-ttu-id="c862d-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c862d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c862d-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="c862d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="c862d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="c862d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="c862d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="c862d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="c862d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c862d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="c862d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="c862d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="c862d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="c862d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="c862d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c862d-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="c862d-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c862d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c862d-126">Requirements</span></span>



| <span data-ttu-id="c862d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c862d-127">Requirement</span></span> | <span data-ttu-id="c862d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c862d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c862d-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c862d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c862d-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c862d-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c862d-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c862d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c862d-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c862d-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c862d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c862d-133">Namespace</span></span><br/>                | <span data-ttu-id="c862d-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c862d-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c862d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c862d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c862d-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c862d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c862d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c862d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c862d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c862d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c862d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c862d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c862d-140">**MSVM \_ virtualsystemsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="c862d-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="c862d-141">**Removevirtualsystemsnapshottree (v1)**</span><span class="sxs-lookup"><span data-stu-id="c862d-141">**RemoveVirtualSystemSnapshotTree (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

