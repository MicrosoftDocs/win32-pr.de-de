---
description: Ruft zusätzliche Informationen zu einem Fehler ab.
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: Geterrorex-Methode der Msvm_VirtualSystemReferencePointExportJob-Klasse
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
ms.openlocfilehash: 4c6c392adb2b638c2d638b758696252adcb54d7e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106367271"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="62d76-103">Geterrorex-Methode der MSVM \_ virtualsystemreferencepointexportjob-Klasse</span><span class="sxs-lookup"><span data-stu-id="62d76-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="62d76-104">Ruft zusätzliche Informationen zu einem Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="62d76-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="62d76-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt **geterrorex** keine **geterrorex** -Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="62d76-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="62d76-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, gibt **geterrorex** mindestens eine [**MSVM- \_ Fehler**](msvm-error.md) Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="62d76-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d76-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62d76-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="62d76-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62d76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d76-109">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62d76-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62d76-110">Wenn der Betriebsstatus des Auftrags nicht "OK" ist, gibt dieser Parameter ein Array von [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="62d76-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="62d76-111">Andernfalls enthält dieser Parameter **null**, wenn der Auftrag "OK" ist.</span><span class="sxs-lookup"><span data-stu-id="62d76-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62d76-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62d76-112">Return value</span></span>

<span data-ttu-id="62d76-113">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62d76-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="62d76-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="62d76-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="62d76-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="62d76-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="62d76-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="62d76-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="62d76-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="62d76-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-121">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="62d76-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="62d76-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="62d76-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="62d76-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="62d76-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="62d76-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="62d76-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62d76-126">Requirements</span></span>



| <span data-ttu-id="62d76-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62d76-127">Requirement</span></span> | <span data-ttu-id="62d76-128">Wert</span><span class="sxs-lookup"><span data-stu-id="62d76-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d76-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62d76-129">Minimum supported client</span></span><br/> | <span data-ttu-id="62d76-130">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62d76-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="62d76-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62d76-131">Minimum supported server</span></span><br/> | <span data-ttu-id="62d76-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="62d76-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="62d76-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="62d76-133">Namespace</span></span><br/>                | <span data-ttu-id="62d76-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="62d76-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62d76-135">MOF</span><span class="sxs-lookup"><span data-stu-id="62d76-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62d76-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62d76-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62d76-137">DLL</span><span class="sxs-lookup"><span data-stu-id="62d76-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62d76-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62d76-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62d76-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62d76-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d76-140">**MSVM \_ virtualsystemreferencepointexportjob**</span><span class="sxs-lookup"><span data-stu-id="62d76-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




