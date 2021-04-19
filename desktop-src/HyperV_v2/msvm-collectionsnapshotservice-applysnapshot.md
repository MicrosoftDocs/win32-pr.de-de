---
description: Wendet eine Momentaufnahme Sammlung auf die Sammlung des virtuellen Computer Systems an.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Applysnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353049"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="7e14a-103">Applysnapshot-Methode der MSVM \_ collectionsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e14a-103">ApplySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="7e14a-104">Wendet eine Momentaufnahme Sammlung auf die Sammlung des virtuellen Computer Systems an.</span><span class="sxs-lookup"><span data-stu-id="7e14a-104">Applies a snapshot collection to the collection of virtual computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e14a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e14a-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7e14a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e14a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e14a-107">*Snapshotcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e14a-107">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e14a-108">Ein Verweis auf eine [**CIM \_**](cim-collection.md) -Auflistung, die die anzuwendende Momentaufnahme Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e14a-108">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="7e14a-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e14a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e14a-110">Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e14a-110">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="7e14a-111">Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e14a-111">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e14a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e14a-112">Return value</span></span>

<span data-ttu-id="7e14a-113">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e14a-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7e14a-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="7e14a-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-115">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="7e14a-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-116">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="7e14a-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="7e14a-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-118">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="7e14a-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-119">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="7e14a-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-120">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="7e14a-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-121">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="7e14a-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="7e14a-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-123">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="7e14a-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7e14a-124">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="7e14a-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7e14a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e14a-125">Requirements</span></span>



| <span data-ttu-id="7e14a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e14a-126">Requirement</span></span> | <span data-ttu-id="7e14a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7e14a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e14a-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e14a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7e14a-129">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e14a-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e14a-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e14a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7e14a-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e14a-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7e14a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e14a-132">Namespace</span></span><br/>                | <span data-ttu-id="7e14a-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e14a-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e14a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7e14a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e14a-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e14a-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e14a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7e14a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e14a-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e14a-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e14a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e14a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e14a-139">**MSVM \_ collectionsnapshotservice**</span><span class="sxs-lookup"><span data-stu-id="7e14a-139">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




