---
description: 'GetError-Methode der Msvm_VirtualSystemReferencePointExportJob Klasse: Ruft den Fehler ab.'
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: GetError-Methode der Msvm_VirtualSystemReferencePointExportJob Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1311e4e56b6396266ece72277e8ddadcdb9d835
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109338"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="3cfbe-103">GetError-Methode der Msvm \_ VirtualSystemReferencePointExportJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="3cfbe-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="3cfbe-104">Ruft den Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="3cfbe-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cfbe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cfbe-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="3cfbe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cfbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cfbe-107">*Fehler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3cfbe-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfbe-108">Der abgerufene Fehler.</span><span class="sxs-lookup"><span data-stu-id="3cfbe-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cfbe-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cfbe-109">Return value</span></span>

<span data-ttu-id="3cfbe-110">Bei Erfolg gibt eine 0 zurück. andernfalls enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="3cfbe-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="3cfbe-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-112">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-113">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-114">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-115">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-117">**Ungültiger** Parameter (32773)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-118">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-119">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-120">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-121">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3cfbe-122">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3cfbe-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cfbe-123">Requirements</span></span>



| <span data-ttu-id="3cfbe-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cfbe-124">Requirement</span></span> | <span data-ttu-id="3cfbe-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3cfbe-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cfbe-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3cfbe-127">Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]</span><span class="sxs-lookup"><span data-stu-id="3cfbe-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3cfbe-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cfbe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3cfbe-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3cfbe-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3cfbe-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cfbe-130">Namespace</span></span><br/>                | <span data-ttu-id="3cfbe-131">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3cfbe-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3cfbe-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3cfbe-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cfbe-133"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cfbe-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cfbe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3cfbe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cfbe-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cfbe-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3cfbe-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3cfbe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cfbe-137">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="3cfbe-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




