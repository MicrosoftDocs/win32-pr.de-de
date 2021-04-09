---
title: MDM_Policy_Result01_Connectivity02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Connectivity02-Klasse stellt die verfügbaren Verbindungs Richtlinien dar.
ms.assetid: af5f21f8-8010-4e5a-b75f-30032333d87d
keywords:
- MDM_Policy_Result01_Connectivity02-Klasse
- MDM_Policy_Result01_Connectivity02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Connectivity02
- MDM_Policy_Result01_Connectivity02.InstanceID
- MDM_Policy_Result01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723e8fa3287f99994d45fcc0a8bc5a09473a7563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858728"
---
# <a name="mdm_policy_result01_connectivity02-class"></a><span data-ttu-id="2e1e1-105">MDM- \_ Richtlinie \_ Result01 \_ Connectivity02-Klasse</span><span class="sxs-lookup"><span data-stu-id="2e1e1-105">MDM\_Policy\_Result01\_Connectivity02 class</span></span>

<span data-ttu-id="2e1e1-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2e1e1-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2e1e1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2e1e1-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Connectivity02** -Klasse stellt die verfügbaren Verbindungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-108">The **MDM\_Policy\_Result01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="2e1e1-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1e1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e1e1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Connectivity02
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

## <a name="members"></a><span data-ttu-id="2e1e1-111">Member</span><span class="sxs-lookup"><span data-stu-id="2e1e1-111">Members</span></span>

<span data-ttu-id="2e1e1-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Connectivity02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2e1e1-112">The **MDM\_Policy\_Result01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="2e1e1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e1e1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e1e1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e1e1-114">Properties</span></span>

<span data-ttu-id="2e1e1-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Connectivity02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-115">The **MDM\_Policy\_Result01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2e1e1-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="2e1e1-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-119">Allowcellulardata</span><span class="sxs-lookup"><span data-stu-id="2e1e1-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-122">Allowcellulardataroaming</span><span class="sxs-lookup"><span data-stu-id="2e1e1-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-125">Allowconnecteddevices</span><span class="sxs-lookup"><span data-stu-id="2e1e1-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="2e1e1-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-131">Allowvpnroamingovercellular</span><span class="sxs-lookup"><span data-stu-id="2e1e1-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-134">Diableprintingoverhttp</span><span class="sxs-lookup"><span data-stu-id="2e1e1-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-137">Disabledownloadingof printdriversoverhttp</span><span class="sxs-lookup"><span data-stu-id="2e1e1-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-140">Disableinternetdownloadforwebpublishingandonlineorderingassistenten</span><span class="sxs-lookup"><span data-stu-id="2e1e1-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-143">Disallownetworkconnectivityactivetests</span><span class="sxs-lookup"><span data-stu-id="2e1e1-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e1e1-146">"Hardeneduncpath"</span><span class="sxs-lookup"><span data-stu-id="2e1e1-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e1e1-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e1e1-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e1e1-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e1e1-153">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="2e1e1-154">Für diese Klasse ist die Zeichenfolge "Connectivity".</span><span class="sxs-lookup"><span data-stu-id="2e1e1-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="2e1e1-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e1e1-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-158">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e1e1-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e1e1-159">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2e1e1-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="2e1e1-160">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="2e1e1-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="2e1e1-161">Prohibitinstallationandconfigurationofnetworkbridge</span><span class="sxs-lookup"><span data-stu-id="2e1e1-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e1e1-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e1e1-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e1e1-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e1e1-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e1e1-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e1e1-164">Requirements</span></span>



| <span data-ttu-id="2e1e1-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e1e1-165">Requirement</span></span> | <span data-ttu-id="2e1e1-166">Wert</span><span class="sxs-lookup"><span data-stu-id="2e1e1-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e1e1-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e1e1-167">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1e1-168">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e1e1-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e1e1-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e1e1-169">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1e1-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2e1e1-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2e1e1-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e1e1-171">Namespace</span></span><br/>                | <span data-ttu-id="2e1e1-172">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2e1e1-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="2e1e1-173">MOF</span><span class="sxs-lookup"><span data-stu-id="2e1e1-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e1e1-174"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e1e1-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e1e1-175">DLL</span><span class="sxs-lookup"><span data-stu-id="2e1e1-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e1e1-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e1e1-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e1e1-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e1e1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1e1-178">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2e1e1-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

