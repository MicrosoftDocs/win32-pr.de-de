---
description: Legt die Schlüssel Schutzvorrichtung für ein virtuelles System fest.
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Setsecuritypolicy-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 35954f27d1184b714091058a35f32a6347d4ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530380"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="46300-103">Setsecuritypolicy-Methode der MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="46300-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="46300-104">Legt die Schlüssel Schutzvorrichtung für ein virtuelles System fest.</span><span class="sxs-lookup"><span data-stu-id="46300-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="46300-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46300-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="46300-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46300-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46300-107">*Securitysettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46300-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46300-108">Die Zeichenfolge enthält eine eingebettete Instanz der [**MSVM \_ securitysettingdata**](msvm-securitysettingdata.md) -Klasse, die die Sicherheitseinstellungen eines virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="46300-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="46300-109">*SecurityPolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46300-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46300-110">Unformatierte Bytearray, das die festzulegende Sicherheitsrichtlinie enthält.</span><span class="sxs-lookup"><span data-stu-id="46300-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="46300-111">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="46300-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46300-112">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="46300-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="46300-113">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="46300-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46300-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46300-114">Return value</span></span>

<span data-ttu-id="46300-115">Bei, Erfolg, wird 0 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46300-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="46300-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="46300-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46300-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="46300-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="46300-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="46300-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="46300-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="46300-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="46300-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="46300-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="46300-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="46300-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="46300-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="46300-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="46300-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="46300-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="46300-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="46300-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="46300-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="46300-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="46300-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="46300-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="46300-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="46300-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="46300-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="46300-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="46300-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46300-129">Requirements</span></span>



| <span data-ttu-id="46300-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46300-130">Requirement</span></span> | <span data-ttu-id="46300-131">Wert</span><span class="sxs-lookup"><span data-stu-id="46300-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46300-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46300-132">Minimum supported client</span></span><br/> | <span data-ttu-id="46300-133">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46300-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="46300-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46300-134">Minimum supported server</span></span><br/> | <span data-ttu-id="46300-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="46300-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="46300-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="46300-136">Namespace</span></span><br/>                | <span data-ttu-id="46300-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="46300-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="46300-138">MOF</span><span class="sxs-lookup"><span data-stu-id="46300-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46300-139"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46300-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46300-140">DLL</span><span class="sxs-lookup"><span data-stu-id="46300-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46300-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46300-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46300-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46300-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46300-143">**MSVM- \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="46300-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




