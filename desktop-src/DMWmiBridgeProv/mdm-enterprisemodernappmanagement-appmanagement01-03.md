---
title: MDM_EnterpriseModernAppManagement_AppManagement01_03-Klasse
description: Die MDM \_ enterprismodernappmanagement \_ AppManagement01 \_ 03-Klasse stellt spezifische Informationen über die APP bereit, wie z. b. Name, Version und Verleger.
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01_03-Klasse
- MDM_EnterpriseModernAppManagement_AppManagement01_03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24c028c6a1f0d551fc54cb078376dcdef968abc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104985"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a><span data-ttu-id="c3cb1-105">MDM \_ enterprismodernappmanagement \_ AppManagement01 \_ 03-Klasse</span><span class="sxs-lookup"><span data-stu-id="c3cb1-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_03 class</span></span>

<span data-ttu-id="c3cb1-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c3cb1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c3cb1-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c3cb1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c3cb1-108">Die **MDM \_ enterprismodernappmanagement \_ AppManagement01 \_ 03** -Klasse stellt spezifische Informationen über die APP bereit, wie z. b. Name, Version und Verleger.</span><span class="sxs-lookup"><span data-stu-id="c3cb1-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class provides specific information about the app, such as name, version, and publisher.</span></span>

<span data-ttu-id="c3cb1-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c3cb1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cb1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3cb1-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a><span data-ttu-id="c3cb1-111">Member</span><span class="sxs-lookup"><span data-stu-id="c3cb1-111">Members</span></span>

<span data-ttu-id="c3cb1-112">Die **MDM \_ enterpritarmodernappmanagement \_ AppManagement01 \_ 03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c3cb1-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these types of members:</span></span>

-   [<span data-ttu-id="c3cb1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3cb1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3cb1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3cb1-114">Properties</span></span>

<span data-ttu-id="c3cb1-115">Die **MDM \_ enterprismodernappmanagement \_ AppManagement01 \_ 03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3cb1-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c3cb1-116">Architektur</span><span class="sxs-lookup"><span data-stu-id="c3cb1-116">Architecture</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-119">InstallDate</span><span class="sxs-lookup"><span data-stu-id="c3cb1-119">InstallDate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-122">INSTALLLOCATION</span><span class="sxs-lookup"><span data-stu-id="c3cb1-122">InstallLocation</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3cb1-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3cb1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3cb1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3cb1-129">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="c3cb1-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="c3cb1-130">Bei dieser Klasse ist die Zeichenfolge die Instanz des vollständigen Paket namens.</span><span class="sxs-lookup"><span data-stu-id="c3cb1-130">For this class, the string is the instance of the package full name.</span></span>

</dd> <dt>

[<span data-ttu-id="c3cb1-131">Isbundle</span><span class="sxs-lookup"><span data-stu-id="c3cb1-131">IsBundle</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-134">Isframework</span><span class="sxs-lookup"><span data-stu-id="c3cb1-134">IsFramework</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-137">Isprovisioning</span><span class="sxs-lookup"><span data-stu-id="c3cb1-137">IsProvisioned</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-140">Name</span><span class="sxs-lookup"><span data-stu-id="c3cb1-140">Name</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-143">Packagestatus</span><span class="sxs-lookup"><span data-stu-id="c3cb1-143">PackageStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3cb1-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3cb1-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-149">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3cb1-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3cb1-150">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="c3cb1-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="c3cb1-151">Für diese Klasse lautet die Zeichenfolge "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*enterpriseid* / *packagefamilyname*".</span><span class="sxs-lookup"><span data-stu-id="c3cb1-151">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="c3cb1-152">Publisher</span><span class="sxs-lookup"><span data-stu-id="c3cb1-152">Publisher</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-155">Requirements-Installation</span><span class="sxs-lookup"><span data-stu-id="c3cb1-155">RequiresReinstall</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-158">ResourceID</span><span class="sxs-lookup"><span data-stu-id="c3cb1-158">ResourceID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-161">Benutzer</span><span class="sxs-lookup"><span data-stu-id="c3cb1-161">Users</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c3cb1-164">Version</span><span class="sxs-lookup"><span data-stu-id="c3cb1-164">Version</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cb1-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3cb1-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3cb1-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3cb1-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3cb1-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3cb1-167">Requirements</span></span>



| <span data-ttu-id="c3cb1-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3cb1-168">Requirement</span></span> | <span data-ttu-id="c3cb1-169">Wert</span><span class="sxs-lookup"><span data-stu-id="c3cb1-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cb1-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3cb1-170">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cb1-171">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3cb1-171">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3cb1-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3cb1-172">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cb1-173">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c3cb1-173">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c3cb1-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3cb1-174">Namespace</span></span><br/>                | <span data-ttu-id="c3cb1-175">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c3cb1-175">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c3cb1-176">MOF</span><span class="sxs-lookup"><span data-stu-id="c3cb1-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3cb1-177"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c3cb1-177"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3cb1-178">DLL</span><span class="sxs-lookup"><span data-stu-id="c3cb1-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3cb1-179"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3cb1-179"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3cb1-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3cb1-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cb1-181">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="c3cb1-181">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

