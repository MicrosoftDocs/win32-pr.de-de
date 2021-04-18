---
description: Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine MSVM- \_ Fehler Instanz zurück.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Geterrorex-Methode der Msvm_StorageJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347212"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="9ae3a-103">Geterrorex-Methode der MSVM \_ storagejob-Klasse</span><span class="sxs-lookup"><span data-stu-id="9ae3a-103">GetErrorEx method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="9ae3a-104">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**MSVM- \_ Fehler**](msvm-error.md) Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="9ae3a-104">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="9ae3a-105">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, werden mindestens eine **MSVM- \_ Fehler** Instanz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ae3a-105">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae3a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ae3a-106">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="9ae3a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ae3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae3a-108">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9ae3a-108">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ae3a-109">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="9ae3a-109">Type: **string\[\]**</span></span>

<span data-ttu-id="9ae3a-110">Wenn der Betriebsstatus des Auftrags nicht "OK" ist, gibt diese Methode ein Array von [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="9ae3a-110">If the operational status of the job is not "OK", this method returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="9ae3a-111">Andernfalls wird **null** zurückgegeben, wenn der Auftrag den Wert "OK" hat.</span><span class="sxs-lookup"><span data-stu-id="9ae3a-111">Otherwise, if the job is "OK", **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae3a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ae3a-112">Return value</span></span>

<span data-ttu-id="9ae3a-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ae3a-113">Type: **uint32**</span></span>

<span data-ttu-id="9ae3a-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9ae3a-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9ae3a-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="9ae3a-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="9ae3a-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-122">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="9ae3a-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="9ae3a-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="9ae3a-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="9ae3a-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9ae3a-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9ae3a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ae3a-127">Remarks</span></span>

<span data-ttu-id="9ae3a-128">Der Zugriff auf die [**MSVM \_ storagejob**](msvm-storagejob.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="9ae3a-128">Access to the [**Msvm\_StorageJob**](msvm-storagejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9ae3a-129">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9ae3a-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae3a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ae3a-130">Requirements</span></span>



| <span data-ttu-id="9ae3a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ae3a-131">Requirement</span></span> | <span data-ttu-id="9ae3a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9ae3a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae3a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae3a-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ae3a-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9ae3a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ae3a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae3a-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ae3a-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9ae3a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ae3a-137">Namespace</span></span><br/>                | <span data-ttu-id="9ae3a-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9ae3a-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9ae3a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9ae3a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ae3a-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9ae3a-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ae3a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae3a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ae3a-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9ae3a-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9ae3a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ae3a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae3a-144">**MSVM \_ storagejob**</span><span class="sxs-lookup"><span data-stu-id="9ae3a-144">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

