---
title: MDM_VPNv2_Sso03-Klasse
description: Die MDM \_ VPNv2 \_ Sso03-Klasse kann verwendet werden, um ein anderes Zertifikat als das VPN-Authentifizierungszertifikat für die Kerberos-Authentifizierung im Fall von Geräte Konformität auszuwählen.
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- MDM_VPNv2_Sso03-Klasse
- MDM_VPNv2_Sso03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5f3f10d365e1405981e206963cd98f0b7f803c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956860"
---
# <a name="mdm_vpnv2_sso03-class"></a><span data-ttu-id="b620d-105">MDM \_ VPNv2 \_ Sso03-Klasse</span><span class="sxs-lookup"><span data-stu-id="b620d-105">MDM\_VPNv2\_Sso03 class</span></span>

<span data-ttu-id="b620d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b620d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b620d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b620d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b620d-108">Die **MDM \_ VPNv2 \_ Sso03** -Klasse kann verwendet werden, um ein anderes Zertifikat als das VPN-Authentifizierungszertifikat für die Kerberos-Authentifizierung im Fall von Geräte Konformität auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b620d-108">The **MDM\_VPNv2\_Sso03** class can be used to select a certificate different from the VPN Authentication certificate for the Kerberos Authentication in the case of Device Compliance.</span></span>

<span data-ttu-id="b620d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b620d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b620d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b620d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a><span data-ttu-id="b620d-111">Member</span><span class="sxs-lookup"><span data-stu-id="b620d-111">Members</span></span>

<span data-ttu-id="b620d-112">Die **MDM \_ VPNv2 \_ Sso03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b620d-112">The **MDM\_VPNv2\_Sso03** class has these types of members:</span></span>

-   [<span data-ttu-id="b620d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b620d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b620d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b620d-114">Properties</span></span>

<span data-ttu-id="b620d-115">Die **MDM \_ VPNv2 \_ Sso03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b620d-115">The **MDM\_VPNv2\_Sso03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b620d-116">EKU</span><span class="sxs-lookup"><span data-stu-id="b620d-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b620d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b620d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b620d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b620d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b620d-119">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b620d-119">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b620d-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b620d-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b620d-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b620d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b620d-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b620d-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b620d-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b620d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b620d-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b620d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b620d-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b620d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b620d-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="b620d-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="b620d-127">Issuerhash</span><span class="sxs-lookup"><span data-stu-id="b620d-127">IssuerHash</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b620d-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b620d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b620d-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b620d-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b620d-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b620d-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b620d-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b620d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b620d-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b620d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b620d-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b620d-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b620d-134">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="b620d-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="b620d-135">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/DeviceCompliance".</span><span class="sxs-lookup"><span data-stu-id="b620d-135">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b620d-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b620d-136">Requirements</span></span>



| <span data-ttu-id="b620d-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b620d-137">Requirement</span></span> | <span data-ttu-id="b620d-138">Wert</span><span class="sxs-lookup"><span data-stu-id="b620d-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b620d-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b620d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b620d-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b620d-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b620d-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b620d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b620d-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b620d-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b620d-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="b620d-143">Namespace</span></span><br/>                | <span data-ttu-id="b620d-144">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b620d-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b620d-145">MOF</span><span class="sxs-lookup"><span data-stu-id="b620d-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b620d-146"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b620d-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b620d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b620d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b620d-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b620d-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b620d-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b620d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b620d-150">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="b620d-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

