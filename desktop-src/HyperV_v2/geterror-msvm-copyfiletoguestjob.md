---
description: 'Msvm_CopyFileToGuestJob::GetError-Methode: Ruft das Fehlerobjekt für den Auftrag ab, sofern vorhanden.'
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: Msvm_CopyFileToGuestJob::GetError-Methode
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
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119368"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="fdf33-103">Msvm \_ CopyFileToGuestJob::GetError-Methode</span><span class="sxs-lookup"><span data-stu-id="fdf33-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="fdf33-104">Ruft das Fehlerobjekt für den Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fdf33-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="fdf33-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode kein [**\_ CIM-Fehlerobjekt**](/previous-versions//cc150671(v=vs.85)) zurück.</span><span class="sxs-lookup"><span data-stu-id="fdf33-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="fdf33-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird eine **\_ CIM-Fehlerinstanz** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fdf33-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf33-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdf33-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="fdf33-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf33-109">*Fehler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fdf33-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf33-110">Wenn der Betriebsstatus des Auftrags nicht 2 (OK) lautet, gibt diese Methode eine eingebettete Instanz der [**Msvm \_ Error-Klasse**](msvm-error.md) im CIM-XML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="fdf33-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="fdf33-111">Wenn der Betriebsstatus des Auftrags 2 (OK) lautet, wird **NULL** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fdf33-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf33-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdf33-112">Return value</span></span>

<span data-ttu-id="fdf33-113">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="fdf33-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fdf33-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="fdf33-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-115">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="fdf33-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="fdf33-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="fdf33-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-118">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="fdf33-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="fdf33-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="fdf33-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="fdf33-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-122">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="fdf33-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-123">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="fdf33-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-124">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="fdf33-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fdf33-125">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="fdf33-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fdf33-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdf33-126">Requirements</span></span>



| <span data-ttu-id="fdf33-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdf33-127">Requirement</span></span> | <span data-ttu-id="fdf33-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fdf33-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf33-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fdf33-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf33-130">Windows 8.1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdf33-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fdf33-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fdf33-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf33-132">Nur Windows Server 2012 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fdf33-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fdf33-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdf33-133">Namespace</span></span><br/>                | <span data-ttu-id="fdf33-134">\\\\Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="fdf33-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="fdf33-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fdf33-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdf33-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdf33-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdf33-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fdf33-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdf33-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fdf33-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fdf33-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fdf33-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf33-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="fdf33-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

