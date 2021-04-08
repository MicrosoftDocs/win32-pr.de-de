---
description: Ruft den Fehler ab.
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: GetError-Methode der Msvm_VirtualSystemReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b26995171059389f7f7afb3fb90e3506b39affd5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050676"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="212f5-103">GetError-Methode der MSVM \_ virtualsystemreferencepointexportjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="212f5-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="212f5-104">Ruft den Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="212f5-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="212f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="212f5-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="212f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="212f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="212f5-107">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="212f5-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="212f5-108">Der abgerufene Fehler.</span><span class="sxs-lookup"><span data-stu-id="212f5-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="212f5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="212f5-109">Return value</span></span>

<span data-ttu-id="212f5-110">Bei Erfolg wird 0 zurückgegeben. Andernfalls enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="212f5-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="212f5-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="212f5-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-112">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="212f5-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-113">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="212f5-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-114">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="212f5-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-115">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="212f5-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="212f5-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-117">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="212f5-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-118">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="212f5-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-119">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="212f5-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-120">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="212f5-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-121">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="212f5-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="212f5-122">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="212f5-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="212f5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="212f5-123">Requirements</span></span>



| <span data-ttu-id="212f5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="212f5-124">Requirement</span></span> | <span data-ttu-id="212f5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="212f5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="212f5-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="212f5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="212f5-127">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="212f5-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="212f5-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="212f5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="212f5-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="212f5-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="212f5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="212f5-130">Namespace</span></span><br/>                | <span data-ttu-id="212f5-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="212f5-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="212f5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="212f5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="212f5-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="212f5-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="212f5-134">DLL</span><span class="sxs-lookup"><span data-stu-id="212f5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="212f5-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="212f5-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="212f5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="212f5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="212f5-137">**MSVM \_ virtualsystemreferencepointexportjob**</span><span class="sxs-lookup"><span data-stu-id="212f5-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




