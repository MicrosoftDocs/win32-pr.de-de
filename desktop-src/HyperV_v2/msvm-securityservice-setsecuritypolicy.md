---
description: 'SetSecurityPolicy-Methode der Msvm_SecurityService Klasse: Legt die Schlüsselschutzvorrichtung für ein virtuelles System fest.'
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: SetSecurityPolicy-Methode der Msvm_SecurityService Klasse
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
ms.openlocfilehash: 31b03ee8a941b0715b85f6a749c4ba59ade032f7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118728"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="b56a6-103">SetSecurityPolicy-Methode der Msvm \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="b56a6-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="b56a6-104">Legt die Schlüsselschutzvorrichtung für ein virtuelles System fest.</span><span class="sxs-lookup"><span data-stu-id="b56a6-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b56a6-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b56a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b56a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56a6-107">*SecuritySettingData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b56a6-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56a6-108">Die Zeichenfolge enthält eine eingebettete Instanz der [**Msvm \_ SecuritySettingData-Klasse,**](msvm-securitysettingdata.md) die die Sicherheitseinstellungen eines virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="b56a6-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="b56a6-109">*SecurityPolicy* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b56a6-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b56a6-110">Unformatiertes Bytearray mit der festgelegten Sicherheitsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b56a6-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="b56a6-111">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b56a6-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b56a6-112">Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b56a6-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="b56a6-113">Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="b56a6-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56a6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b56a6-114">Return value</span></span>

<span data-ttu-id="b56a6-115">On, success, gibt eine 0 zurück. andernfalls gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b56a6-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b56a6-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="b56a6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-117">**Überprüfte Methodenparameter – Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="b56a6-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-118">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="b56a6-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="b56a6-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="b56a6-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-121">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="b56a6-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b56a6-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-123">**Ungültiger** Parameter (32773)</span><span class="sxs-lookup"><span data-stu-id="b56a6-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="b56a6-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-125">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="b56a6-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-126">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="b56a6-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-127">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="b56a6-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b56a6-128">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="b56a6-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b56a6-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b56a6-129">Requirements</span></span>



| <span data-ttu-id="b56a6-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b56a6-130">Requirement</span></span> | <span data-ttu-id="b56a6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b56a6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56a6-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b56a6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b56a6-133">Windows 10, nur Desktop-Apps der Version 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="b56a6-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b56a6-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b56a6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b56a6-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b56a6-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b56a6-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="b56a6-136">Namespace</span></span><br/>                | <span data-ttu-id="b56a6-137">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b56a6-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b56a6-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b56a6-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b56a6-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b56a6-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b56a6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b56a6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b56a6-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b56a6-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b56a6-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b56a6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56a6-143">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="b56a6-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




