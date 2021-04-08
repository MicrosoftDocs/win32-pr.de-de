---
description: Ruft den Fehler ab.
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: GetError-Methode der Msvm_StorageJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7d8ff9c2c01bb21343b4859e2db2dbed7ad643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866396"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="6a1e3-103">GetError-Methode der MSVM \_ storagejob-Klasse</span><span class="sxs-lookup"><span data-stu-id="6a1e3-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="6a1e3-104">Ruft den Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="6a1e3-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a1e3-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="6a1e3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a1e3-107">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a1e3-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a1e3-108">Der abgerufene Fehler.</span><span class="sxs-lookup"><span data-stu-id="6a1e3-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a1e3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a1e3-109">Return value</span></span>

<span data-ttu-id="6a1e3-110">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="6a1e3-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6a1e3-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-112">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="6a1e3-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-113">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-114">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-115">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="6a1e3-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-117">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-118">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="6a1e3-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-119">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="6a1e3-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-120">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="6a1e3-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-121">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="6a1e3-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6a1e3-122">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6a1e3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a1e3-123">Requirements</span></span>



| <span data-ttu-id="6a1e3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a1e3-124">Requirement</span></span> | <span data-ttu-id="6a1e3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6a1e3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1e3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6a1e3-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a1e3-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6a1e3-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a1e3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6a1e3-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a1e3-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6a1e3-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a1e3-130">Namespace</span></span><br/>                | <span data-ttu-id="6a1e3-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a1e3-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a1e3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6a1e3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a1e3-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6a1e3-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a1e3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6a1e3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a1e3-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a1e3-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a1e3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a1e3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1e3-137">**MSVM \_ storagejob**</span><span class="sxs-lookup"><span data-stu-id="6a1e3-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




