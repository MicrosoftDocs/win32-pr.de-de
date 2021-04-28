---
description: 'GetErrorEx-Methode der Msvm_VirtualSystemReferencePointExportJob-Klasse: Ruft zusätzliche Informationen zu einem Fehler ab.'
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: GetErrorEx-Methode der Msvm_VirtualSystemReferencePointExportJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80e0850018b20497dbc42bbdbb802ffe4317489b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118608"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="e2cd6-103">GetErrorEx-Methode der Msvm \_ VirtualSystemReferencePointExportJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2cd6-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="e2cd6-104">Ruft zusätzliche Informationen zu einem Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="e2cd6-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="e2cd6-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt **GetErrorEx** keine **GetErrorEx-Instanz** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2cd6-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="e2cd6-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, gibt **GetErrorEx** eine oder mehrere [**Msvm-Fehlerinstanzen \_**](msvm-error.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="e2cd6-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2cd6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2cd6-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="e2cd6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2cd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2cd6-109">*Fehler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e2cd6-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2cd6-110">Wenn der Betriebsstatus des Auftrags nicht "OK" lautet, gibt dieser Parameter ein Array von [**\_ Msvm-Fehlerinstanzen**](msvm-error.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="e2cd6-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="e2cd6-111">Andernfalls enthält dieser Parameter **NULL,** wenn der Auftrag "OK" ist.</span><span class="sxs-lookup"><span data-stu-id="e2cd6-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2cd6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2cd6-112">Return value</span></span>

<span data-ttu-id="e2cd6-113">Bei Erfolg wird 0 zurückgegeben. andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2cd6-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e2cd6-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-115">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-118">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-122">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-123">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-124">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e2cd6-125">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e2cd6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2cd6-126">Requirements</span></span>



| <span data-ttu-id="e2cd6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2cd6-127">Requirement</span></span> | <span data-ttu-id="e2cd6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e2cd6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2cd6-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e2cd6-130">Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]</span><span class="sxs-lookup"><span data-stu-id="e2cd6-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e2cd6-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2cd6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e2cd6-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e2cd6-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e2cd6-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2cd6-133">Namespace</span></span><br/>                | <span data-ttu-id="e2cd6-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e2cd6-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e2cd6-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e2cd6-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2cd6-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd6-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2cd6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e2cd6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2cd6-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd6-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2cd6-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2cd6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2cd6-140">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="e2cd6-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




