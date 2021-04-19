---
title: MDM_VPNv2_DeviceCompliance02-Klasse
description: Reserviert für zukünftige Verwendung. | MDM_VPNv2_DeviceCompliance02-Klasse
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- MDM_VPNv2_DeviceCompliance02-Klasse
- MDM_VPNv2_DeviceCompliance02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373472"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a><span data-ttu-id="dc7aa-106">MDM \_ VPNv2 \_ DeviceCompliance02-Klasse</span><span class="sxs-lookup"><span data-stu-id="dc7aa-106">MDM\_VPNv2\_DeviceCompliance02 class</span></span>

<span data-ttu-id="dc7aa-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dc7aa-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="dc7aa-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dc7aa-109">Für zukünftige Verwendung reserviert</span><span class="sxs-lookup"><span data-stu-id="dc7aa-109">Reserved for Future Use</span></span>

<span data-ttu-id="dc7aa-110">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7aa-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc7aa-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a><span data-ttu-id="dc7aa-112">Member</span><span class="sxs-lookup"><span data-stu-id="dc7aa-112">Members</span></span>

<span data-ttu-id="dc7aa-113">Die **MDM \_ VPNv2 \_ DeviceCompliance02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc7aa-113">The **MDM\_VPNv2\_DeviceCompliance02** class has these types of members:</span></span>

-   [<span data-ttu-id="dc7aa-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc7aa-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc7aa-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc7aa-115">Properties</span></span>

<span data-ttu-id="dc7aa-116">Die **MDM \_ VPNv2 \_ DeviceCompliance02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-116">The **MDM\_VPNv2\_DeviceCompliance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dc7aa-117">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="dc7aa-117">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc7aa-118">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dc7aa-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc7aa-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc7aa-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc7aa-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc7aa-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc7aa-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc7aa-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc7aa-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc7aa-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc7aa-124">Hinzugefügt in Windows 10, Version 1607.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-124">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="dc7aa-125">Knoten unter devicecompliance können verwendet werden, um den Aad-basierten bedingten Zugriff für VPN zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-125">Nodes under DeviceCompliance can be used to enable AAD-based Conditional Access for VPN.</span></span>

</dd> <dt>

<span data-ttu-id="dc7aa-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc7aa-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc7aa-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc7aa-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc7aa-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc7aa-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc7aa-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc7aa-130">Hinzugefügt in Windows 10, Version 1607.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-130">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="dc7aa-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="dc7aa-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="dc7aa-132">Für diese Klasse ist die Zeichen *Folge "./Vendor/MSFT/VPNv2/profile* Name".</span><span class="sxs-lookup"><span data-stu-id="dc7aa-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc7aa-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc7aa-133">Requirements</span></span>



| <span data-ttu-id="dc7aa-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc7aa-134">Requirement</span></span> | <span data-ttu-id="dc7aa-135">Wert</span><span class="sxs-lookup"><span data-stu-id="dc7aa-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7aa-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc7aa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dc7aa-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc7aa-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc7aa-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc7aa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dc7aa-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dc7aa-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dc7aa-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc7aa-140">Namespace</span></span><br/>                | <span data-ttu-id="dc7aa-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dc7aa-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dc7aa-142">MOF</span><span class="sxs-lookup"><span data-stu-id="dc7aa-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc7aa-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc7aa-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc7aa-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dc7aa-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc7aa-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc7aa-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc7aa-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc7aa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7aa-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="dc7aa-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

