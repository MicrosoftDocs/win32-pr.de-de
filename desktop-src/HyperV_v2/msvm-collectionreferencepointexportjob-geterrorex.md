---
description: 'GetErrorEx-Methode der Msvm_CollectionReferencePointExportJob-Klasse: Ruft zusätzliche Informationen zu einem Fehler ab.'
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: GetErrorEx-Methode der Msvm_CollectionReferencePointExportJob-Klasse
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
ms.openlocfilehash: 3b84c41776c081c302078773d9402145b0fe41e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112088"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="b62eb-103">GetErrorEx-Methode der Msvm \_ CollectionReferencePointExportJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="b62eb-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="b62eb-104">Ruft zusätzliche Informationen zu einem Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="b62eb-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="b62eb-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt **GetErrorEx** keine [**Msvm \_ Error-Instanz**](msvm-error.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="b62eb-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="b62eb-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, gibt **GetErrorEx** eine oder mehrere **Msvm-Fehlerinstanzen \_** zurück.</span><span class="sxs-lookup"><span data-stu-id="b62eb-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="b62eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b62eb-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="b62eb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b62eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b62eb-109">*Fehler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b62eb-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b62eb-110">Wenn der Betriebsstatus des Auftrags nicht "OK" lautet, gibt dieser Parameter ein Array von [**\_ Msvm-Fehlerinstanzen**](msvm-error.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="b62eb-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="b62eb-111">Andernfalls enthält dieser Parameter **NULL,** wenn der Auftrag "OK" ist.</span><span class="sxs-lookup"><span data-stu-id="b62eb-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b62eb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b62eb-112">Return value</span></span>

<span data-ttu-id="b62eb-113">Bei Erfolg wird 0 zurückgegeben. andernfalls wird einer der folgenden Fehlerwerte zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="b62eb-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="b62eb-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b62eb-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-115">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="b62eb-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="b62eb-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="b62eb-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-118">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="b62eb-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b62eb-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="b62eb-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="b62eb-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-122">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="b62eb-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-123">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="b62eb-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-124">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="b62eb-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b62eb-125">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="b62eb-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b62eb-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b62eb-126">Requirements</span></span>



| <span data-ttu-id="b62eb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b62eb-127">Requirement</span></span> | <span data-ttu-id="b62eb-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b62eb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b62eb-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b62eb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b62eb-130">Windows 10 Desktop-Apps, Version 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="b62eb-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b62eb-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b62eb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b62eb-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b62eb-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b62eb-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b62eb-133">Namespace</span></span><br/>                | <span data-ttu-id="b62eb-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b62eb-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b62eb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b62eb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b62eb-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b62eb-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b62eb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b62eb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b62eb-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b62eb-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b62eb-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b62eb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b62eb-140">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="b62eb-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




