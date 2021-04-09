---
description: Überprüft, ob ein Dateisystem eine virtuelle Festplatte mit aktivierten permanenten Reservierungen unterstützen kann.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Validatepersistentreservationsupport-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 596e5cf840ee65dc0b3ad5315462db4666c8b262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959038"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="fb203-103">Validatepersistentreservationsupport-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb203-103">ValidatePersistentReservationSupport method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="fb203-104">Überprüft, ob ein Dateisystem eine virtuelle Festplatte mit aktivierten permanenten Reservierungen unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="fb203-104">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb203-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb203-105">Syntax</span></span>


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fb203-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb203-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb203-107">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb203-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb203-108">Ein voll qualifizierter Pfad, der den Speicherort einer Datenträger Image Datei oder eines Verzeichnisses angibt, in dem eine Datenträger Image Datei abgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb203-108">A fully-qualified path that specifies the location of a disk image file or a directory in which a disk image file might be placed.</span></span>

</dd> <dt>

<span data-ttu-id="fb203-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb203-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb203-110">Ein Verweis auf den Auftrag (kann NULL sein, wenn der Task erfolgreich abgeschlossen wurde).</span><span class="sxs-lookup"><span data-stu-id="fb203-110">A reference to the job (can be null if the task is completed succesfully).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb203-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb203-111">Return value</span></span>

<span data-ttu-id="fb203-112">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="fb203-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="fb203-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="fb203-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="fb203-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="fb203-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="fb203-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="fb203-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="fb203-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="fb203-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="fb203-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="fb203-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="fb203-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="fb203-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="fb203-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="fb203-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fb203-126">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="fb203-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fb203-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb203-127">Requirements</span></span>



| <span data-ttu-id="fb203-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb203-128">Requirement</span></span> | <span data-ttu-id="fb203-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fb203-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb203-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb203-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fb203-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fb203-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fb203-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb203-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fb203-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fb203-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fb203-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb203-134">Namespace</span></span><br/>                | <span data-ttu-id="fb203-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb203-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fb203-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fb203-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb203-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb203-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb203-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fb203-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb203-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb203-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb203-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb203-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb203-141">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="fb203-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




