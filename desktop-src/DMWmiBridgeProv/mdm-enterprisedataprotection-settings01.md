---
title: MDM_EnterpriseDataProtection_Settings01-Klasse
description: Die MDM \_ enterprisedataprotection \_ Settings01-Klasse wird zum Konfigurieren von Windows Information Protection (WIP)-spezifischen Einstellungen (früher als Unternehmens Datenschutz bezeichnet) verwendet.
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- MDM_EnterpriseDataProtection_Settings01-Klasse
- MDM_EnterpriseDataProtection_Settings01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478066"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a><span data-ttu-id="a78e6-105">MDM \_ enterprisdataprotection \_ Settings01-Klasse</span><span class="sxs-lookup"><span data-stu-id="a78e6-105">MDM\_EnterpriseDataProtection\_Settings01 class</span></span>

<span data-ttu-id="a78e6-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a78e6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a78e6-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="a78e6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a78e6-108">Die **MDM \_ enterprisedataprotection \_ Settings01** -Klasse wird zum Konfigurieren von Windows Information Protection (WIP)-spezifischen Einstellungen (früher als Unternehmens Datenschutz bezeichnet) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a78e6-108">The **MDM\_EnterpriseDataProtection\_Settings01** class is used to configure Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span> <span data-ttu-id="a78e6-109">Weitere Informationen zu WIP finden Sie unter [Schützen von Unternehmensdaten mithilfe von Enterprise Data Protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="a78e6-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="a78e6-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a78e6-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a78e6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a78e6-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a><span data-ttu-id="a78e6-112">Member</span><span class="sxs-lookup"><span data-stu-id="a78e6-112">Members</span></span>

<span data-ttu-id="a78e6-113">Die **MDM \_ enterpritardataprotection \_ Settings01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a78e6-113">The **MDM\_EnterpriseDataProtection\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="a78e6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a78e6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a78e6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a78e6-115">Properties</span></span>

<span data-ttu-id="a78e6-116">Die **MDM \_ enterprigendataprotection \_ Settings01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a78e6-116">The **MDM\_EnterpriseDataProtection\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a78e6-117">Zuordnung von "zuzurermsforedp"</span><span class="sxs-lookup"><span data-stu-id="a78e6-117">AllowAzureRMSForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a78e6-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a78e6-120">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="a78e6-120">AllowUserDecryption</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a78e6-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a78e6-123">Datarecoverycertificate</span><span class="sxs-lookup"><span data-stu-id="a78e6-123">DataRecoveryCertificate</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a78e6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-126">**Qualifizierer: octetstring**</span><span class="sxs-lookup"><span data-stu-id="a78e6-126">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a78e6-127">EDPEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="a78e6-127">EDPEnforcementLevel</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-128">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a78e6-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a78e6-130">Edpshowicons</span><span class="sxs-lookup"><span data-stu-id="a78e6-130">EDPShowIcons</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a78e6-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a78e6-133">EnterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="a78e6-133">EnterpriseProtectedDomainNames</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a78e6-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a78e6-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a78e6-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a78e6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a78e6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-139">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a78e6-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a78e6-140">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="a78e6-140">Identifies the name of the parent node.</span></span> <span data-ttu-id="a78e6-141">Für diese Klasse ist die Zeichenfolge "Settings".</span><span class="sxs-lookup"><span data-stu-id="a78e6-141">For this class, the string is "Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a78e6-142">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a78e6-142">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a78e6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a78e6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-145">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a78e6-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a78e6-146">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="a78e6-146">Describes the full path to the parent node.</span></span> <span data-ttu-id="a78e6-147">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="a78e6-147">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="a78e6-148">Revokeondereroll</span><span class="sxs-lookup"><span data-stu-id="a78e6-148">RevokeOnUnenroll</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-149">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a78e6-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a78e6-151">Rmstemplateidforedp</span><span class="sxs-lookup"><span data-stu-id="a78e6-151">RMSTemplateIDForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a78e6-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a78e6-154">Smbauyverschlüsseltedfileextensions</span><span class="sxs-lookup"><span data-stu-id="a78e6-154">SMBAutoEncryptedFileExtensions</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a78e6-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a78e6-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a78e6-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a78e6-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a78e6-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a78e6-157">Requirements</span></span>



| <span data-ttu-id="a78e6-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a78e6-158">Requirement</span></span> | <span data-ttu-id="a78e6-159">Wert</span><span class="sxs-lookup"><span data-stu-id="a78e6-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a78e6-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a78e6-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a78e6-161">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a78e6-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a78e6-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a78e6-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a78e6-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a78e6-163">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a78e6-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="a78e6-164">Namespace</span></span><br/>                | <span data-ttu-id="a78e6-165">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a78e6-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a78e6-166">MOF</span><span class="sxs-lookup"><span data-stu-id="a78e6-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a78e6-167"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a78e6-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="a78e6-168">DLL</span><span class="sxs-lookup"><span data-stu-id="a78e6-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a78e6-169"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="a78e6-169"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

