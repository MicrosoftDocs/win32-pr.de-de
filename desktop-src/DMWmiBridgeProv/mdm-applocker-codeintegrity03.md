---
title: MDM_AppLocker_CodeIntegrity03-Klasse
description: Die MDM \_ AppLocker \_ CodeIntegrity03-Klasse definiert die Richtlinie für die Code Integrität.
ms.assetid: 8e7649b4-2e89-4d79-923e-3767e5b0ea52
keywords:
- MDM_AppLocker_CodeIntegrity03-Klasse
- MDM_AppLocker_CodeIntegrity03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_CodeIntegrity03
- MDM_AppLocker_CodeIntegrity03.InstanceID
- MDM_AppLocker_CodeIntegrity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff702f2887f47c1cc5fcebeb4b8ec9a08c450b8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741201"
---
# <a name="mdm_applocker_codeintegrity03-class"></a><span data-ttu-id="7bb3d-105">MDM \_ AppLocker \_ CodeIntegrity03-Klasse</span><span class="sxs-lookup"><span data-stu-id="7bb3d-105">MDM\_AppLocker\_CodeIntegrity03 class</span></span>

<span data-ttu-id="7bb3d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7bb3d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="7bb3d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7bb3d-108">Die **MDM \_ AppLocker \_ CodeIntegrity03** -Klasse definiert die Richtlinie für die Code Integrität.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-108">The **MDM\_AppLocker\_CodeIntegrity03** class defines the policy for Code Integrity.</span></span>

<span data-ttu-id="7bb3d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb3d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bb3d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_CodeIntegrity03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="7bb3d-111">Member</span><span class="sxs-lookup"><span data-stu-id="7bb3d-111">Members</span></span>

<span data-ttu-id="7bb3d-112">Die **MDM \_ AppLocker \_ CodeIntegrity03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7bb3d-112">The **MDM\_AppLocker\_CodeIntegrity03** class has these types of members:</span></span>

-   [<span data-ttu-id="7bb3d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7bb3d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bb3d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7bb3d-114">Properties</span></span>

<span data-ttu-id="7bb3d-115">Die **MDM- \_ AppLocker- \_ CodeIntegrity03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-115">The **MDM\_AppLocker\_CodeIntegrity03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bb3d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bb3d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bb3d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7bb3d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bb3d-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bb3d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7bb3d-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="7bb3d-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bb3d-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bb3d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7bb3d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bb3d-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bb3d-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7bb3d-125">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="7bb3d-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="7bb3d-126">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions".</span><span class="sxs-lookup"><span data-stu-id="7bb3d-126">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="7bb3d-127">**Policy**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-127">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bb3d-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bb3d-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7bb3d-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7bb3d-130">**Qualifizierer: octetstring**</span><span class="sxs-lookup"><span data-stu-id="7bb3d-130">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bb3d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bb3d-131">Requirements</span></span>



| <span data-ttu-id="7bb3d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bb3d-132">Requirement</span></span> | <span data-ttu-id="7bb3d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7bb3d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb3d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bb3d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb3d-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7bb3d-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7bb3d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bb3d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb3d-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7bb3d-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7bb3d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bb3d-138">Namespace</span></span><br/>                | <span data-ttu-id="7bb3d-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7bb3d-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7bb3d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7bb3d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bb3d-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7bb3d-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bb3d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7bb3d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bb3d-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bb3d-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb3d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bb3d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb3d-145">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="7bb3d-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

