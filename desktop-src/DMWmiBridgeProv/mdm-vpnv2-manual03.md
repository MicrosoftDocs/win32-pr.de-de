---
title: MDM_VPNv2_Manual03-Klasse
description: Die MDM- \_ VPNv2 \_ Manual03class ist ein optionaler Knoten, der die manuellen Servereinstellungen enthält.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- MDM_VPNv2_Manual03-Klasse
- MDM_VPNv2_Manual03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957031"
---
# <a name="mdm_vpnv2_manual03-class"></a><span data-ttu-id="85fbc-105">MDM \_ VPNv2 \_ Manual03-Klasse</span><span class="sxs-lookup"><span data-stu-id="85fbc-105">MDM\_VPNv2\_Manual03 class</span></span>

<span data-ttu-id="85fbc-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="85fbc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="85fbc-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="85fbc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="85fbc-108">Die **MDM \_ VPNv2 \_ Manual03**-Klasse ist ein optionaler Knoten, der die manuellen Servereinstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="85fbc-108">The **MDM\_VPNv2\_Manual03** class is an optional node containing the manual server settings.</span></span>

<span data-ttu-id="85fbc-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="85fbc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="85fbc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="85fbc-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a><span data-ttu-id="85fbc-111">Member</span><span class="sxs-lookup"><span data-stu-id="85fbc-111">Members</span></span>

<span data-ttu-id="85fbc-112">Die **MDM \_ VPNv2 \_ Manual03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="85fbc-112">The **MDM\_VPNv2\_Manual03** class has these types of members:</span></span>

-   [<span data-ttu-id="85fbc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85fbc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85fbc-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85fbc-114">Properties</span></span>

<span data-ttu-id="85fbc-115">Die **MDM \_ VPNv2 \_ Manual03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85fbc-115">The **MDM\_VPNv2\_Manual03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85fbc-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="85fbc-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85fbc-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85fbc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85fbc-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85fbc-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85fbc-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85fbc-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="85fbc-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="85fbc-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="85fbc-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="85fbc-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85fbc-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85fbc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85fbc-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85fbc-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85fbc-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="85fbc-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="85fbc-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="85fbc-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="85fbc-126">Für diese Klasse ist die Zeichenfolge "*./Vendor/MSFT/VPNv2/profile* Name/Proxy/".</span><span class="sxs-lookup"><span data-stu-id="85fbc-126">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span></span>

</dd> <dt>

[<span data-ttu-id="85fbc-127">Server</span><span class="sxs-lookup"><span data-stu-id="85fbc-127">Server</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

<span data-ttu-id="85fbc-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="85fbc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85fbc-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="85fbc-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85fbc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85fbc-130">Requirements</span></span>



| <span data-ttu-id="85fbc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85fbc-131">Requirement</span></span> | <span data-ttu-id="85fbc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="85fbc-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85fbc-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85fbc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="85fbc-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85fbc-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85fbc-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85fbc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="85fbc-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="85fbc-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="85fbc-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="85fbc-137">Namespace</span></span><br/>                | <span data-ttu-id="85fbc-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="85fbc-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="85fbc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="85fbc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85fbc-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="85fbc-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="85fbc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="85fbc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85fbc-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85fbc-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85fbc-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85fbc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85fbc-144">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="85fbc-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

