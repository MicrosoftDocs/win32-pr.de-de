---
title: MDM_VPNv2_01-Klasse
description: Die MDM \_ - \_ Klasse VPNv2 01 ermöglicht die Konfiguration des VPN-Profils des Geräts.
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- MDM_VPNv2_01-Klasse
- MDM_VPNv2_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3457220c438d0143db90c1955d48352353fee29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956628"
---
# <a name="mdm_vpnv2_01-class"></a><span data-ttu-id="9f00b-105">MDM \_ VPNv2 \_ 01-Klasse</span><span class="sxs-lookup"><span data-stu-id="9f00b-105">MDM\_VPNv2\_01 class</span></span>

<span data-ttu-id="9f00b-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9f00b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f00b-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="9f00b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9f00b-108">Die **MDM-Klasse \_ VPNv2 \_ 01** ermöglicht die Konfiguration des VPN-Profils des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f00b-108">The **MDM\_VPNv2\_01** class allows configuration of the VPN profile of the device.</span></span>

<span data-ttu-id="9f00b-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f00b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f00b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f00b-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a><span data-ttu-id="9f00b-111">Member</span><span class="sxs-lookup"><span data-stu-id="9f00b-111">Members</span></span>

<span data-ttu-id="9f00b-112">Die **MDM \_ VPNv2 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9f00b-112">The **MDM\_VPNv2\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="9f00b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f00b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f00b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f00b-114">Properties</span></span>

<span data-ttu-id="9f00b-115">Die **MDM \_ VPNv2 \_ 01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f00b-115">The **MDM\_VPNv2\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9f00b-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="9f00b-116">AlwaysOn</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f00b-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f00b-119">Bypassforlocal</span><span class="sxs-lookup"><span data-stu-id="9f00b-119">ByPassForLocal</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f00b-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f00b-122">DnsSuffix</span><span class="sxs-lookup"><span data-stu-id="9f00b-122">DnsSuffix</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f00b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f00b-125">Edpmodeid</span><span class="sxs-lookup"><span data-stu-id="9f00b-125">EdpModeId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f00b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f00b-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9f00b-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f00b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f00b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f00b-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f00b-132">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="9f00b-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="9f00b-133">Bei dieser Klasse ist die Zeichenfolge der Name des VPN-Profils.</span><span class="sxs-lookup"><span data-stu-id="9f00b-133">For this class, the string is the VPN profile name.</span></span>

</dd> <dt>

[<span data-ttu-id="9f00b-134">Sperrmodus</span><span class="sxs-lookup"><span data-stu-id="9f00b-134">LockDown</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f00b-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f00b-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9f00b-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f00b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f00b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f00b-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f00b-141">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="9f00b-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="9f00b-142">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/VPNv2".</span><span class="sxs-lookup"><span data-stu-id="9f00b-142">For this class, the string is "./Vendor/MSFT/VPNv2"</span></span>

</dd> <dt>

[<span data-ttu-id="9f00b-143">ProfileXML</span><span class="sxs-lookup"><span data-stu-id="9f00b-143">ProfileXML</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f00b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f00b-146">RememberCredentials</span><span class="sxs-lookup"><span data-stu-id="9f00b-146">RememberCredentials</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-147">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f00b-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f00b-149">Treuhänder-networkerkennung</span><span class="sxs-lookup"><span data-stu-id="9f00b-149">TrustedNetworkDetection</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f00b-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f00b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f00b-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9f00b-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f00b-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f00b-152">Requirements</span></span>



| <span data-ttu-id="9f00b-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f00b-153">Requirement</span></span> | <span data-ttu-id="9f00b-154">Wert</span><span class="sxs-lookup"><span data-stu-id="9f00b-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f00b-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f00b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="9f00b-156">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f00b-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f00b-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f00b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="9f00b-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f00b-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9f00b-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f00b-159">Namespace</span></span><br/>                | <span data-ttu-id="9f00b-160">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9f00b-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9f00b-161">MOF</span><span class="sxs-lookup"><span data-stu-id="9f00b-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f00b-162"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f00b-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f00b-163">DLL</span><span class="sxs-lookup"><span data-stu-id="9f00b-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f00b-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f00b-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f00b-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f00b-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f00b-166">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="9f00b-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

