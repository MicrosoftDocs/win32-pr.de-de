---
title: MDM_BitLocker-Klasse
description: Die MDM \_ -BitLocker-Klasse wird vom Unternehmen verwendet, um die Verschlüsselung von PCs und Geräten zu verwalten.
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- MDM_BitLocker-Klasse
- MDM_BitLocker-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106137"
---
# <a name="mdm_bitlocker-class"></a><span data-ttu-id="534ce-105">MDM- \_ BitLocker-Klasse</span><span class="sxs-lookup"><span data-stu-id="534ce-105">MDM\_BitLocker class</span></span>

<span data-ttu-id="534ce-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="534ce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="534ce-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="534ce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="534ce-108">Die MDM \_ -BitLocker-Klasse wird vom Unternehmen verwendet, um die Verschlüsselung von PCs und Geräten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="534ce-108">The MDM\_BitLocker class is used by the enterprise to manage encryption of PCs and devices.</span></span>

<span data-ttu-id="534ce-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="534ce-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="534ce-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="534ce-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a><span data-ttu-id="534ce-111">Member</span><span class="sxs-lookup"><span data-stu-id="534ce-111">Members</span></span>

<span data-ttu-id="534ce-112">Die **MDM- \_ BitLocker** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="534ce-112">The **MDM\_BitLocker** class has these types of members:</span></span>

-   [<span data-ttu-id="534ce-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="534ce-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="534ce-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="534ce-114">Properties</span></span>

<span data-ttu-id="534ce-115">Die **MDM- \_ BitLocker** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="534ce-115">The **MDM\_BitLocker** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="534ce-116">Allowwarningforotherdiskencryption</span><span class="sxs-lookup"><span data-stu-id="534ce-116">AllowWarningForOtherDiskEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="534ce-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-119">Verschlüsselungsmethodbydrivetype</span><span class="sxs-lookup"><span data-stu-id="534ce-119">EncryptionMethodByDriveType</span></span>](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-122">Fixeddrivesherstellyoptions</span><span class="sxs-lookup"><span data-stu-id="534ce-122">FixedDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-125">Fixeddrivesrequirements-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="534ce-125">FixedDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="534ce-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="534ce-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="534ce-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="534ce-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="534ce-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="534ce-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="534ce-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="534ce-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="534ce-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="534ce-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-136">Removabledrivesrequirements-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="534ce-136">RemovableDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-139">Requirements deviceencryption</span><span class="sxs-lookup"><span data-stu-id="534ce-139">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-140">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="534ce-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-142">Requirements storagecardencryption</span><span class="sxs-lookup"><span data-stu-id="534ce-142">RequireStorageCardEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-143">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="534ce-143">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-145">Systemdrivesminimumpinlength</span><span class="sxs-lookup"><span data-stu-id="534ce-145">SystemDrivesMinimumPINLength</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-148">Systemdriveswiederherstellbarkeits-</span><span class="sxs-lookup"><span data-stu-id="534ce-148">SystemDrivesRecoveryMessage</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-151">Systemdriveswiederherstellbarkeits Optionen</span><span class="sxs-lookup"><span data-stu-id="534ce-151">SystemDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="534ce-154">Systemdrivesrequirements startupauthentication</span><span class="sxs-lookup"><span data-stu-id="534ce-154">SystemDrivesRequireStartupAuthentication</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="534ce-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="534ce-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="534ce-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="534ce-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="534ce-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="534ce-157">Requirements</span></span>



| <span data-ttu-id="534ce-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="534ce-158">Requirement</span></span> | <span data-ttu-id="534ce-159">Wert</span><span class="sxs-lookup"><span data-stu-id="534ce-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="534ce-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="534ce-160">Minimum supported client</span></span><br/> | <span data-ttu-id="534ce-161">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="534ce-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="534ce-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="534ce-162">Minimum supported server</span></span><br/> | <span data-ttu-id="534ce-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="534ce-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="534ce-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="534ce-164">Namespace</span></span><br/>                | <span data-ttu-id="534ce-165">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="534ce-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="534ce-166">MOF</span><span class="sxs-lookup"><span data-stu-id="534ce-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="534ce-167"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="534ce-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="534ce-168">DLL</span><span class="sxs-lookup"><span data-stu-id="534ce-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="534ce-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="534ce-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

