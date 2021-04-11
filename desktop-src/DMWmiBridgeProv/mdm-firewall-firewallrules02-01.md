---
title: MDM_Firewall_FirewallRules02_01-Klasse
description: Die MDM- \_ Firewall \_ FirewallRules02 01- \_ Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.
ms.assetid: b09cbd98-152e-486c-acb5-4e1d83e5f8e2
keywords:
- MDM_Firewall_FirewallRules02_01-Klasse
- MDM_Firewall_FirewallRules02_01-Klasse, beschrieben
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01.InstanceID
- MDM_Firewall_FirewallRules02_01.ParentID
- MDM_Firewall_FirewallRules02_01.IcmpTypesAndCodes
- MDM_Firewall_FirewallRules02_01.FriendlyName
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 494be18ece91e7a1776780542f988b80cb822e42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103334"
---
# <a name="mdm_firewall_firewallrules02_01-class"></a><span data-ttu-id="d2c97-105">MDM- \_ Firewall \_ FirewallRules02 01- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="d2c97-105">MDM\_Firewall\_FirewallRules02\_01 class</span></span>

<span data-ttu-id="d2c97-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d2c97-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d2c97-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d2c97-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d2c97-108">Die MDM- \_ Firewall \_ FirewallRules02 01- \_ Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d2c97-108">The MDM\_Firewall\_FirewallRules02\_01 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="d2c97-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d2c97-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c97-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2c97-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_FirewallRules02_01
{
  string  InstanceID;
  string  ParentID;
  sint32  Protocol;
  string  LocalPortRanges;
  string  RemotePortRanges;
  string  LocalAddressRanges;
  string  RemoteAddressRanges;
  string  Description;
  boolean Enabled;
  sint32  Profiles;
  string  Direction;
  string  InterfaceTypes;
  string  IcmpTypesAndCodes;
  boolean EdgeTraversal;
  string  LocalUserAuthorizedList;
  string  Status;
  string  FriendlyName;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="d2c97-111">Member</span><span class="sxs-lookup"><span data-stu-id="d2c97-111">Members</span></span>

<span data-ttu-id="d2c97-112">Die **MDM- \_ Firewall \_ FirewallRules02 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d2c97-112">The **MDM\_Firewall\_FirewallRules02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="d2c97-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2c97-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2c97-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2c97-114">Properties</span></span>

<span data-ttu-id="d2c97-115">Die **MDM- \_ Firewall \_ FirewallRules02 \_ 01** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2c97-115">The **MDM\_Firewall\_FirewallRules02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d2c97-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2c97-116">Description</span></span>](/windows/client-management/mdm/firewall-csp#description)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-119">Richtung</span><span class="sxs-lookup"><span data-stu-id="d2c97-119">Direction</span></span>](/windows/client-management/mdm/firewall-csp#direction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-122">Edgetraversal</span><span class="sxs-lookup"><span data-stu-id="d2c97-122">EdgeTraversal</span></span>](/windows/client-management/mdm/firewall-csp#edgetraversal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d2c97-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-125">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d2c97-125">Enabled</span></span>](/windows/client-management/mdm/firewall-csp#enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d2c97-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2c97-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="d2c97-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d2c97-131">TBD</span><span class="sxs-lookup"><span data-stu-id="d2c97-131">TBD</span></span>

</dd> <dt>

<span data-ttu-id="d2c97-132">**Icmptypesandcodes**</span><span class="sxs-lookup"><span data-stu-id="d2c97-132">**IcmpTypesAndCodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d2c97-135">TBD</span><span class="sxs-lookup"><span data-stu-id="d2c97-135">TBD</span></span>

</dd> <dt>

<span data-ttu-id="d2c97-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2c97-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2c97-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-139">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d2c97-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-140">Interfaketypes</span><span class="sxs-lookup"><span data-stu-id="d2c97-140">InterfaceTypes</span></span>](/windows/client-management/mdm/firewall-csp#interfacetypes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-143">Localaddressranges</span><span class="sxs-lookup"><span data-stu-id="d2c97-143">LocalAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-146">Localportranges</span><span class="sxs-lookup"><span data-stu-id="d2c97-146">LocalPortRanges</span></span>](/windows/client-management/mdm/firewall-csp#localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-149">Localuserauthorizedlist</span><span class="sxs-lookup"><span data-stu-id="d2c97-149">LocalUserAuthorizedList</span></span>](/windows/client-management/mdm/firewall-csp#localuserauthorizedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-152">Name</span><span class="sxs-lookup"><span data-stu-id="d2c97-152">Name</span></span>](/windows/client-management/mdm/firewall-csp#name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2c97-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d2c97-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d2c97-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-158">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d2c97-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-159">Profiles</span><span class="sxs-lookup"><span data-stu-id="d2c97-159">Profiles</span></span>](/windows/client-management/mdm/firewall-csp#profiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-160">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d2c97-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-161">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-162">Protokoll</span><span class="sxs-lookup"><span data-stu-id="d2c97-162">Protocol</span></span>](/windows/client-management/mdm/firewall-csp#protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-163">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d2c97-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-165">Remoteaddressranges</span><span class="sxs-lookup"><span data-stu-id="d2c97-165">RemoteAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-168">Remoteportranges</span><span class="sxs-lookup"><span data-stu-id="d2c97-168">RemotePortRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2c97-171">Status</span><span class="sxs-lookup"><span data-stu-id="d2c97-171">Status</span></span>](/windows/client-management/mdm/firewall-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2c97-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d2c97-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2c97-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d2c97-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2c97-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2c97-174">Requirements</span></span>



| <span data-ttu-id="d2c97-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2c97-175">Requirement</span></span> | <span data-ttu-id="d2c97-176">Wert</span><span class="sxs-lookup"><span data-stu-id="d2c97-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c97-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2c97-177">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c97-178">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2c97-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d2c97-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2c97-179">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c97-180">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d2c97-180">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d2c97-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2c97-181">Namespace</span></span><br/>                | <span data-ttu-id="d2c97-182">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d2c97-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="d2c97-183">MOF</span><span class="sxs-lookup"><span data-stu-id="d2c97-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2c97-184"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d2c97-184"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2c97-185">DLL</span><span class="sxs-lookup"><span data-stu-id="d2c97-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2c97-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2c97-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

