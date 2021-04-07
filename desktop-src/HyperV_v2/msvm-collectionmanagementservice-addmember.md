---
description: Fügt das angegebene verwaltete Element als Member des angegebenen CIM \_ CollectionOfMSEs-Objekts hinzu.
ms.assetid: 6f23eecc-b445-4495-ae96-76b89652a1cb
title: AddMember-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.AddMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6b885701086262fda48c5d50abd750eca6866c72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760500"
---
# <a name="addmember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="b0ed3-103">AddMember-Methode der MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b0ed3-103">AddMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="b0ed3-104">Fügt das angegebene verwaltete Element als Member des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0ed3-104">Adds the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ed3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0ed3-105">Syntax</span></span>


```mof
uint32 AddMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b0ed3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0ed3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0ed3-107">*Mitglied* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed3-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed3-108">Der Member, der der Auflistung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0ed3-108">The member to add to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed3-109">*Sammlung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0ed3-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed3-110">Die Auflistung, der das Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0ed3-110">The collection to add the member to.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed3-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b0ed3-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ed3-112">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="b0ed3-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0ed3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0ed3-113">Return value</span></span>

<span data-ttu-id="b0ed3-114">Gibt 0 zurück, wenn erfolgreich, oder 4096, wenn der Auftrag gestartet wurde. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0ed3-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b0ed3-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="b0ed3-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="b0ed3-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="b0ed3-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="b0ed3-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="b0ed3-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b0ed3-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="b0ed3-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b0ed3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0ed3-129">Requirements</span></span>



| <span data-ttu-id="b0ed3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0ed3-130">Requirement</span></span> | <span data-ttu-id="b0ed3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b0ed3-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ed3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b0ed3-133">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0ed3-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b0ed3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0ed3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b0ed3-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b0ed3-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b0ed3-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0ed3-136">Namespace</span></span><br/>                | <span data-ttu-id="b0ed3-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b0ed3-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b0ed3-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b0ed3-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0ed3-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed3-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0ed3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b0ed3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0ed3-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0ed3-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b0ed3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0ed3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0ed3-143">**MSVM \_ collectionmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="b0ed3-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




