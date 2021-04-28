---
description: 'SetKeyProtector-Methode der Msvm_SecurityService-Klasse: Legt die Schlüsselschutzvorrichtung für ein virtuelles System fest.'
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: SetKeyProtector-Methode der Msvm_SecurityService-Klasse
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
ms.openlocfilehash: 3b5eca7ddcc506d158175782e3e13796e56de267
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111408"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="2d451-103">SetKeyProtector-Methode der Msvm \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="2d451-103">SetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="2d451-104">Legt die Schlüsselschutzvorrichtung für ein virtuelles System fest.</span><span class="sxs-lookup"><span data-stu-id="2d451-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d451-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d451-105">Syntax</span></span>


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2d451-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d451-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d451-107">*SecuritySettingData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2d451-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d451-108">String enthält eine eingebettete Instanz der [**Msvm \_ SecuritySettingData-Klasse,**](msvm-securitysettingdata.md) die die Sicherheitseinstellungen eines virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d451-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="2d451-109">*KeyProtector* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2d451-109">*KeyProtector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d451-110">Unformatiertes Bytearray, das die festzulegende Schlüsselschutzvorrichtung enthält.</span><span class="sxs-lookup"><span data-stu-id="2d451-110">Raw byte array that contains the key protector to set.</span></span>

</dd> <dt>

<span data-ttu-id="2d451-111">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2d451-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d451-112">Ein optionaler Parameter zum Überwachen des Vorgangsfortschritts, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="2d451-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="2d451-113">Wenn der Vorgang asynchron ausgeführt wird, lautet der Rückgabewert 4096.</span><span class="sxs-lookup"><span data-stu-id="2d451-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d451-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d451-114">Return value</span></span>

<span data-ttu-id="2d451-115">Gibt bei Erfolg 0 oder 4096 zurück. andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2d451-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2d451-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="2d451-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-117">**Methodenparameter überprüft** – Auftrag gestartet (4096)</span><span class="sxs-lookup"><span data-stu-id="2d451-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-118">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="2d451-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="2d451-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="2d451-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-121">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="2d451-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="2d451-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="2d451-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="2d451-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-125">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="2d451-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-126">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="2d451-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-127">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="2d451-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2d451-128">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="2d451-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2d451-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d451-129">Requirements</span></span>



| <span data-ttu-id="2d451-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d451-130">Requirement</span></span> | <span data-ttu-id="2d451-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2d451-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d451-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d451-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2d451-133">Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]</span><span class="sxs-lookup"><span data-stu-id="2d451-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2d451-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d451-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2d451-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2d451-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2d451-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d451-136">Namespace</span></span><br/>                | <span data-ttu-id="2d451-137">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d451-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d451-138">MOF</span><span class="sxs-lookup"><span data-stu-id="2d451-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d451-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d451-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d451-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2d451-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d451-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d451-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d451-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2d451-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d451-143">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="2d451-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




