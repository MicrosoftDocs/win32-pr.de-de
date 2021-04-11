---
title: MDM_Policy_Result01_Security02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Security02-Klasse stellt die verfügbaren Sicherheitsrichtlinien dar.
ms.assetid: e4f9bbeb-b542-454d-930b-0b4ac88fe189
keywords:
- MDM_Policy_Result01_Security02-Klasse
- MDM_Policy_Result01_Security02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Security02
- MDM_Policy_Result01_Security02.InstanceID
- MDM_Policy_Result01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 959d5cbc9382b4bef0899f5b44d8ee2d171bd704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040408"
---
# <a name="mdm_policy_result01_security02-class"></a><span data-ttu-id="5663f-105">MDM- \_ Richtlinie \_ Result01 \_ Security02-Klasse</span><span class="sxs-lookup"><span data-stu-id="5663f-105">MDM\_Policy\_Result01\_Security02 class</span></span>

<span data-ttu-id="5663f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="5663f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5663f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="5663f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5663f-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Security02** -Klasse stellt die verfügbaren Sicherheitsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="5663f-108">The **MDM\_Policy\_Result01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="5663f-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="5663f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5663f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5663f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a><span data-ttu-id="5663f-111">Member</span><span class="sxs-lookup"><span data-stu-id="5663f-111">Members</span></span>

<span data-ttu-id="5663f-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Security02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5663f-112">The **MDM\_Policy\_Result01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="5663f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5663f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5663f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5663f-114">Properties</span></span>

<span data-ttu-id="5663f-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Security02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5663f-115">The **MDM\_Policy\_Result01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5663f-116">Allowaddprovisioningpackage</span><span class="sxs-lookup"><span data-stu-id="5663f-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5663f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5663f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5663f-119">Allowremoveprovisioningpackage</span><span class="sxs-lookup"><span data-stu-id="5663f-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5663f-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5663f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5663f-122">Cleartpmibernotready</span><span class="sxs-lookup"><span data-stu-id="5663f-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5663f-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5663f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5663f-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5663f-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5663f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5663f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5663f-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5663f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5663f-129">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="5663f-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="5663f-130">Für diese Klasse ist die Zeichenfolge "Security".</span><span class="sxs-lookup"><span data-stu-id="5663f-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="5663f-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5663f-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5663f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5663f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5663f-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5663f-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5663f-135">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="5663f-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="5663f-136">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="5663f-136">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="5663f-137">Preventautomaticdeviceverschlüsseltionforazuread joineddevices</span><span class="sxs-lookup"><span data-stu-id="5663f-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5663f-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5663f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5663f-140">Requirements deviceencryption</span><span class="sxs-lookup"><span data-stu-id="5663f-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5663f-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5663f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5663f-143">Requirements provisioningpackagesignature</span><span class="sxs-lookup"><span data-stu-id="5663f-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5663f-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5663f-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5663f-146">Requuneregsevehealthcertificateonboot</span><span class="sxs-lookup"><span data-stu-id="5663f-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5663f-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5663f-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5663f-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5663f-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5663f-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5663f-149">Requirements</span></span>



| <span data-ttu-id="5663f-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5663f-150">Requirement</span></span> | <span data-ttu-id="5663f-151">Wert</span><span class="sxs-lookup"><span data-stu-id="5663f-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5663f-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5663f-152">Minimum supported client</span></span><br/> | <span data-ttu-id="5663f-153">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5663f-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5663f-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5663f-154">Minimum supported server</span></span><br/> | <span data-ttu-id="5663f-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5663f-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5663f-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="5663f-156">Namespace</span></span><br/>                | <span data-ttu-id="5663f-157">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="5663f-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5663f-158">MOF</span><span class="sxs-lookup"><span data-stu-id="5663f-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5663f-159"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5663f-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5663f-160">DLL</span><span class="sxs-lookup"><span data-stu-id="5663f-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5663f-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5663f-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5663f-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5663f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5663f-163">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="5663f-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

