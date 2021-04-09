---
title: MDM_Policy_Config01_Connectivity02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Connectivity02-Klasse stellt die verfügbaren Verbindungs Richtlinien dar.
ms.assetid: 670e48c2-1af1-45e9-81c6-cdf3a310240f
keywords:
- MDM_Policy_Config01_Connectivity02-Klasse
- MDM_Policy_Config01_Connectivity02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Connectivity02
- MDM_Policy_Config01_Connectivity02.InstanceID
- MDM_Policy_Config01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b39b897998bf47c5f5411456ccae7fcb6927aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740968"
---
# <a name="mdm_policy_config01_connectivity02-class"></a><span data-ttu-id="f4873-105">MDM- \_ Richtlinie \_ Config01 \_ Connectivity02-Klasse</span><span class="sxs-lookup"><span data-stu-id="f4873-105">MDM\_Policy\_Config01\_Connectivity02 class</span></span>

<span data-ttu-id="f4873-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f4873-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f4873-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="f4873-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f4873-108">Die **MDM- \_ Richtlinie \_ Config01 \_ Connectivity02** -Klasse stellt die verfügbaren Verbindungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="f4873-108">The **MDM\_Policy\_Config01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="f4873-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f4873-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4873-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4873-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a><span data-ttu-id="f4873-111">Member</span><span class="sxs-lookup"><span data-stu-id="f4873-111">Members</span></span>

<span data-ttu-id="f4873-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Connectivity02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f4873-112">The **MDM\_Policy\_Config01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="f4873-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4873-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4873-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4873-114">Properties</span></span>

<span data-ttu-id="f4873-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Connectivity02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f4873-115">The **MDM\_Policy\_Config01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f4873-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="f4873-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4873-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-119">Allowcellulardata</span><span class="sxs-lookup"><span data-stu-id="f4873-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4873-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-122">Allowcellulardataroaming</span><span class="sxs-lookup"><span data-stu-id="f4873-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4873-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-125">Allowconnecteddevices</span><span class="sxs-lookup"><span data-stu-id="f4873-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4873-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="f4873-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4873-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-131">Allowvpnroamingovercellular</span><span class="sxs-lookup"><span data-stu-id="f4873-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4873-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-134">Diableprintingoverhttp</span><span class="sxs-lookup"><span data-stu-id="f4873-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4873-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-137">Disabledownloadingof printdriversoverhttp</span><span class="sxs-lookup"><span data-stu-id="f4873-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4873-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-140">Disableinternetdownloadforwebpublishingandonlineorderingassistenten</span><span class="sxs-lookup"><span data-stu-id="f4873-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4873-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-143">Disallownetworkconnectivityactivetests</span><span class="sxs-lookup"><span data-stu-id="f4873-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f4873-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f4873-146">"Hardeneduncpath"</span><span class="sxs-lookup"><span data-stu-id="f4873-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4873-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f4873-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f4873-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4873-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4873-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4873-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f4873-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f4873-153">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="f4873-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="f4873-154">Für diese Klasse ist die Zeichenfolge "Connectivity".</span><span class="sxs-lookup"><span data-stu-id="f4873-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="f4873-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f4873-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4873-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4873-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4873-158">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f4873-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f4873-159">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="f4873-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="f4873-160">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="f4873-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="f4873-161">Prohibitinstallationandconfigurationofnetworkbridge</span><span class="sxs-lookup"><span data-stu-id="f4873-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4873-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4873-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4873-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4873-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4873-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4873-164">Requirements</span></span>



| <span data-ttu-id="f4873-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4873-165">Requirement</span></span> | <span data-ttu-id="f4873-166">Wert</span><span class="sxs-lookup"><span data-stu-id="f4873-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4873-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4873-167">Minimum supported client</span></span><br/> | <span data-ttu-id="f4873-168">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4873-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4873-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4873-169">Minimum supported server</span></span><br/> | <span data-ttu-id="f4873-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f4873-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f4873-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4873-171">Namespace</span></span><br/>                | <span data-ttu-id="f4873-172">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="f4873-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="f4873-173">MOF</span><span class="sxs-lookup"><span data-stu-id="f4873-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4873-174"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f4873-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4873-175">DLL</span><span class="sxs-lookup"><span data-stu-id="f4873-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4873-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4873-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4873-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4873-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4873-178">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="f4873-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

