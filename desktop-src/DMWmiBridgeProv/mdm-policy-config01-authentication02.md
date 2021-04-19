---
title: MDM_Policy_Config01_Authentication02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Authentication02-Klasse stellt die verfügbaren Authentifizierungs Verwaltungsrichtlinien dar.
ms.assetid: 928e0b60-5533-45dc-90e6-be7d70210138
keywords:
- MDM_Policy_Config01_Authentication02-Klasse
- MDM_Policy_Config01_Authentication02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Authentication02
- MDM_Policy_Config01_Authentication02.InstanceID
- MDM_Policy_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfab66a548f4a92c445f748aca1bb15758ac48c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342419"
---
# <a name="mdm_policy_config01_authentication02-class"></a><span data-ttu-id="e86ed-105">MDM- \_ Richtlinie \_ Config01 \_ Authentication02-Klasse</span><span class="sxs-lookup"><span data-stu-id="e86ed-105">MDM\_Policy\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="e86ed-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e86ed-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e86ed-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e86ed-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e86ed-108">Die **MDM- \_ Richtlinie \_ Config01 \_ Authentication02** -Klasse stellt die verfügbaren Authentifizierungs Verwaltungsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="e86ed-108">The **MDM\_Policy\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="e86ed-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e86ed-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86ed-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e86ed-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="e86ed-111">Member</span><span class="sxs-lookup"><span data-stu-id="e86ed-111">Members</span></span>

<span data-ttu-id="e86ed-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Authentication02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e86ed-112">The **MDM\_Policy\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="e86ed-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e86ed-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e86ed-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e86ed-114">Properties</span></span>

<span data-ttu-id="e86ed-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Authentication02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e86ed-115">The **MDM\_Policy\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e86ed-116">Zuordnung von "zukenpasswordreset"</span><span class="sxs-lookup"><span data-stu-id="e86ed-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86ed-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e86ed-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e86ed-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e86ed-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="e86ed-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86ed-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e86ed-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e86ed-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e86ed-122">Allowfdodevicesignon</span><span class="sxs-lookup"><span data-stu-id="e86ed-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86ed-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e86ed-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e86ed-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e86ed-125">Allowsecondaryauthenticationdevice</span><span class="sxs-lookup"><span data-stu-id="e86ed-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86ed-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e86ed-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e86ed-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e86ed-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e86ed-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86ed-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e86ed-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e86ed-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e86ed-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e86ed-132">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="e86ed-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="e86ed-133">Für diese Klasse ist die Zeichenfolge "Authentication".</span><span class="sxs-lookup"><span data-stu-id="e86ed-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="e86ed-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e86ed-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86ed-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e86ed-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e86ed-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86ed-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e86ed-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e86ed-138">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="e86ed-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="e86ed-139">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="e86ed-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e86ed-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e86ed-140">Requirements</span></span>



| <span data-ttu-id="e86ed-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e86ed-141">Requirement</span></span> | <span data-ttu-id="e86ed-142">Wert</span><span class="sxs-lookup"><span data-stu-id="e86ed-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e86ed-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e86ed-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e86ed-144">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e86ed-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e86ed-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e86ed-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e86ed-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e86ed-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e86ed-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="e86ed-147">Namespace</span></span><br/>                | <span data-ttu-id="e86ed-148">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e86ed-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e86ed-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e86ed-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e86ed-150"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e86ed-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e86ed-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e86ed-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e86ed-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e86ed-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86ed-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e86ed-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86ed-154">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="e86ed-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

