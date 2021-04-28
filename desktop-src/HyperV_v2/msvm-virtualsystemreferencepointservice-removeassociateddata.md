---
description: 'RemoveAssociatedData-Methode der Msvm_VirtualSystemReferencePointService Klasse: Entfernt das dem Verweispunkt zugeordnete Datenprotokoll.'
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: RemoveAssociatedData-Methode der Msvm_VirtualSystemReferencePointService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b5291e4e018edc89909ccde36ce0e420698af8e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118618"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="53808-103">RemoveAssociatedData-Methode der Msvm \_ VirtualSystemReferencePointService-Klasse</span><span class="sxs-lookup"><span data-stu-id="53808-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="53808-104">Entfernt das dem Referenzpunkt zugeordnete Datenprotokoll.</span><span class="sxs-lookup"><span data-stu-id="53808-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="53808-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53808-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="53808-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53808-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53808-107">*AffectedReferencePoint* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="53808-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53808-108">Ein Verweis auf die [**Msvm \_ VirtualSystemReferencePoint-Instanz,**](msvm-virtualsystemreferencepoint.md) die den zu entfernenden Verweispunkt darstellt.</span><span class="sxs-lookup"><span data-stu-id="53808-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="53808-109">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53808-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53808-110">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="53808-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="53808-111">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="53808-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53808-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53808-112">Return value</span></span>

<span data-ttu-id="53808-113">Bei Erfolg wird 0 (Vollständig ohne Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="53808-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="53808-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="53808-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53808-115">**Überprüfte Methodenparameter – Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="53808-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="53808-116">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="53808-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="53808-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="53808-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="53808-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="53808-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="53808-119">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="53808-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="53808-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="53808-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="53808-121">**Ungültiger** Parameter (32773)</span><span class="sxs-lookup"><span data-stu-id="53808-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="53808-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="53808-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="53808-123">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="53808-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="53808-124">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="53808-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="53808-125">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="53808-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="53808-126">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="53808-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="53808-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53808-127">Requirements</span></span>



| <span data-ttu-id="53808-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53808-128">Requirement</span></span> | <span data-ttu-id="53808-129">Wert</span><span class="sxs-lookup"><span data-stu-id="53808-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53808-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53808-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53808-131">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53808-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="53808-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53808-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53808-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="53808-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="53808-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="53808-134">Namespace</span></span><br/>                | <span data-ttu-id="53808-135">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="53808-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53808-136">MOF</span><span class="sxs-lookup"><span data-stu-id="53808-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53808-137"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="53808-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53808-138">DLL</span><span class="sxs-lookup"><span data-stu-id="53808-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53808-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53808-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53808-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53808-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53808-141">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="53808-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




