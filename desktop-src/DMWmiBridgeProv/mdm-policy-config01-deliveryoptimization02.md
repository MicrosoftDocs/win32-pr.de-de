---
title: MDM_Policy_Config01_DeliveryOptimization02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ DeliveryOptimization02-Klasse stellt die verfügbaren Übermittlungs Optimierungs Richtlinien dar.
ms.assetid: 10dfb751-f044-4f30-90e0-af0fcb0931fb
keywords:
- MDM_Policy_Config01_DeliveryOptimization02-Klasse
- MDM_Policy_Config01_DeliveryOptimization02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeliveryOptimization02
- MDM_Policy_Config01_DeliveryOptimization02.InstanceID
- MDM_Policy_Config01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb9675f87a5bf9951e125bded69ae5eb10feb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103307"
---
# <a name="mdm_policy_config01_deliveryoptimization02-class"></a><span data-ttu-id="c263d-105">MDM- \_ Richtlinie \_ Config01 \_ DeliveryOptimization02-Klasse</span><span class="sxs-lookup"><span data-stu-id="c263d-105">MDM\_Policy\_Config01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="c263d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c263d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c263d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c263d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c263d-108">Die **MDM- \_ Richtlinie \_ Config01 \_ DeliveryOptimization02** -Klasse stellt die verfügbaren Übermittlungs Optimierungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="c263d-108">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="c263d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c263d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c263d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c263d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a><span data-ttu-id="c263d-111">Member</span><span class="sxs-lookup"><span data-stu-id="c263d-111">Members</span></span>

<span data-ttu-id="c263d-112">Die **MDM- \_ Richtlinie \_ Config01 \_ DeliveryOptimization02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c263d-112">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="c263d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c263d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c263d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c263d-114">Properties</span></span>

<span data-ttu-id="c263d-115">Die **MDM- \_ Richtlinie \_ Config01 \_ DeliveryOptimization02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c263d-115">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c263d-116">Doabsolutemaxcachesize</span><span class="sxs-lookup"><span data-stu-id="c263d-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-119">Doallowvpnpeercaching</span><span class="sxs-lookup"><span data-stu-id="c263d-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-122">Docachehost</span><span class="sxs-lookup"><span data-stu-id="c263d-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c263d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-125">Dodownloadmode</span><span class="sxs-lookup"><span data-stu-id="c263d-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-128">Dogroupid</span><span class="sxs-lookup"><span data-stu-id="c263d-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c263d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-131">Domaxcacheage</span><span class="sxs-lookup"><span data-stu-id="c263d-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-134">Domaxcachesize</span><span class="sxs-lookup"><span data-stu-id="c263d-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-137">Domaxdownloadbandwidth</span><span class="sxs-lookup"><span data-stu-id="c263d-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-140">Domaxuploadbandwidth</span><span class="sxs-lookup"><span data-stu-id="c263d-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-143">Dominbackgroundqos</span><span class="sxs-lookup"><span data-stu-id="c263d-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-146">Dominbatteryprozagezudepwedtoupload</span><span class="sxs-lookup"><span data-stu-id="c263d-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-149">Domindisksizezuweisung wedtopeer</span><span class="sxs-lookup"><span data-stu-id="c263d-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-152">Dominfilesizetocache</span><span class="sxs-lookup"><span data-stu-id="c263d-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-155">Dominramallowedtopeer</span><span class="sxs-lookup"><span data-stu-id="c263d-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-158">Domodifycachedrive</span><span class="sxs-lookup"><span data-stu-id="c263d-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c263d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-161">Domonthlyuploaddatacap</span><span class="sxs-lookup"><span data-stu-id="c263d-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c263d-164">Dopercentagemaxdownloadbandwidth</span><span class="sxs-lookup"><span data-stu-id="c263d-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c263d-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c263d-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c263d-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c263d-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c263d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c263d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c263d-170">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c263d-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c263d-171">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="c263d-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="c263d-172">Für diese Klasse ist die Zeichenfolge "deliveryoptimization".</span><span class="sxs-lookup"><span data-stu-id="c263d-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="c263d-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c263d-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c263d-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c263d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c263d-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c263d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c263d-176">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c263d-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c263d-177">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="c263d-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="c263d-178">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="c263d-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c263d-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c263d-179">Requirements</span></span>



| <span data-ttu-id="c263d-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c263d-180">Requirement</span></span> | <span data-ttu-id="c263d-181">Wert</span><span class="sxs-lookup"><span data-stu-id="c263d-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c263d-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c263d-182">Minimum supported client</span></span><br/> | <span data-ttu-id="c263d-183">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c263d-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c263d-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c263d-184">Minimum supported server</span></span><br/> | <span data-ttu-id="c263d-185">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c263d-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c263d-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="c263d-186">Namespace</span></span><br/>                | <span data-ttu-id="c263d-187">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c263d-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c263d-188">MOF</span><span class="sxs-lookup"><span data-stu-id="c263d-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c263d-189"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c263d-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c263d-190">DLL</span><span class="sxs-lookup"><span data-stu-id="c263d-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c263d-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c263d-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c263d-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c263d-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c263d-193">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="c263d-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

