---
description: Erstellt ein neues CIM \_ CollectionOfMSEs-Objekt.
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Definecollection-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362659"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="84262-103">Definecollection-Methode der MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="84262-103">DefineCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="84262-104">Erstellt ein neues [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="84262-104">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="84262-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84262-105">Syntax</span></span>


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="84262-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84262-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84262-107">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84262-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84262-108">Der Name der neuen Auflistung.</span><span class="sxs-lookup"><span data-stu-id="84262-108">The name of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="84262-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84262-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84262-110">Die ID der neuen Auflistung.</span><span class="sxs-lookup"><span data-stu-id="84262-110">The ID of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="84262-111">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84262-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84262-112">Der Typ der neuen Auflistung.</span><span class="sxs-lookup"><span data-stu-id="84262-112">The type of the new collection.</span></span>

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

<span data-ttu-id="84262-113">**Sammlung virtueller Systeme** (0)</span><span class="sxs-lookup"><span data-stu-id="84262-113">**Collection of Virtual Systems** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

<span data-ttu-id="84262-114">**Sammlung von Sammlungen** (1)</span><span class="sxs-lookup"><span data-stu-id="84262-114">**Collection of Collections** (1)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="84262-115">*Definedcollection* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="84262-115">*DefinedCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84262-116">Verweis auf die-Objekte, die die Auflistung definieren.</span><span class="sxs-lookup"><span data-stu-id="84262-116">Reference to the objects that define the collection.</span></span>

</dd> <dt>

<span data-ttu-id="84262-117">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="84262-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84262-118">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="84262-118">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84262-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84262-119">Return value</span></span>

<span data-ttu-id="84262-120">Wenn erfolgreich, wird 0 oder 4096 zurückgegeben (Auftrag gestartet); Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84262-120">If successful, returns a 0 or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="84262-121">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="84262-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84262-122">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="84262-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="84262-123">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="84262-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="84262-124">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="84262-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="84262-125">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="84262-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="84262-126">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="84262-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="84262-127">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="84262-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="84262-128">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="84262-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="84262-129">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="84262-129">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="84262-130">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="84262-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="84262-131">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="84262-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="84262-132">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="84262-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="84262-133">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="84262-133">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="84262-134">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="84262-134">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84262-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84262-135">Requirements</span></span>



| <span data-ttu-id="84262-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84262-136">Requirement</span></span> | <span data-ttu-id="84262-137">Wert</span><span class="sxs-lookup"><span data-stu-id="84262-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84262-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84262-138">Minimum supported client</span></span><br/> | <span data-ttu-id="84262-139">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84262-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="84262-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84262-140">Minimum supported server</span></span><br/> | <span data-ttu-id="84262-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84262-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="84262-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="84262-142">Namespace</span></span><br/>                | <span data-ttu-id="84262-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="84262-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84262-144">MOF</span><span class="sxs-lookup"><span data-stu-id="84262-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84262-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="84262-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84262-146">DLL</span><span class="sxs-lookup"><span data-stu-id="84262-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84262-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84262-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84262-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84262-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84262-149">**MSVM \_ collectionmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="84262-149">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




