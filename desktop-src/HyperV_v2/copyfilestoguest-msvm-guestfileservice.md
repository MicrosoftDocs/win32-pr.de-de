---
description: Dateien werden vom Hyper-V-Host auf den virtuellen Computer kopiert.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Msvm_GuestFileService:: copyfilestoguest-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350318"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a><span data-ttu-id="ede0d-103">MSVM \_ guestfileservice:: copyfilestoguest-Methode</span><span class="sxs-lookup"><span data-stu-id="ede0d-103">Msvm\_GuestFileService::CopyFilesToGuest method</span></span>

<span data-ttu-id="ede0d-104">Dateien werden vom Hyper-V-Host auf den virtuellen Computer kopiert.</span><span class="sxs-lookup"><span data-stu-id="ede0d-104">Copies files from the Hyper-V host to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ede0d-105">Syntax</span></span>


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a><span data-ttu-id="ede0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ede0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede0d-107">*Copyfiledeguestsettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ede0d-107">*CopyFileToGuestSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede0d-108">Ein Array von Instanzen der [**MSVM \_ copyfiledeguestsettingdata**](msvm-copyfiletoguestsettingdata.md) -Klasse, das einen Gast Datei Dienst-Vorgangs Auftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="ede0d-108">An array of instances of the [**Msvm\_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) class that represents a guest file service operation job.</span></span>

</dd> <dt>

<span data-ttu-id="ede0d-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ede0d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ede0d-110">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ede0d-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="ede0d-111">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="ede0d-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="ede0d-112">Dieser Parameter wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ede0d-112">This parameter was added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="ede0d-113">"Parser"- *Pools* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="ede0d-113">*ParentPools* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ede0d-114">Ein optionales Array von [**MSVM \_ copyfiledeguestjob**](msvm-copyfiletoguestjob.md) -verweisen, die zum Überwachen des Fortschritts des Vorgangs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ede0d-114">An optional array of [**Msvm\_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) references that are used for monitoring progress of the operation.</span></span> <span data-ttu-id="ede0d-115">**Copyfilestoguest** verwendet *para Pools* , wenn es nicht synchron ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ede0d-115">**CopyFilesToGuest** uses *ParentPools* if it can't execute synchronously.</span></span> <span data-ttu-id="ede0d-116">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="ede0d-116">If the operation executes asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="ede0d-117">Dieser Parameter wurde in Windows 10 entfernt.</span><span class="sxs-lookup"><span data-stu-id="ede0d-117">This parameter was removed in Windows 10.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede0d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ede0d-118">Return value</span></span>

<span data-ttu-id="ede0d-119">Bei Erfolg wird 0 zurückgegeben. Andernfalls wird ein Fehlerwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ede0d-119">On success, returns 0; otherwise, returns an error value.</span></span>

<dl> <dt>

<span data-ttu-id="ede0d-120">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ede0d-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="ede0d-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-122">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="ede0d-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-123">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="ede0d-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-124">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="ede0d-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-125">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="ede0d-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ede0d-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-127">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="ede0d-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-128">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="ede0d-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-129">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="ede0d-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-130">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="ede0d-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-131">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="ede0d-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ede0d-132">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="ede0d-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ede0d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ede0d-133">Requirements</span></span>



| <span data-ttu-id="ede0d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ede0d-134">Requirement</span></span> | <span data-ttu-id="ede0d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ede0d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ede0d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ede0d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ede0d-137">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="ede0d-137">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ede0d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ede0d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ede0d-139">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ede0d-139">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ede0d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ede0d-140">Namespace</span></span><br/>                | <span data-ttu-id="ede0d-141">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ede0d-141">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="ede0d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ede0d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ede0d-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ede0d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ede0d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ede0d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ede0d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ede0d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ede0d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ede0d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede0d-147">**MSVM \_ guestfileservice**</span><span class="sxs-lookup"><span data-stu-id="ede0d-147">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> </dl>

 

 




