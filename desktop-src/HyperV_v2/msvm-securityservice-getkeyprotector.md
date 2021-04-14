---
description: Ruft die Schlüssel Schutzvorrichtung für ein virtuelles System ab.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Getkeyprotector-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350649"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="1ad09-103">Getkeyprotector-Methode der MSVM \_ SecurityService-Klasse</span><span class="sxs-lookup"><span data-stu-id="1ad09-103">GetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="1ad09-104">Ruft die Schlüssel Schutzvorrichtung für ein virtuelles System ab.</span><span class="sxs-lookup"><span data-stu-id="1ad09-104">Retrieves the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ad09-105">Syntax</span></span>


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a><span data-ttu-id="1ad09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ad09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad09-107">*Securitysettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ad09-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad09-108">Die Zeichenfolge enthält eine eingebettete Instanz der [**MSVM \_ securitysettingdata**](msvm-securitysettingdata.md) -Klasse, die die Sicherheitseinstellungen eines virtuellen Systems darstellt.</span><span class="sxs-lookup"><span data-stu-id="1ad09-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="1ad09-109">*Keyprotector* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1ad09-109">*KeyProtector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ad09-110">Empfängt das rohbytearray, das die derzeit verwendete Schlüssel Schutzvorrichtung enthält.</span><span class="sxs-lookup"><span data-stu-id="1ad09-110">Receives the raw byte array that contains the key protector currently in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ad09-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ad09-111">Return value</span></span>

<span data-ttu-id="1ad09-112">Bei Erfolg wird 0 oder 4096 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1ad09-112">On success, returns a 0 or 4096.</span></span> <span data-ttu-id="1ad09-113">Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1ad09-113">Otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1ad09-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="1ad09-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="1ad09-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="1ad09-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="1ad09-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="1ad09-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="1ad09-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="1ad09-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="1ad09-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-122">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="1ad09-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="1ad09-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="1ad09-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="1ad09-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1ad09-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="1ad09-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1ad09-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ad09-127">Requirements</span></span>



| <span data-ttu-id="1ad09-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ad09-128">Requirement</span></span> | <span data-ttu-id="1ad09-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1ad09-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad09-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ad09-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad09-131">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ad09-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1ad09-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ad09-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad09-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1ad09-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1ad09-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ad09-134">Namespace</span></span><br/>                | <span data-ttu-id="1ad09-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ad09-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1ad09-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1ad09-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ad09-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ad09-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ad09-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1ad09-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ad09-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ad09-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ad09-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ad09-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad09-141">**MSVM- \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="1ad09-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




