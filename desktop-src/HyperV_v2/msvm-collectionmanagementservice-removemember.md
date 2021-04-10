---
description: Entfernt das angegebene verwaltete Element als Member des angegebenen CIM \_ CollectionOfMSEs-Objekts.
ms.assetid: ea945d24-bcff-476b-9adb-c6573cdbc0b5
title: RemoveMember-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 894230dcf5e9a537ca444815f8e941a8e6fcf09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867968"
---
# <a name="removemember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="3ad6e-103">RemoveMember-Methode der MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="3ad6e-103">RemoveMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="3ad6e-104">Entfernt das angegebene verwaltete Element als Member des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3ad6e-104">Removes the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ad6e-105">Syntax</span></span>


```mof
uint32 RemoveMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3ad6e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ad6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad6e-107">*Mitglied* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ad6e-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad6e-108">Der zu entfernende Member.</span><span class="sxs-lookup"><span data-stu-id="3ad6e-108">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="3ad6e-109">*Sammlung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ad6e-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad6e-110">Die Auflistung, aus der das Element entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ad6e-110">The collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="3ad6e-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ad6e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad6e-112">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="3ad6e-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad6e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ad6e-113">Return value</span></span>

<span data-ttu-id="3ad6e-114">Gibt 0 zurück, wenn erfolgreich, oder 4096, wenn der Auftrag gestartet wurde. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3ad6e-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3ad6e-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3ad6e-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3ad6e-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3ad6e-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3ad6e-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3ad6e-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3ad6e-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="3ad6e-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3ad6e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ad6e-129">Requirements</span></span>



| <span data-ttu-id="3ad6e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ad6e-130">Requirement</span></span> | <span data-ttu-id="3ad6e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3ad6e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad6e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad6e-133">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ad6e-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3ad6e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ad6e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad6e-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3ad6e-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3ad6e-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ad6e-136">Namespace</span></span><br/>                | <span data-ttu-id="3ad6e-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3ad6e-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ad6e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3ad6e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ad6e-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ad6e-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ad6e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3ad6e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ad6e-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ad6e-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ad6e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ad6e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad6e-143">**MSVM \_ collectionmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="3ad6e-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




