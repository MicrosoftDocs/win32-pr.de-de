---
title: MDM_Firewall_PublicProfile02-Klasse
description: Die MDM- \_ Firewall \_ PublicProfile02-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.
ms.assetid: 5524b931-10fa-43dc-8901-238312ecb6a8
keywords:
- MDM_Firewall_PublicProfile02-Klasse
- MDM_Firewall_PublicProfile02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Firewall_PublicProfile02
- MDM_Firewall_PublicProfile02.InstanceID
- MDM_Firewall_PublicProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530bac28c33b9ed3937f962a7f040e82b2ee1919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476044"
---
# <a name="mdm_firewall_publicprofile02-class"></a><span data-ttu-id="d575f-105">MDM- \_ Firewall \_ PublicProfile02-Klasse</span><span class="sxs-lookup"><span data-stu-id="d575f-105">MDM\_Firewall\_PublicProfile02 class</span></span>

<span data-ttu-id="d575f-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d575f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d575f-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d575f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d575f-108">Die MDM- \_ Firewall \_ PublicProfile02-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d575f-108">The MDM\_Firewall\_PublicProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="d575f-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d575f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d575f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d575f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PublicProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a><span data-ttu-id="d575f-111">Member</span><span class="sxs-lookup"><span data-stu-id="d575f-111">Members</span></span>

<span data-ttu-id="d575f-112">Die **MDM- \_ Firewall \_ PublicProfile02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d575f-112">The **MDM\_Firewall\_PublicProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="d575f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d575f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d575f-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d575f-114">Properties</span></span>

<span data-ttu-id="d575f-115">Die **MDM- \_ Firewall \_ PublicProfile02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d575f-115">The **MDM\_Firewall\_PublicProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d575f-116">Allowlocalipsecpolicymerge</span><span class="sxs-lookup"><span data-stu-id="d575f-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-119">Allowlocalpolicymerge</span><span class="sxs-lookup"><span data-stu-id="d575f-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-122">Authappsallowuserpräfemerge</span><span class="sxs-lookup"><span data-stu-id="d575f-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-125">Defaultinboundaction</span><span class="sxs-lookup"><span data-stu-id="d575f-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-128">Defaultoutboundaction</span><span class="sxs-lookup"><span data-stu-id="d575f-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-131">Disableinboundbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d575f-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-134">Disablestealthmode</span><span class="sxs-lookup"><span data-stu-id="d575f-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-137">Disablestealthmodeipsecsecuredpacketexemption</span><span class="sxs-lookup"><span data-stu-id="d575f-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-140">Disableunicastresponabstomulticastbroadcast</span><span class="sxs-lookup"><span data-stu-id="d575f-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="d575f-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-146">Globalportsallowuserpräfemerge</span><span class="sxs-lookup"><span data-stu-id="d575f-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d575f-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d575f-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d575f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d575f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d575f-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d575f-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d575f-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d575f-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d575f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d575f-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d575f-156">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d575f-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575f-157">Geschützt</span><span class="sxs-lookup"><span data-stu-id="d575f-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575f-158">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d575f-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d575f-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d575f-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d575f-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d575f-160">Requirements</span></span>



| <span data-ttu-id="d575f-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d575f-161">Requirement</span></span> | <span data-ttu-id="d575f-162">Wert</span><span class="sxs-lookup"><span data-stu-id="d575f-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d575f-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d575f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d575f-164">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d575f-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d575f-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d575f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d575f-166">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d575f-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d575f-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="d575f-167">Namespace</span></span><br/>                | <span data-ttu-id="d575f-168">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d575f-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="d575f-169">MOF</span><span class="sxs-lookup"><span data-stu-id="d575f-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d575f-170"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d575f-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="d575f-171">DLL</span><span class="sxs-lookup"><span data-stu-id="d575f-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d575f-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d575f-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

