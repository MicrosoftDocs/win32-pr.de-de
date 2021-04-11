---
title: MDM_VPNv2_Authentication03-Klasse
description: Die MDM \_ VPNv2 \_ Authentication03-Klasse enthält Authentifizierungsinformationen für das Native VPN-Profil.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- MDM_VPNv2_Authentication03-Klasse
- MDM_VPNv2_Authentication03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040626"
---
# <a name="mdm_vpnv2_authentication03-class"></a><span data-ttu-id="18a36-105">MDM \_ VPNv2 \_ Authentication03-Klasse</span><span class="sxs-lookup"><span data-stu-id="18a36-105">MDM\_VPNv2\_Authentication03 class</span></span>

<span data-ttu-id="18a36-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="18a36-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="18a36-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="18a36-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="18a36-108">Die [**MDM \_ VPNv2 \_ Authentication03**](mdm-vpnv2-01.md) -Klasse enthält Authentifizierungsinformationen für das Native VPN-Profil.</span><span class="sxs-lookup"><span data-stu-id="18a36-108">The [**MDM\_VPNv2\_Authentication03**](mdm-vpnv2-01.md) class contains authentication information for the native VPN profile.</span></span>

<span data-ttu-id="18a36-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="18a36-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a36-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="18a36-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a><span data-ttu-id="18a36-111">Member</span><span class="sxs-lookup"><span data-stu-id="18a36-111">Members</span></span>

<span data-ttu-id="18a36-112">Die **MDM \_ VPNv2 \_ Authentication03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18a36-112">The **MDM\_VPNv2\_Authentication03** class has these types of members:</span></span>

-   [<span data-ttu-id="18a36-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18a36-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18a36-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18a36-114">Properties</span></span>

<span data-ttu-id="18a36-115">Die **MDM \_ VPNv2 \_ Authentication03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="18a36-115">The **MDM\_VPNv2\_Authentication03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18a36-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18a36-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18a36-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18a36-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18a36-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18a36-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18a36-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18a36-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18a36-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="18a36-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="18a36-121">Machinemethod</span><span class="sxs-lookup"><span data-stu-id="18a36-121">MachineMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18a36-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18a36-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18a36-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="18a36-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18a36-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="18a36-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18a36-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18a36-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18a36-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="18a36-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18a36-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18a36-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18a36-128">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="18a36-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="18a36-129">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/NativeProfile".</span><span class="sxs-lookup"><span data-stu-id="18a36-129">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="18a36-130">UserMethod</span><span class="sxs-lookup"><span data-stu-id="18a36-130">UserMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="18a36-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="18a36-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18a36-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="18a36-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18a36-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18a36-133">Requirements</span></span>



| <span data-ttu-id="18a36-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18a36-134">Requirement</span></span> | <span data-ttu-id="18a36-135">Wert</span><span class="sxs-lookup"><span data-stu-id="18a36-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a36-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18a36-136">Minimum supported client</span></span><br/> | <span data-ttu-id="18a36-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18a36-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18a36-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18a36-138">Minimum supported server</span></span><br/> | <span data-ttu-id="18a36-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="18a36-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="18a36-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="18a36-140">Namespace</span></span><br/>                | <span data-ttu-id="18a36-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="18a36-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="18a36-142">MOF</span><span class="sxs-lookup"><span data-stu-id="18a36-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18a36-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="18a36-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="18a36-144">DLL</span><span class="sxs-lookup"><span data-stu-id="18a36-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18a36-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18a36-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a36-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18a36-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a36-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="18a36-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

