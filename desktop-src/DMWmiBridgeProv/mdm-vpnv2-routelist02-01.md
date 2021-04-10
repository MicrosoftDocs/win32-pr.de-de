---
title: MDM_VPNv2_RouteList02_01-Klasse
description: Die MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse enthält eine optionale Liste der Routen, die der Routing Tabelle für die VPN-Schnittstelle hinzugefügt werden sollen.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01-Klasse
- MDM_VPNv2_RouteList02_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040827"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a><span data-ttu-id="b9c93-105">MDM \_ VPNv2 \_ RouteList02 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9c93-105">MDM\_VPNv2\_RouteList02\_01 class</span></span>

<span data-ttu-id="b9c93-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b9c93-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b9c93-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b9c93-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b9c93-108">Die **MDM \_ VPNv2 \_ RouteList02 \_ 01** -Klasse enthält eine optionale Liste der Routen, die der Routing Tabelle für die VPN-Schnittstelle hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9c93-108">The **MDM\_VPNv2\_RouteList02\_01** class contains an optional list of routes to be added to the routing table for the VPN interface.</span></span>

<span data-ttu-id="b9c93-109">Dies ist erforderlich, wenn die VPN-Serversite über mehr Subnetze verfügt, die auf der IP-Adresse basieren, die der Schnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b9c93-109">This is required for split tunneling case where the VPN server site has more subnets that the default subnet based on the IP assigned to the interface.</span></span>

<span data-ttu-id="b9c93-110">Alle Computer, auf denen TCP/IP ausgeführt wird, treffen Routing Entscheidungen.</span><span class="sxs-lookup"><span data-stu-id="b9c93-110">Every computer that runs TCP/IP makes routing decisions.</span></span> <span data-ttu-id="b9c93-111">Diese Entscheidungen werden von der IP-Routing Tabelle gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b9c93-111">These decisions are controlled by the IP routing table.</span></span> <span data-ttu-id="b9c93-112">Durch das Hinzufügen von Werten unter diesem Knoten wird die Routing Tabelle mit Routen für die VPN-Schnittstelle nach Verbindung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b9c93-112">Adding values under this node updates the routing table with routes for the VPN interface post connection.</span></span> <span data-ttu-id="b9c93-113">Die Werte unter diesem Knoten stellen das Ziel Präfix von IP-Routen dar.</span><span class="sxs-lookup"><span data-stu-id="b9c93-113">The values under this node represent the destination prefix of IP routes.</span></span> <span data-ttu-id="b9c93-114">Ein Ziel Präfix besteht aus einem IP-Adress Präfix und einer Präfix Länge.</span><span class="sxs-lookup"><span data-stu-id="b9c93-114">A destination prefix consists of an IP address prefix and a prefix length.</span></span>

<span data-ttu-id="b9c93-115">Wenn Sie hier eine Route hinzufügen, kann der Netzwerk Stapel den Datenverkehr ermitteln, der über die VPN-Schnittstelle für Split-Tunnel-VPN geleitet werden muss.</span><span class="sxs-lookup"><span data-stu-id="b9c93-115">Adding a route here allows the networking stack to identify the traffic that needs to go over the VPN interface for split tunnel VPN.</span></span> <span data-ttu-id="b9c93-116">Einige VPN-Server können dies während der Verbindungs Verhandlung konfigurieren und benötigen diese Informationen nicht im VPN-Profil.</span><span class="sxs-lookup"><span data-stu-id="b9c93-116">Some VPN servers can configure this during connect negotiation and do not need this information in the VPN Profile.</span></span> <span data-ttu-id="b9c93-117">Wenden Sie sich an den VPN-Server Administrator, um zu ermitteln, ob Sie diese Informationen im VPN-Profil benötigen.</span><span class="sxs-lookup"><span data-stu-id="b9c93-117">Please check with your VPN server administrator to determine whether you need this information in the VPN profile.</span></span>

<span data-ttu-id="b9c93-118">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b9c93-118">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c93-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9c93-119">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a><span data-ttu-id="b9c93-120">Member</span><span class="sxs-lookup"><span data-stu-id="b9c93-120">Members</span></span>

<span data-ttu-id="b9c93-121">Die **MDM \_ VPNv2 \_ RouteList02 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b9c93-121">The **MDM\_VPNv2\_RouteList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="b9c93-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9c93-122">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9c93-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9c93-123">Properties</span></span>

<span data-ttu-id="b9c93-124">Die **MDM \_ VPNv2 \_ RouteList02 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9c93-124">The **MDM\_VPNv2\_RouteList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b9c93-125">Adresse</span><span class="sxs-lookup"><span data-stu-id="b9c93-125">Address</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c93-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9c93-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c93-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9c93-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b9c93-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b9c93-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c93-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9c93-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c93-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9c93-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9c93-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9c93-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9c93-132">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="b9c93-132">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="b9c93-133">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b9c93-133">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c93-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9c93-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c93-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9c93-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9c93-136">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9c93-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9c93-137">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="b9c93-137">Describes the full path to the parent node.</span></span> <span data-ttu-id="b9c93-138">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/RouteList".</span><span class="sxs-lookup"><span data-stu-id="b9c93-138">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span></span>

</dd> <dt>

[<span data-ttu-id="b9c93-139">Prefixsize</span><span class="sxs-lookup"><span data-stu-id="b9c93-139">PrefixSize</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c93-140">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c93-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c93-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b9c93-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9c93-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9c93-142">Requirements</span></span>



| <span data-ttu-id="b9c93-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9c93-143">Requirement</span></span> | <span data-ttu-id="b9c93-144">Wert</span><span class="sxs-lookup"><span data-stu-id="b9c93-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c93-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9c93-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c93-146">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9c93-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9c93-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9c93-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c93-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b9c93-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b9c93-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9c93-149">Namespace</span></span><br/>                | <span data-ttu-id="b9c93-150">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b9c93-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b9c93-151">MOF</span><span class="sxs-lookup"><span data-stu-id="b9c93-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9c93-152"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b9c93-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9c93-153">DLL</span><span class="sxs-lookup"><span data-stu-id="b9c93-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9c93-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9c93-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9c93-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9c93-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c93-156">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="b9c93-156">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

