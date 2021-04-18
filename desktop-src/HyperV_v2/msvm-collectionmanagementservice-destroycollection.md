---
description: Löscht das angegebene CIM \_ CollectionOfMSEs-Objekt.
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Destroycollection-Methode der Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69b35bfac3601bd92bc7b1fea967de404b716773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351592"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="54631-103">Destroycollection-Methode der MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="54631-103">DestroyCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="54631-104">Löscht das angegebene [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="54631-104">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="54631-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54631-105">Syntax</span></span>


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="54631-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54631-107">*Sammlung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54631-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54631-108">Die zu löschender Auflistung.</span><span class="sxs-lookup"><span data-stu-id="54631-108">The collection to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="54631-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54631-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54631-110">Ein Verweis auf den Auftrag (kann NULL sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="54631-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54631-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54631-111">Return value</span></span>

<span data-ttu-id="54631-112">Gibt 0 zurück, wenn erfolgreich, oder 4096, wenn der Auftrag gestartet wurde. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54631-112">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="54631-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="54631-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="54631-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="54631-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="54631-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="54631-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="54631-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="54631-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="54631-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="54631-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="54631-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="54631-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="54631-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="54631-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="54631-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="54631-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="54631-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="54631-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="54631-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="54631-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="54631-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="54631-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="54631-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="54631-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="54631-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="54631-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="54631-126">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="54631-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="54631-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54631-127">Requirements</span></span>



| <span data-ttu-id="54631-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54631-128">Requirement</span></span> | <span data-ttu-id="54631-129">Wert</span><span class="sxs-lookup"><span data-stu-id="54631-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54631-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54631-130">Minimum supported client</span></span><br/> | <span data-ttu-id="54631-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54631-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="54631-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54631-132">Minimum supported server</span></span><br/> | <span data-ttu-id="54631-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="54631-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="54631-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="54631-134">Namespace</span></span><br/>                | <span data-ttu-id="54631-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="54631-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54631-136">MOF</span><span class="sxs-lookup"><span data-stu-id="54631-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54631-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="54631-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54631-138">DLL</span><span class="sxs-lookup"><span data-stu-id="54631-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54631-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54631-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54631-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54631-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54631-141">**MSVM \_ collectionmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="54631-141">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




