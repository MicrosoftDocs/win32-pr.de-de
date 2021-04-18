---
description: Ruft zusätzliche Informationen zu einem Fehler ab.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Geterrorex-Methode der Msvm_CollectionReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352390"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="862b3-103">Geterrorex-Methode der MSVM \_ collectionreferencepointexportjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="862b3-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="862b3-104">Ruft zusätzliche Informationen zu einem Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="862b3-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="862b3-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt **geterrorex** keine [**MSVM- \_ Fehler**](msvm-error.md) Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="862b3-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="862b3-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, gibt **geterrorex** mindestens eine **MSVM- \_ Fehler** Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="862b3-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="862b3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="862b3-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="862b3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="862b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="862b3-109">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="862b3-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="862b3-110">Wenn der Betriebsstatus des Auftrags nicht "OK" ist, gibt dieser Parameter ein Array von [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="862b3-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="862b3-111">Andernfalls enthält dieser Parameter **null**, wenn der Auftrag "OK" ist.</span><span class="sxs-lookup"><span data-stu-id="862b3-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="862b3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="862b3-112">Return value</span></span>

<span data-ttu-id="862b3-113">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird einer der folgenden Fehler Werte zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="862b3-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="862b3-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="862b3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="862b3-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="862b3-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="862b3-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="862b3-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="862b3-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="862b3-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-121">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="862b3-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="862b3-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="862b3-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="862b3-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="862b3-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="862b3-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="862b3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="862b3-126">Requirements</span></span>



| <span data-ttu-id="862b3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="862b3-127">Requirement</span></span> | <span data-ttu-id="862b3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="862b3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="862b3-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="862b3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="862b3-130">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="862b3-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="862b3-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="862b3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="862b3-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="862b3-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="862b3-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="862b3-133">Namespace</span></span><br/>                | <span data-ttu-id="862b3-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="862b3-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="862b3-135">MOF</span><span class="sxs-lookup"><span data-stu-id="862b3-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="862b3-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="862b3-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="862b3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="862b3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="862b3-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="862b3-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="862b3-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="862b3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862b3-140">**MSVM \_ collectionreferencepointexportjob**</span><span class="sxs-lookup"><span data-stu-id="862b3-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




