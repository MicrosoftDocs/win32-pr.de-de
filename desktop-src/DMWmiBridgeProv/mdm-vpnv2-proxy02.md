---
title: MDM_VPNv2_Proxy02-Klasse
description: Die MDM \_ VPNv2 \_ Proxy02-Klasse definiert ein Konfigurationsobjekt, um eine Post-Connect-Proxy Unterstützung für VPN zu aktivieren.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- MDM_VPNv2_Proxy02-Klasse
- MDM_VPNv2_Proxy02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476767"
---
# <a name="mdm_vpnv2_proxy02-class"></a><span data-ttu-id="359df-105">MDM \_ VPNv2 \_ Proxy02-Klasse</span><span class="sxs-lookup"><span data-stu-id="359df-105">MDM\_VPNv2\_Proxy02 class</span></span>

<span data-ttu-id="359df-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="359df-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="359df-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="359df-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="359df-108">Die **MDM \_ VPNv2 \_ Proxy02** -Klasse definiert ein Konfigurationsobjekt, um eine Post-Connect-Proxy Unterstützung für VPN zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="359df-108">The **MDM\_VPNv2\_Proxy02** class defines a configuration object to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="359df-109">Der Proxy, der für dieses Profil definiert ist, wird angewendet, wenn dieses Profil aktiv und verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="359df-109">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

<span data-ttu-id="359df-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="359df-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="359df-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="359df-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a><span data-ttu-id="359df-112">Member</span><span class="sxs-lookup"><span data-stu-id="359df-112">Members</span></span>

<span data-ttu-id="359df-113">Die **MDM \_ VPNv2 \_ Proxy02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="359df-113">The **MDM\_VPNv2\_Proxy02** class has these types of members:</span></span>

-   [<span data-ttu-id="359df-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="359df-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="359df-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="359df-115">Properties</span></span>

<span data-ttu-id="359df-116">Die **MDM \_ VPNv2 \_ Proxy02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="359df-116">The **MDM\_VPNv2\_Proxy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="359df-117">AutoConfigUrl</span><span class="sxs-lookup"><span data-stu-id="359df-117">AutoConfigUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="359df-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="359df-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="359df-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="359df-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="359df-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="359df-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="359df-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="359df-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="359df-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="359df-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="359df-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="359df-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="359df-124">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="359df-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="359df-125">Eine Auflistung von Konfigurationsobjekten, die eine Post-Connect-Proxy Unterstützung für VPN aktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="359df-125">A collection of configuration objects to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="359df-126">Der Proxy, der für dieses Profil definiert ist, wird angewendet, wenn dieses Profil aktiv und verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="359df-126">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

</dd> <dt>

<span data-ttu-id="359df-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="359df-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="359df-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="359df-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="359df-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="359df-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="359df-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="359df-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="359df-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="359df-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="359df-132">Für diese Klasse ist die Zeichen *Folge "./Vendor/MSFT/VPNv2/profile* Name".</span><span class="sxs-lookup"><span data-stu-id="359df-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="359df-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="359df-133">Requirements</span></span>



| <span data-ttu-id="359df-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="359df-134">Requirement</span></span> | <span data-ttu-id="359df-135">Wert</span><span class="sxs-lookup"><span data-stu-id="359df-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="359df-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="359df-136">Minimum supported client</span></span><br/> | <span data-ttu-id="359df-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="359df-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="359df-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="359df-138">Minimum supported server</span></span><br/> | <span data-ttu-id="359df-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="359df-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="359df-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="359df-140">Namespace</span></span><br/>                | <span data-ttu-id="359df-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="359df-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="359df-142">MOF</span><span class="sxs-lookup"><span data-stu-id="359df-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="359df-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="359df-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="359df-144">DLL</span><span class="sxs-lookup"><span data-stu-id="359df-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="359df-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="359df-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="359df-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="359df-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359df-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="359df-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

