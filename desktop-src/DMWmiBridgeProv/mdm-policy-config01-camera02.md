---
title: MDM_Policy_Config01_Camera02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Camera02-Klasse stellt die verfügbaren Kamera Richtlinien dar.
ms.assetid: dd17c2bc-8c96-4f5e-a4d2-cf1d27a92eb7
keywords:
- MDM_Policy_Config01_Camera02-Klasse
- MDM_Policy_Config01_Camera02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Camera02
- MDM_Policy_Config01_Camera02.InstanceID
- MDM_Policy_Config01_Camera02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 377a9eb695560d7bf93fd6a5d761b1e95202bf20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740969"
---
# <a name="mdm_policy_config01_camera02-class"></a><span data-ttu-id="71d9c-105">MDM- \_ Richtlinie \_ Config01 \_ Camera02-Klasse</span><span class="sxs-lookup"><span data-stu-id="71d9c-105">MDM\_Policy\_Config01\_Camera02 class</span></span>

<span data-ttu-id="71d9c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="71d9c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="71d9c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="71d9c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="71d9c-108">Die **MDM- \_ Richtlinie \_ Config01 \_ Camera02** -Klasse stellt die verfügbaren Kamera Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="71d9c-108">The **MDM\_Policy\_Config01\_Camera02** class represents the camera policies available.</span></span>

<span data-ttu-id="71d9c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="71d9c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d9c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="71d9c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Camera02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCamera;
};
```

## <a name="members"></a><span data-ttu-id="71d9c-111">Member</span><span class="sxs-lookup"><span data-stu-id="71d9c-111">Members</span></span>

<span data-ttu-id="71d9c-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Camera02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="71d9c-112">The **MDM\_Policy\_Config01\_Camera02** class has these types of members:</span></span>

-   [<span data-ttu-id="71d9c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71d9c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71d9c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71d9c-114">Properties</span></span>

<span data-ttu-id="71d9c-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Camera02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="71d9c-115">The **MDM\_Policy\_Config01\_Camera02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="71d9c-116">AllowCamera</span><span class="sxs-lookup"><span data-stu-id="71d9c-116">AllowCamera</span></span>](/windows/client-management/mdm/policy-csp-camera#camera-allowcamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d9c-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d9c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d9c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="71d9c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="71d9c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="71d9c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d9c-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71d9c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d9c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71d9c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71d9c-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71d9c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71d9c-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="71d9c-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="71d9c-124">Für diese Klasse ist die Zeichenfolge "Kamera".</span><span class="sxs-lookup"><span data-stu-id="71d9c-124">For this class, the string is "Camera".</span></span>

</dd> <dt>

<span data-ttu-id="71d9c-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="71d9c-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d9c-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71d9c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d9c-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71d9c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71d9c-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71d9c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71d9c-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="71d9c-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="71d9c-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="71d9c-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71d9c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71d9c-131">Requirements</span></span>



| <span data-ttu-id="71d9c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71d9c-132">Requirement</span></span> | <span data-ttu-id="71d9c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="71d9c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d9c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71d9c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="71d9c-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71d9c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71d9c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71d9c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="71d9c-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="71d9c-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="71d9c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="71d9c-138">Namespace</span></span><br/>                | <span data-ttu-id="71d9c-139">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="71d9c-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="71d9c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="71d9c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71d9c-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="71d9c-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="71d9c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="71d9c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d9c-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d9c-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d9c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71d9c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d9c-145">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="71d9c-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

