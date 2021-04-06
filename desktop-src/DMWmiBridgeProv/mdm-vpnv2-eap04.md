---
title: MDM_VPNv2_Eap04-Klasse
description: Die MDM \_ VPNv2 \_ Eap04-Klasse enthält die erforderlichen XML-Konfigurationsinformationen, wenn das Native Profil die EAP-Authentifizierung angibt.
ms.assetid: 87a78743-1ee6-4b86-bfbf-62ba9059535a
keywords:
- MDM_VPNv2_Eap04-Klasse
- MDM_VPNv2_Eap04-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04.InstanceID
- MDM_VPNv2_Eap04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9270bf1cae37c345fe81be674e9d9afc2c533bc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743161"
---
# <a name="mdm_vpnv2_eap04-class"></a><span data-ttu-id="8dfdb-105">MDM \_ VPNv2 \_ Eap04-Klasse</span><span class="sxs-lookup"><span data-stu-id="8dfdb-105">MDM\_VPNv2\_Eap04 class</span></span>

<span data-ttu-id="8dfdb-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8dfdb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8dfdb-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8dfdb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8dfdb-108">Die **MDM \_ VPNv2 \_ Eap04** -Klasse enthält die erforderlichen XML-Konfigurationsinformationen, wenn das Native Profil die EAP-Authentifizierung angibt.</span><span class="sxs-lookup"><span data-stu-id="8dfdb-108">The **MDM\_VPNv2\_Eap04** class contains the required configuration XML information when the native profile specifies EAP authentication.</span></span>

<span data-ttu-id="8dfdb-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8dfdb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfdb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dfdb-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Eap04
{
  string InstanceID;
  string ParentID;
  string Configuration;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="8dfdb-111">Member</span><span class="sxs-lookup"><span data-stu-id="8dfdb-111">Members</span></span>

<span data-ttu-id="8dfdb-112">Die **MDM \_ VPNv2 \_ Eap04** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8dfdb-112">The **MDM\_VPNv2\_Eap04** class has these types of members:</span></span>

-   [<span data-ttu-id="8dfdb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dfdb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dfdb-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dfdb-114">Properties</span></span>

<span data-ttu-id="8dfdb-115">Die **MDM \_ VPNv2 \_ Eap04** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8dfdb-115">The **MDM\_VPNv2\_Eap04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8dfdb-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="8dfdb-116">Configuration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-eap-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdb-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dfdb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdb-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dfdb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8dfdb-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8dfdb-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdb-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dfdb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdb-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dfdb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dfdb-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dfdb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dfdb-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="8dfdb-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="8dfdb-124">Für diese Klasse ist die Zeichenfolge "EAP".</span><span class="sxs-lookup"><span data-stu-id="8dfdb-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

<span data-ttu-id="8dfdb-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8dfdb-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdb-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8dfdb-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdb-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8dfdb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8dfdb-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8dfdb-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8dfdb-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="8dfdb-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="8dfdb-130">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/NativeProfile/Authentication".</span><span class="sxs-lookup"><span data-stu-id="8dfdb-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> <dt>

[<span data-ttu-id="8dfdb-131">Type</span><span class="sxs-lookup"><span data-stu-id="8dfdb-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfdb-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8dfdb-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dfdb-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8dfdb-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dfdb-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dfdb-134">Requirements</span></span>



| <span data-ttu-id="8dfdb-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dfdb-135">Requirement</span></span> | <span data-ttu-id="8dfdb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="8dfdb-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfdb-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dfdb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfdb-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8dfdb-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8dfdb-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dfdb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfdb-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8dfdb-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8dfdb-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dfdb-141">Namespace</span></span><br/>                | <span data-ttu-id="8dfdb-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8dfdb-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8dfdb-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8dfdb-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8dfdb-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8dfdb-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8dfdb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8dfdb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dfdb-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dfdb-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dfdb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dfdb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfdb-148">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="8dfdb-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

