---
title: MDM_VPNv2_Certificate04-Klasse
description: Reserviert für zukünftige Verwendung.
ms.assetid: 0fa831e0-918a-472f-88bf-7e40c4081417
keywords:
- MDM_VPNv2_Certificate04-Klasse
- MDM_VPNv2_Certificate04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04.InstanceID
- MDM_VPNv2_Certificate04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88bd26e8dc9916e7e2db97b980065d7a8733ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956482"
---
# <a name="mdm_vpnv2_certificate04-class"></a><span data-ttu-id="dd2b5-105">MDM \_ VPNv2 \_ Certificate04-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd2b5-105">MDM\_VPNv2\_Certificate04 class</span></span>

<span data-ttu-id="dd2b5-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dd2b5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd2b5-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="dd2b5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd2b5-108">Für zukünftige Verwendung reserviert</span><span class="sxs-lookup"><span data-stu-id="dd2b5-108">Reserved for future Use</span></span>

<span data-ttu-id="dd2b5-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd2b5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2b5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd2b5-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Certificate04
{
  string InstanceID;
  string ParentID;
  string Issuer;
  string Eku;
};
```

## <a name="members"></a><span data-ttu-id="dd2b5-111">Member</span><span class="sxs-lookup"><span data-stu-id="dd2b5-111">Members</span></span>

<span data-ttu-id="dd2b5-112">Die **MDM \_ VPNv2 \_ Certificate04** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd2b5-112">The **MDM\_VPNv2\_Certificate04** class has these types of members:</span></span>

-   [<span data-ttu-id="dd2b5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd2b5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd2b5-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd2b5-114">Properties</span></span>

<span data-ttu-id="dd2b5-115">Die **MDM \_ VPNv2 \_ Certificate04** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd2b5-115">The **MDM\_VPNv2\_Certificate04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dd2b5-116">EKU</span><span class="sxs-lookup"><span data-stu-id="dd2b5-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2b5-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd2b5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2b5-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd2b5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd2b5-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd2b5-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2b5-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd2b5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2b5-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd2b5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd2b5-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd2b5-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd2b5-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="dd2b5-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="dd2b5-124">Für diese Klasse ist die Zeichenfolge "EAP".</span><span class="sxs-lookup"><span data-stu-id="dd2b5-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

[<span data-ttu-id="dd2b5-125">Aussteller</span><span class="sxs-lookup"><span data-stu-id="dd2b5-125">Issuer</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-issuer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2b5-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd2b5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2b5-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dd2b5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd2b5-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd2b5-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd2b5-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd2b5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd2b5-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd2b5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd2b5-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd2b5-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd2b5-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="dd2b5-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="dd2b5-133">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/NativeProfile/Authentication".</span><span class="sxs-lookup"><span data-stu-id="dd2b5-133">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd2b5-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd2b5-134">Requirements</span></span>



| <span data-ttu-id="dd2b5-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd2b5-135">Requirement</span></span> | <span data-ttu-id="dd2b5-136">Wert</span><span class="sxs-lookup"><span data-stu-id="dd2b5-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2b5-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd2b5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2b5-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd2b5-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd2b5-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd2b5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2b5-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd2b5-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd2b5-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd2b5-141">Namespace</span></span><br/>                | <span data-ttu-id="dd2b5-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dd2b5-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dd2b5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="dd2b5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd2b5-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd2b5-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd2b5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2b5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd2b5-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd2b5-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2b5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd2b5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2b5-148">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="dd2b5-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

