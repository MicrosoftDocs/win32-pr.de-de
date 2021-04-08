---
description: Aktualisiert den Elementnamen für das angegebene CIM \_ CollectionOfMSEs-Objekt.
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Renamecollection-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4bb127fc8fba528e883631602fcea8ba0b4de2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867967"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="87cf4-103">Renamecollection-Methode der MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="87cf4-103">RenameCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="87cf4-104">Aktualisiert den Elementnamen für das angegebene [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="87cf4-104">Updates the element name for the specified [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cf4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87cf4-105">Syntax</span></span>


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="87cf4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87cf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87cf4-107">*Sammlung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87cf4-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87cf4-108">Die Auflistung, die umbenannt werden soll.</span><span class="sxs-lookup"><span data-stu-id="87cf4-108">The collection to rename.</span></span>

</dd> <dt>

<span data-ttu-id="87cf4-109">*NewName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87cf4-109">*NewName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87cf4-110">Der neue Name, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="87cf4-110">The new name to use.</span></span>

</dd> <dt>

<span data-ttu-id="87cf4-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="87cf4-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87cf4-112">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="87cf4-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87cf4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87cf4-113">Return value</span></span>

<span data-ttu-id="87cf4-114">Gibt 0 zurück, wenn erfolgreich, oder 4096, wenn der Auftrag gestartet wurde. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87cf4-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="87cf4-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="87cf4-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="87cf4-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="87cf4-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="87cf4-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="87cf4-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="87cf4-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="87cf4-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="87cf4-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="87cf4-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="87cf4-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="87cf4-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="87cf4-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="87cf4-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="87cf4-128">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="87cf4-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="87cf4-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87cf4-129">Requirements</span></span>



| <span data-ttu-id="87cf4-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87cf4-130">Requirement</span></span> | <span data-ttu-id="87cf4-131">Wert</span><span class="sxs-lookup"><span data-stu-id="87cf4-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cf4-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87cf4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="87cf4-133">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87cf4-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="87cf4-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87cf4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="87cf4-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="87cf4-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="87cf4-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="87cf4-136">Namespace</span></span><br/>                | <span data-ttu-id="87cf4-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="87cf4-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87cf4-138">MOF</span><span class="sxs-lookup"><span data-stu-id="87cf4-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87cf4-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="87cf4-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87cf4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="87cf4-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87cf4-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87cf4-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87cf4-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87cf4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cf4-143">**MSVM \_ collectionmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="87cf4-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




