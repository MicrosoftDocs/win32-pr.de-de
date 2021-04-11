---
title: MDM_VPNv2_TrafficFilterList02_01-Klasse
description: Die MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01-Klasse enthält eine optionale Liste von Regeln. Nur Datenverkehr, der diesen Regeln entspricht, kann über die VPN-Schnittstelle gesendet werden.
ms.assetid: 3cffe96d-7454-43a1-aa5b-33e820369e7e
keywords:
- MDM_VPNv2_TrafficFilterList02_01-Klasse
- MDM_VPNv2_TrafficFilterList02_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01.InstanceID
- MDM_VPNv2_TrafficFilterList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3005026a85aa118a4122e073579fcb06389a9fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104955"
---
# <a name="mdm_vpnv2_trafficfilterlist02_01-class"></a><span data-ttu-id="e96c7-106">MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="e96c7-106">MDM\_VPNv2\_TrafficFilterList02\_01 class</span></span>

<span data-ttu-id="e96c7-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e96c7-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e96c7-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e96c7-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e96c7-109">Die **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** -Klasse enthält eine optionale Liste von Regeln.</span><span class="sxs-lookup"><span data-stu-id="e96c7-109">The **MDM\_VPNv2\_TrafficFilterList02\_01** class contains an optional list of rules.</span></span> <span data-ttu-id="e96c7-110">Nur Datenverkehr, der diesen Regeln entspricht, kann über die VPN-Schnittstelle gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e96c7-110">Only traffic that matches these rules can be sent via the VPN Interface.</span></span>

<span data-ttu-id="e96c7-111">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e96c7-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e96c7-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="e96c7-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_01
{
  string InstanceID;
  string ParentID;
  string Claims;
  sint32 Protocol;
  string LocalPortRanges;
  string RemotePortRanges;
  string LocalAddressRanges;
  string RemoteAddressRanges;
  string RoutingPolicyType;
};
```

## <a name="members"></a><span data-ttu-id="e96c7-113">Member</span><span class="sxs-lookup"><span data-stu-id="e96c7-113">Members</span></span>

<span data-ttu-id="e96c7-114">Die **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e96c7-114">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e96c7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e96c7-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e96c7-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e96c7-116">Properties</span></span>

<span data-ttu-id="e96c7-117">Die **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e96c7-117">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e96c7-118">Ansprüche</span><span class="sxs-lookup"><span data-stu-id="e96c7-118">Claims</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-claims)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e96c7-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e96c7-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e96c7-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e96c7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e96c7-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e96c7-125">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="e96c7-125">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="e96c7-126">Localaddressranges</span><span class="sxs-lookup"><span data-stu-id="e96c7-126">LocalAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e96c7-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e96c7-129">Localportranges</span><span class="sxs-lookup"><span data-stu-id="e96c7-129">LocalPortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e96c7-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e96c7-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e96c7-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e96c7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e96c7-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e96c7-136">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="e96c7-136">Describes the full path to the parent node.</span></span> <span data-ttu-id="e96c7-137">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/TrafficFilterList".</span><span class="sxs-lookup"><span data-stu-id="e96c7-137">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span></span>

</dd> <dt>

[<span data-ttu-id="e96c7-138">Protokoll</span><span class="sxs-lookup"><span data-stu-id="e96c7-138">Protocol</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-139">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e96c7-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e96c7-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e96c7-141">Remoteaddressranges</span><span class="sxs-lookup"><span data-stu-id="e96c7-141">RemoteAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e96c7-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e96c7-144">Remoteportranges</span><span class="sxs-lookup"><span data-stu-id="e96c7-144">RemotePortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e96c7-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e96c7-147">Routingpolicytype</span><span class="sxs-lookup"><span data-stu-id="e96c7-147">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e96c7-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e96c7-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e96c7-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e96c7-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e96c7-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e96c7-150">Requirements</span></span>



| <span data-ttu-id="e96c7-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e96c7-151">Requirement</span></span> | <span data-ttu-id="e96c7-152">Wert</span><span class="sxs-lookup"><span data-stu-id="e96c7-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e96c7-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e96c7-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e96c7-154">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e96c7-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e96c7-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e96c7-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e96c7-156">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e96c7-156">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e96c7-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="e96c7-157">Namespace</span></span><br/>                | <span data-ttu-id="e96c7-158">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e96c7-158">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e96c7-159">MOF</span><span class="sxs-lookup"><span data-stu-id="e96c7-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e96c7-160"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e96c7-160"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e96c7-161">DLL</span><span class="sxs-lookup"><span data-stu-id="e96c7-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e96c7-162"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e96c7-162"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e96c7-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e96c7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e96c7-164">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="e96c7-164">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

