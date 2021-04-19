---
description: Legt die Schlüssel Schutzvorrichtung für ein virtuelles System fest.
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: Setkeyprotector-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 404baf0a529a6e96869fbcd355a81308f5d1e966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348224"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="3591d-103">Setkeyprotector-Methode der MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="3591d-103">SetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="3591d-104">Legt die Schlüssel Schutzvorrichtung für ein virtuelles System fest.</span><span class="sxs-lookup"><span data-stu-id="3591d-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3591d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3591d-105">Syntax</span></span>


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3591d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3591d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3591d-107">*Securitysettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3591d-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3591d-108">Die Zeichenfolge enthält eine eingebettete Instanz der [**MSVM \_ securitysettingdata**](msvm-securitysettingdata.md) -Klasse, die die Sicherheitseinstellungen eines virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="3591d-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="3591d-109">*Keyprotector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3591d-109">*KeyProtector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3591d-110">Rohbytearray, das die festzulegende Schlüssel Schutzvorrichtung enthält.</span><span class="sxs-lookup"><span data-stu-id="3591d-110">Raw byte array that contains the key protector to set.</span></span>

</dd> <dt>

<span data-ttu-id="3591d-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3591d-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3591d-112">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="3591d-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="3591d-113">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="3591d-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3591d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3591d-114">Return value</span></span>

<span data-ttu-id="3591d-115">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3591d-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3591d-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3591d-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3591d-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3591d-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3591d-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3591d-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3591d-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3591d-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3591d-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="3591d-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3591d-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3591d-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3591d-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3591d-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3591d-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3591d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3591d-129">Requirements</span></span>



| <span data-ttu-id="3591d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3591d-130">Requirement</span></span> | <span data-ttu-id="3591d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3591d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3591d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3591d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3591d-133">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3591d-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3591d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3591d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3591d-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3591d-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3591d-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3591d-136">Namespace</span></span><br/>                | <span data-ttu-id="3591d-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3591d-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3591d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3591d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3591d-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3591d-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3591d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3591d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3591d-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3591d-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3591d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3591d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3591d-143">**MSVM- \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="3591d-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




