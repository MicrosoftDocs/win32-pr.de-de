---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse
description: Die MDM \_ enterprismodernappmanagement \_ StoreLicenses02 \_ 01-Klasse wird verwendet, um Lizenzen für Store-Apps zu verwalten.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040831"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="dd7dc-105">MDM \_ enterprismodernappmanagement \_ StoreLicenses02 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd7dc-105">MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="dd7dc-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd7dc-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="dd7dc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd7dc-108">Die **MDM \_ enterprismodernappmanagement \_ StoreLicenses02 \_ 01** -Klasse wird verwendet, um Lizenzen für Store-Apps zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-108">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class is used to manage licenses for store apps.</span></span>

<span data-ttu-id="dd7dc-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd7dc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd7dc-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a><span data-ttu-id="dd7dc-111">Member</span><span class="sxs-lookup"><span data-stu-id="dd7dc-111">Members</span></span>

<span data-ttu-id="dd7dc-112">Die **MDM \_ enterpritarmodernappmanagement \_ StoreLicenses02 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd7dc-112">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="dd7dc-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd7dc-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd7dc-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd7dc-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd7dc-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd7dc-115">Methods</span></span>

<span data-ttu-id="dd7dc-116">Die **MDM \_ enterprismodernappmanagement \_ StoreLicenses02 \_ 01** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-116">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these methods.</span></span>



| <span data-ttu-id="dd7dc-117">Methode</span><span class="sxs-lookup"><span data-stu-id="dd7dc-117">Method</span></span>                                                                                                              | <span data-ttu-id="dd7dc-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd7dc-118">Description</span></span>                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="dd7dc-119">**Addlicenanmethod**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-119">**AddLicenseMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | <span data-ttu-id="dd7dc-120">Methode zum Hinzufügen einer Lizenz.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-120">Method for adding a license.</span></span><br/>                 |
| [<span data-ttu-id="dd7dc-121">**Getlicenabfromstoremethod**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-121">**GetLicenseFromStoreMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | <span data-ttu-id="dd7dc-122">Methode zum erhalten einer Lizenz aus dem Store.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-122">Method for getting a license from the store.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd7dc-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd7dc-123">Properties</span></span>

<span data-ttu-id="dd7dc-124">Die **MDM \_ enterprismodernappmanagement \_ StoreLicenses02 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-124">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd7dc-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd7dc-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd7dc-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd7dc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd7dc-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd7dc-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd7dc-129">Optionaler Knoten.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-129">Optional node.</span></span> <span data-ttu-id="dd7dc-130">Lizenz-ID für eine installierte Store-App.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-130">License ID for a store installed app.</span></span> <span data-ttu-id="dd7dc-131">Die Lizenz-ID ist im Allgemeinen der PFN der app.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-131">The license ID is generally the PFN of the app.</span></span>

<span data-ttu-id="dd7dc-132">Unterstützte Vorgänge sind Add, Get und DELETE.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-132">Supported operations are Add, Get, and Delete.</span></span>

</dd> <dt>

[<span data-ttu-id="dd7dc-133">Licensecategory</span><span class="sxs-lookup"><span data-stu-id="dd7dc-133">LicenseCategory</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd7dc-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd7dc-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd7dc-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd7dc-136">Licensusage</span><span class="sxs-lookup"><span data-stu-id="dd7dc-136">LicenseUsage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd7dc-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd7dc-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd7dc-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd7dc-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd7dc-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd7dc-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd7dc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd7dc-142">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd7dc-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd7dc-143">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="dd7dc-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="dd7dc-144">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses".</span><span class="sxs-lookup"><span data-stu-id="dd7dc-144">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span></span>

</dd> <dt>

[<span data-ttu-id="dd7dc-145">RequesterID</span><span class="sxs-lookup"><span data-stu-id="dd7dc-145">RequesterID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd7dc-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd7dc-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd7dc-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd7dc-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd7dc-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd7dc-148">Requirements</span></span>



| <span data-ttu-id="dd7dc-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd7dc-149">Requirement</span></span> | <span data-ttu-id="dd7dc-150">Wert</span><span class="sxs-lookup"><span data-stu-id="dd7dc-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7dc-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd7dc-151">Minimum supported client</span></span><br/> | <span data-ttu-id="dd7dc-152">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd7dc-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd7dc-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd7dc-153">Minimum supported server</span></span><br/> | <span data-ttu-id="dd7dc-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd7dc-154">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd7dc-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd7dc-155">Namespace</span></span><br/>                | <span data-ttu-id="dd7dc-156">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dd7dc-156">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dd7dc-157">MOF</span><span class="sxs-lookup"><span data-stu-id="dd7dc-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd7dc-158"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd7dc-158"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd7dc-159">DLL</span><span class="sxs-lookup"><span data-stu-id="dd7dc-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd7dc-160"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd7dc-160"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd7dc-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd7dc-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd7dc-162">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="dd7dc-162">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

