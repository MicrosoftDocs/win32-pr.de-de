---
description: Wiederherstellung bis zur letzten als funktionierend bekannten Schlüssel Schutzvorrichtung.
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Restorelastknowngoodkeyprotector-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349737"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="28fc3-103">Restorelastknowngoodkeyprotector-Methode der MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="28fc3-103">RestoreLastKnownGoodKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="28fc3-104">Wiederherstellung bis zur letzten als funktionierend bekannten Schlüssel Schutzvorrichtung.</span><span class="sxs-lookup"><span data-stu-id="28fc3-104">Restores back to the last known good key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fc3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28fc3-105">Syntax</span></span>


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="28fc3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28fc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28fc3-107">*Securitysettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28fc3-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28fc3-108">Die Zeichenfolge enthält eine eingebettete Instanz der [**MSVM \_ securitysettingdata**](msvm-securitysettingdata.md) -Klasse, die die Sicherheitseinstellungen eines virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="28fc3-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="28fc3-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="28fc3-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28fc3-110">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="28fc3-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="28fc3-111">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="28fc3-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28fc3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28fc3-112">Return value</span></span>

<span data-ttu-id="28fc3-113">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28fc3-113">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="28fc3-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="28fc3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="28fc3-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="28fc3-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="28fc3-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="28fc3-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="28fc3-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="28fc3-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="28fc3-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="28fc3-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="28fc3-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="28fc3-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="28fc3-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="28fc3-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="28fc3-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="28fc3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28fc3-127">Requirements</span></span>



| <span data-ttu-id="28fc3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28fc3-128">Requirement</span></span> | <span data-ttu-id="28fc3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="28fc3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28fc3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28fc3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28fc3-131">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28fc3-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28fc3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28fc3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28fc3-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="28fc3-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="28fc3-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="28fc3-134">Namespace</span></span><br/>                | <span data-ttu-id="28fc3-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="28fc3-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="28fc3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="28fc3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28fc3-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="28fc3-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28fc3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="28fc3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28fc3-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28fc3-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28fc3-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28fc3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fc3-141">**MSVM- \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="28fc3-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




