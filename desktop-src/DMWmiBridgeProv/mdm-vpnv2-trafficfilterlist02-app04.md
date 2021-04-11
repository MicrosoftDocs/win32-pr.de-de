---
title: MDM_VPNv2_TrafficFilterList02_App04-Klasse
description: Die MDM \_ TrafficFilterList02 \_ App04-Klasse ermöglicht die Konfiguration der apps, die über die VPN-Schnittstelle zulässig sind.
ms.assetid: a56d004b-8fe3-4187-8aad-962f1cab8f7f
keywords:
- MDM_VPNv2_TrafficFilterList02_App04-Klasse
- MDM_VPNv2_TrafficFilterList02_App04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04.InstanceID
- MDM_VPNv2_TrafficFilterList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1cd3edbfec5fa270f8404983af57dba4fad31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104954"
---
# <a name="mdm_vpnv2_trafficfilterlist02_app04-class"></a><span data-ttu-id="d318d-105">MDM \_ VPNv2 \_ TrafficFilterList02 \_ App04-Klasse</span><span class="sxs-lookup"><span data-stu-id="d318d-105">MDM\_VPNv2\_TrafficFilterList02\_App04 class</span></span>

<span data-ttu-id="d318d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d318d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d318d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d318d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d318d-108">Die **MDM \_ TrafficFilterList02 \_ App04** -Klasse ermöglicht die Konfiguration der apps, die über die VPN-Schnittstelle zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d318d-108">The **MDM\_TrafficFilterList02\_App04** class provides configuration of the apps that are allowed over the VPN interface.</span></span>

<span data-ttu-id="d318d-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d318d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d318d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d318d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="d318d-111">Member</span><span class="sxs-lookup"><span data-stu-id="d318d-111">Members</span></span>

<span data-ttu-id="d318d-112">Die **MDM \_ VPNv2 \_ TrafficFilterList02 \_ App04** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d318d-112">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="d318d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d318d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d318d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d318d-114">Properties</span></span>

<span data-ttu-id="d318d-115">Die **MDM \_ VPNv2 \_ TrafficFilterList02 \_ App04** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d318d-115">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d318d-116">Id</span><span class="sxs-lookup"><span data-stu-id="d318d-116">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d318d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d318d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d318d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d318d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d318d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d318d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d318d-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d318d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d318d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d318d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d318d-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d318d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d318d-123">Pro-App-VPN-Regel.</span><span class="sxs-lookup"><span data-stu-id="d318d-123">Per app VPN rule.</span></span> <span data-ttu-id="d318d-124">Auf diese Weise können nur die angegebenen Apps über die VPN-Schnittstelle zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="d318d-124">This will allow only the apps specified to be allowed over the VPN interface.</span></span> <span data-ttu-id="d318d-125">Für diese Klasse ist die Zeichenfolge "App".</span><span class="sxs-lookup"><span data-stu-id="d318d-125">For this class, the string is "App"</span></span>

</dd> <dt>

<span data-ttu-id="d318d-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d318d-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d318d-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d318d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d318d-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d318d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d318d-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d318d-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d318d-130">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="d318d-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="d318d-131">Für diese Klasse lautet die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/TrafficFilterList/*trafficfilterlistid*"</span><span class="sxs-lookup"><span data-stu-id="d318d-131">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span></span>

</dd> <dt>

[<span data-ttu-id="d318d-132">Type</span><span class="sxs-lookup"><span data-stu-id="d318d-132">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d318d-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d318d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d318d-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d318d-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d318d-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d318d-135">Requirements</span></span>



| <span data-ttu-id="d318d-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d318d-136">Requirement</span></span> | <span data-ttu-id="d318d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d318d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d318d-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d318d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d318d-139">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d318d-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d318d-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d318d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d318d-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d318d-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d318d-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="d318d-142">Namespace</span></span><br/>                | <span data-ttu-id="d318d-143">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d318d-143">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d318d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d318d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d318d-145"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d318d-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d318d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d318d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d318d-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d318d-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d318d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d318d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d318d-149">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="d318d-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

