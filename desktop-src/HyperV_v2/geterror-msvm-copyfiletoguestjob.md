---
description: Ruft das Fehler Objekt für den Auftrag ab, sofern vorhanden.
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Msvm_CopyFileToGuestJob:: GetError-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a0a89feab4e78ba3703e117972598c4de5f70310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360069"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="b445f-103">MSVM \_ copyfiledeguestjob:: GetError-Methode</span><span class="sxs-lookup"><span data-stu-id="b445f-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="b445f-104">Ruft das Fehler Objekt für den Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b445f-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="b445f-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode kein CIM- [**\_ Fehler**](/previous-versions//cc150671(v=vs.85)) Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b445f-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="b445f-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, wird eine CIM- **\_ Fehler** Instanz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b445f-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="b445f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b445f-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="b445f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b445f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b445f-109">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b445f-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b445f-110">Wenn der Betriebsstatus des Auftrags nicht 2 (OK) ist, gibt diese Methode eine eingebettete Instanz der [**MSVM- \_ Fehler**](msvm-error.md) Klasse im CIM-XML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="b445f-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="b445f-111">Wenn der Betriebsstatus des Auftrags 2 (OK) ist, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b445f-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b445f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b445f-112">Return value</span></span>

<span data-ttu-id="b445f-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b445f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b445f-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b445f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="b445f-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="b445f-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="b445f-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="b445f-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b445f-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="b445f-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-121">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="b445f-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="b445f-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="b445f-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="b445f-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b445f-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="b445f-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b445f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b445f-126">Requirements</span></span>



| <span data-ttu-id="b445f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b445f-127">Requirement</span></span> | <span data-ttu-id="b445f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b445f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b445f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b445f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b445f-130">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b445f-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b445f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b445f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b445f-132">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b445f-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b445f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b445f-133">Namespace</span></span><br/>                | <span data-ttu-id="b445f-134">\\\\\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b445f-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="b445f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b445f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b445f-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b445f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b445f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b445f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b445f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b445f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b445f-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b445f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b445f-140">**MSVM \_ copyfilein guestjob**</span><span class="sxs-lookup"><span data-stu-id="b445f-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

