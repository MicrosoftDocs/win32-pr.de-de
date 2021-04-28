---
description: 'Msvm_CopyFileToGuestJob::GetErrorEx-Methode: Ruft die Fehlerobjekte für den Auftrag ab, sofern vorhanden.'
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: Msvm_CopyFileToGuestJob::GetErrorEx-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81a570c42457257212e83f9c0c034c4a390e4c04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109668"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="13614-103">Msvm \_ CopyFileToGuestJob::GetErrorEx-Methode</span><span class="sxs-lookup"><span data-stu-id="13614-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="13614-104">Ruft die Fehlerobjekte für den Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="13614-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="13614-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**Msvm \_ Error-Instanz**](msvm-error.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="13614-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="13614-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird mindestens eine **Msvm \_ Error-Instanz** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13614-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="13614-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="13614-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="13614-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="13614-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13614-109">*Fehler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="13614-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13614-110">Wenn der Betriebsstatus des Auftrags nicht 2 (OK) ist, gibt diese Methode mindestens eine eingebettete Instanz der [**Msvm \_ Error-Klasse**](msvm-error.md) im CIM-XML-Format zurück, die die im Auftrag aufgetretenen Fehler darstellen.</span><span class="sxs-lookup"><span data-stu-id="13614-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="13614-111">Wenn der Betriebsstatus des Auftrags 2 (OK) ist, wird **NULL** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13614-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13614-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13614-112">Return value</span></span>

<span data-ttu-id="13614-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="13614-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="13614-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="13614-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13614-115">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="13614-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="13614-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="13614-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="13614-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="13614-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="13614-118">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="13614-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="13614-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="13614-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="13614-120">**Ungültiger** Parameter (32773)</span><span class="sxs-lookup"><span data-stu-id="13614-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="13614-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="13614-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="13614-122">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="13614-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="13614-123">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="13614-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="13614-124">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="13614-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="13614-125">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="13614-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="13614-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13614-126">Requirements</span></span>



| <span data-ttu-id="13614-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13614-127">Requirement</span></span> | <span data-ttu-id="13614-128">Wert</span><span class="sxs-lookup"><span data-stu-id="13614-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13614-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13614-129">Minimum supported client</span></span><br/> | <span data-ttu-id="13614-130">nur Windows 8.1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13614-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="13614-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13614-131">Minimum supported server</span></span><br/> | <span data-ttu-id="13614-132">Nur Windows Server 2012 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13614-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="13614-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="13614-133">Namespace</span></span><br/>                | <span data-ttu-id="13614-134">\\\\Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="13614-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="13614-135">MOF</span><span class="sxs-lookup"><span data-stu-id="13614-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13614-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="13614-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13614-137">DLL</span><span class="sxs-lookup"><span data-stu-id="13614-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13614-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13614-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13614-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13614-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13614-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="13614-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




