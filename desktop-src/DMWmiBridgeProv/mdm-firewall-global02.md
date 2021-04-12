---
title: MDM_Firewall_Global02-Klasse
description: Die MDM- \_ Firewall \_ Global02-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- MDM_Firewall_Global02-Klasse
- MDM_Firewall_Global02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213711"
---
# <a name="mdm_firewall_global02-class"></a><span data-ttu-id="f589c-105">MDM- \_ Firewall \_ Global02-Klasse</span><span class="sxs-lookup"><span data-stu-id="f589c-105">MDM\_Firewall\_Global02 class</span></span>

<span data-ttu-id="f589c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f589c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f589c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="f589c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f589c-108">Die MDM- \_ Firewall \_ Global02-Klasse wird verwendet, um die Windows Defender Firewall-Einstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f589c-108">The MDM\_Firewall\_Global02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="f589c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f589c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f589c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f589c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a><span data-ttu-id="f589c-111">Member</span><span class="sxs-lookup"><span data-stu-id="f589c-111">Members</span></span>

<span data-ttu-id="f589c-112">Die **MDM- \_ Firewall \_ Global02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f589c-112">The **MDM\_Firewall\_Global02** class has these types of members:</span></span>

-   [<span data-ttu-id="f589c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f589c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f589c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f589c-114">Properties</span></span>

<span data-ttu-id="f589c-115">Die **MDM- \_ Firewall \_ Global02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f589c-115">The **MDM\_Firewall\_Global02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f589c-116">Binaryversionsupported</span><span class="sxs-lookup"><span data-stu-id="f589c-116">BinaryVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f589c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-119">Crlcheck</span><span class="sxs-lookup"><span data-stu-id="f589c-119">CRLcheck</span></span>](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f589c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-122">Currentprofiles</span><span class="sxs-lookup"><span data-stu-id="f589c-122">CurrentProfiles</span></span>](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f589c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-125">Disablestatus</span><span class="sxs-lookup"><span data-stu-id="f589c-125">DisableStatefulFtp</span></span>](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f589c-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-128">Enablepacketqueue</span><span class="sxs-lookup"><span data-stu-id="f589c-128">EnablePacketQueue</span></span>](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f589c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f589c-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f589c-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f589c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f589c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f589c-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f589c-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-135">Ipsecausgenommen</span><span class="sxs-lookup"><span data-stu-id="f589c-135">IPsecExempt</span></span>](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-136">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f589c-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-138">Opportunisticallymatchauthsetperkm</span><span class="sxs-lookup"><span data-stu-id="f589c-138">OpportunisticallyMatchAuthSetPerKM</span></span>](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f589c-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f589c-141">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f589c-141">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f589c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f589c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f589c-144">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f589c-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-145">PolicyVersion</span><span class="sxs-lookup"><span data-stu-id="f589c-145">PolicyVersion</span></span>](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f589c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-148">Policyversionsupported</span><span class="sxs-lookup"><span data-stu-id="f589c-148">PolicyVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-149">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f589c-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-151">Presharedkeyencoding</span><span class="sxs-lookup"><span data-stu-id="f589c-151">PresharedKeyEncoding</span></span>](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-152">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f589c-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f589c-154">Saidletime</span><span class="sxs-lookup"><span data-stu-id="f589c-154">SaIdleTime</span></span>](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f589c-155">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f589c-155">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f589c-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f589c-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f589c-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f589c-157">Requirements</span></span>



| <span data-ttu-id="f589c-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f589c-158">Requirement</span></span> | <span data-ttu-id="f589c-159">Wert</span><span class="sxs-lookup"><span data-stu-id="f589c-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f589c-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f589c-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f589c-161">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f589c-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f589c-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f589c-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f589c-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f589c-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f589c-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="f589c-164">Namespace</span></span><br/>                | <span data-ttu-id="f589c-165">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="f589c-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="f589c-166">MOF</span><span class="sxs-lookup"><span data-stu-id="f589c-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f589c-167"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f589c-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="f589c-168">DLL</span><span class="sxs-lookup"><span data-stu-id="f589c-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f589c-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f589c-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

