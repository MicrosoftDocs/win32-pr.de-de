---
title: MDM_VPNv2_NativeProfile02-Klasse
description: Die MDM \_ VPNv2 \_ NativeProfile2-Klasse definiert Profilinformationen bei Verwendung eines Windows-Eingangsbox-VPN-Protokolls (IKEv2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- MDM_VPNv2_NativeProfile02-Klasse
- MDM_VPNv2_NativeProfile02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859190"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a><span data-ttu-id="88780-105">MDM \_ VPNv2 \_ NativeProfile02-Klasse</span><span class="sxs-lookup"><span data-stu-id="88780-105">MDM\_VPNv2\_NativeProfile02 class</span></span>

<span data-ttu-id="88780-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="88780-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="88780-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="88780-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="88780-108">Die **MDM \_ VPNv2 \_ NativeProfile2** -Klasse definiert Profilinformationen bei Verwendung eines Windows-Eingangsbox-VPN-Protokolls (IKEv2, PPTP, L2TP).</span><span class="sxs-lookup"><span data-stu-id="88780-108">The **MDM\_VPNv2\_NativeProfile2** class defines profile information when using a Windows Inbox VPN Protocol (IKEv2, PPTP, L2TP).</span></span>

<span data-ttu-id="88780-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88780-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88780-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="88780-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a><span data-ttu-id="88780-111">Member</span><span class="sxs-lookup"><span data-stu-id="88780-111">Members</span></span>

<span data-ttu-id="88780-112">Die **MDM \_ VPNv2 \_ NativeProfile02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="88780-112">The **MDM\_VPNv2\_NativeProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="88780-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88780-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88780-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88780-114">Properties</span></span>

<span data-ttu-id="88780-115">Die **MDM \_ VPNv2 \_ NativeProfile02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88780-115">The **MDM\_VPNv2\_NativeProfile02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88780-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="88780-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88780-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="88780-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88780-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88780-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88780-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88780-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88780-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="88780-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="88780-121">L2tpPsk</span><span class="sxs-lookup"><span data-stu-id="88780-121">L2tpPsk</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

<span data-ttu-id="88780-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="88780-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88780-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="88780-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="88780-124">Nativeprotocoltype</span><span class="sxs-lookup"><span data-stu-id="88780-124">NativeProtocolType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="88780-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="88780-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88780-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="88780-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88780-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="88780-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88780-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="88780-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88780-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="88780-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88780-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88780-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88780-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="88780-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="88780-132">Für diese Klasse ist die Zeichen *Folge "./Vendor/MSFT/VPNv2/profile* Name".</span><span class="sxs-lookup"><span data-stu-id="88780-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="88780-133">Routingpolicytype</span><span class="sxs-lookup"><span data-stu-id="88780-133">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="88780-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="88780-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88780-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="88780-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="88780-136">Server</span><span class="sxs-lookup"><span data-stu-id="88780-136">Servers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="88780-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="88780-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88780-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="88780-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88780-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88780-139">Requirements</span></span>



| <span data-ttu-id="88780-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88780-140">Requirement</span></span> | <span data-ttu-id="88780-141">Wert</span><span class="sxs-lookup"><span data-stu-id="88780-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88780-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88780-142">Minimum supported client</span></span><br/> | <span data-ttu-id="88780-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88780-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88780-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88780-144">Minimum supported server</span></span><br/> | <span data-ttu-id="88780-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="88780-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="88780-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="88780-146">Namespace</span></span><br/>                | <span data-ttu-id="88780-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="88780-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="88780-148">MOF</span><span class="sxs-lookup"><span data-stu-id="88780-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88780-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="88780-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="88780-150">DLL</span><span class="sxs-lookup"><span data-stu-id="88780-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88780-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88780-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88780-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88780-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88780-153">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="88780-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

