---
description: Entfernt das angegebene verwaltete Element als Member der CIM \_ CollectionOfMSEs mit dem angegebenen Bezeichner. Dies ist auch dann erfolgreich, wenn das Objekt mit diesem Bezeichner nicht vorhanden ist.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Removemembership byid-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218699"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="6ac8c-104">Removemembership byid-Methode der MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="6ac8c-104">RemoveMemberById method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="6ac8c-105">Entfernt das angegebene verwaltete Element als Member der [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) mit dem angegebenen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6ac8c-105">Removes the specified managed element as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="6ac8c-106">Dies ist auch dann erfolgreich, wenn das Objekt mit diesem Bezeichner nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6ac8c-106">This will succeed even if the object with that identifier is not present.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac8c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ac8c-107">Syntax</span></span>


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6ac8c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ac8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac8c-109">*Mitglied* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ac8c-109">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac8c-110">Der zu entfernende Member.</span><span class="sxs-lookup"><span data-stu-id="6ac8c-110">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="6ac8c-111">*CollectionId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ac8c-111">*CollectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac8c-112">Die Sammlungs-ID der Auflistung, aus der das Element entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ac8c-112">The collection ID of the collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="6ac8c-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6ac8c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac8c-114">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="6ac8c-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac8c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ac8c-115">Return value</span></span>

<span data-ttu-id="6ac8c-116">Gibt 0 zurück, wenn erfolgreich, oder 4096, wenn der Auftrag gestartet wurde. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ac8c-116">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6ac8c-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="6ac8c-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="6ac8c-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="6ac8c-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="6ac8c-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="6ac8c-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6ac8c-130">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="6ac8c-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6ac8c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ac8c-131">Requirements</span></span>



| <span data-ttu-id="6ac8c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ac8c-132">Requirement</span></span> | <span data-ttu-id="6ac8c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6ac8c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac8c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6ac8c-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ac8c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6ac8c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ac8c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6ac8c-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6ac8c-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6ac8c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ac8c-138">Namespace</span></span><br/>                | <span data-ttu-id="6ac8c-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6ac8c-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6ac8c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6ac8c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ac8c-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6ac8c-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ac8c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6ac8c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ac8c-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ac8c-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ac8c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ac8c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac8c-145">**MSVM \_ collectionmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="6ac8c-145">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




