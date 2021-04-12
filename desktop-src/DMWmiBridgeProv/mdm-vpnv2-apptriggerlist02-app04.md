---
title: MDM_VPNv2_AppTriggerList02_App04-Klasse
description: Die MDM \_ VPNv2AppTriggerList02 \_ App04-Klasse beschreibt eine Liste von Anwendungen, die für das auslöst des VPN festgelegt sind.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- MDM_VPNv2_AppTriggerList02_App04-Klasse
- MDM_VPNv2_AppTriggerList02_App04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62685ea94b99e843625e87e7c653a2ff19ab737d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104168"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a><span data-ttu-id="6c029-105">MDM \_ VPNv2 \_ AppTriggerList02 \_ App04-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c029-105">MDM\_VPNv2\_AppTriggerList02\_App04 class</span></span>

<span data-ttu-id="6c029-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6c029-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6c029-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6c029-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6c029-108">Die **MDM \_ VPNv2AppTriggerList02 \_ App04** -Klasse beschreibt eine Liste von Anwendungen, die für das auslöst des VPN festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6c029-108">The **MDM\_VPNv2AppTriggerList02\_App04** class describes a list of applications set to trigger the VPN.</span></span>

<span data-ttu-id="6c029-109">Wenn eine dieser apps gestartet wird und das VPN-Profil derzeit das aktive Profil ist, wird dieses VPN-Profil ausgelöst, um eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6c029-109">If any of these apps are launched and the VPN profile is currently the active profile, this VPN profile will be triggered to connect.</span></span>

<span data-ttu-id="6c029-110">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c029-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c029-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c029-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="6c029-112">Member</span><span class="sxs-lookup"><span data-stu-id="6c029-112">Members</span></span>

<span data-ttu-id="6c029-113">Die **MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c029-113">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="6c029-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c029-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c029-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c029-115">Properties</span></span>

<span data-ttu-id="6c029-116">Die **MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c029-116">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6c029-117">Id</span><span class="sxs-lookup"><span data-stu-id="6c029-117">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c029-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c029-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c029-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6c029-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6c029-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6c029-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c029-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c029-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c029-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c029-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c029-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6c029-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6c029-124">App-Knoten unter der Zeilen-ID.</span><span class="sxs-lookup"><span data-stu-id="6c029-124">App Node under the Row Id.</span></span>

</dd> <dt>

<span data-ttu-id="6c029-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6c029-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c029-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c029-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c029-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c029-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c029-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6c029-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6c029-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="6c029-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="6c029-130">Für diese Klasse lautet die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/AppTriggerList/*apptriggerrowid*".</span><span class="sxs-lookup"><span data-stu-id="6c029-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span></span>

</dd> <dt>

[<span data-ttu-id="6c029-131">Type</span><span class="sxs-lookup"><span data-stu-id="6c029-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c029-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c029-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c029-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6c029-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c029-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c029-134">Requirements</span></span>



| <span data-ttu-id="6c029-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c029-135">Requirement</span></span> | <span data-ttu-id="6c029-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6c029-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c029-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c029-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6c029-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c029-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c029-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c029-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6c029-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6c029-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6c029-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c029-141">Namespace</span></span><br/>                | <span data-ttu-id="6c029-142">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6c029-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6c029-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6c029-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c029-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6c029-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c029-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6c029-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c029-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c029-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c029-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c029-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c029-148">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="6c029-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

