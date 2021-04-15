---
description: Erstellt einen Referenzpunkt einer Sammlung virtueller Systeme.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Die Methode "kreatereferencepoint" der Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350318"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="64f02-103">Die Methode "kreatereferencepoint" der Klasse "MSVM \_ collectionreferencepointservice"</span><span class="sxs-lookup"><span data-stu-id="64f02-103">CreateReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="64f02-104">Erstellt einen Referenzpunkt einer Sammlung virtueller Systeme.</span><span class="sxs-lookup"><span data-stu-id="64f02-104">Creates a reference point of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f02-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="64f02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f02-107">*Sammlung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f02-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f02-108">Verweis auf die betroffene Auflistung von virtuellen Systemen.</span><span class="sxs-lookup"><span data-stu-id="64f02-108">Reference to the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="64f02-109">*Referencepointsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f02-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f02-110">Parameter Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="64f02-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="64f02-111">*Referencepointtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f02-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f02-112">Gibt den Typ des Bezugspunkts an.</span><span class="sxs-lookup"><span data-stu-id="64f02-112">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64f02-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="64f02-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="64f02-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Protokoll basiert** (1)</span><span class="sxs-lookup"><span data-stu-id="64f02-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="64f02-115">Protokoll Nachverfolgung für Hyper-V-Replikate.</span><span class="sxs-lookup"><span data-stu-id="64f02-115">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="64f02-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basiert** (2)</span><span class="sxs-lookup"><span data-stu-id="64f02-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="64f02-117">Basierend auf robusten Änderungsnachverfolgung von virtuellen Datenträgern.</span><span class="sxs-lookup"><span data-stu-id="64f02-117">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="64f02-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="64f02-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="64f02-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="64f02-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="64f02-120">*Resultingreferencepointcollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="64f02-120">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f02-121">Der resultierende Bezugspunkt einer Sammlung virtueller Systeme.</span><span class="sxs-lookup"><span data-stu-id="64f02-121">Resulting reference point of a virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="64f02-122">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64f02-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f02-123">Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64f02-123">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f02-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f02-124">Return value</span></span>

<span data-ttu-id="64f02-125">Wenn erfolgreich, wird entweder 0 (kein Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64f02-125">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="64f02-126">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="64f02-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-127">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="64f02-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-128">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="64f02-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-129">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="64f02-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-130">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="64f02-130">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-131">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="64f02-131">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-132">**Ungültiger Typ** (6)</span><span class="sxs-lookup"><span data-stu-id="64f02-132">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-133">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="64f02-133">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-134">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="64f02-134">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-135">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="64f02-135">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="64f02-136">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="64f02-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="64f02-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f02-137">Requirements</span></span>



| <span data-ttu-id="64f02-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f02-138">Requirement</span></span> | <span data-ttu-id="64f02-139">Wert</span><span class="sxs-lookup"><span data-stu-id="64f02-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f02-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64f02-140">Minimum supported client</span></span><br/> | <span data-ttu-id="64f02-141">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64f02-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="64f02-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64f02-142">Minimum supported server</span></span><br/> | <span data-ttu-id="64f02-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="64f02-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="64f02-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="64f02-144">Namespace</span></span><br/>                | <span data-ttu-id="64f02-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="64f02-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64f02-146">MOF</span><span class="sxs-lookup"><span data-stu-id="64f02-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64f02-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="64f02-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64f02-148">DLL</span><span class="sxs-lookup"><span data-stu-id="64f02-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64f02-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64f02-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64f02-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f02-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f02-151">**MSVM \_ collectionreferencepointservice**</span><span class="sxs-lookup"><span data-stu-id="64f02-151">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




