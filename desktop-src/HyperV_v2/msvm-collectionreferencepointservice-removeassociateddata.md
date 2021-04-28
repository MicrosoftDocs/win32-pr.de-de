---
description: RemoveAssociatedData-Methode der Msvm_CollectionReferencePointService - Entfernt das dem Verweispunkt zugeordnete Datenprotokoll.
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: RemoveAssociatedData-Methode der Msvm_CollectionReferencePointService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66a5cf068545f31f9919a9da60a1b09b32f78e4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119228"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="0048a-103">RemoveAssociatedData-Methode der Msvm \_ CollectionReferencePointService-Klasse</span><span class="sxs-lookup"><span data-stu-id="0048a-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="0048a-104">Entfernt das dem Referenzpunkt zugeordnete Datenprotokoll.</span><span class="sxs-lookup"><span data-stu-id="0048a-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="0048a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0048a-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0048a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0048a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0048a-107">*AffectedReferencePointCollection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0048a-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0048a-108">Verweis auf die betroffene Auflistung des Referenzpunkts des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="0048a-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="0048a-109">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0048a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0048a-110">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0048a-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0048a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0048a-111">Return value</span></span>

<span data-ttu-id="0048a-112">Bei Erfolg wird entweder 0 (kein Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0048a-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="0048a-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="0048a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="0048a-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-115">**Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="0048a-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="0048a-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-117">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="0048a-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-118">**Ungültiger Zustand** (5)</span><span class="sxs-lookup"><span data-stu-id="0048a-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-119">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="0048a-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-120">**DMTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="0048a-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-121">**Überprüfte Methodenparameter – Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="0048a-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-122">**Reservierte Methode** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="0048a-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0048a-123">**Herstellerspezifisch** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="0048a-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0048a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0048a-124">Requirements</span></span>



| <span data-ttu-id="0048a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0048a-125">Requirement</span></span> | <span data-ttu-id="0048a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0048a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0048a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0048a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0048a-128">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0048a-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0048a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0048a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0048a-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0048a-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0048a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0048a-131">Namespace</span></span><br/>                | <span data-ttu-id="0048a-132">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0048a-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0048a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0048a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0048a-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="0048a-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0048a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0048a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0048a-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0048a-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0048a-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0048a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0048a-138">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="0048a-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




