---
title: MDM_Policy_Result01_Camera02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Camera02-Klasse stellt die verfügbaren Kamera Richtlinien dar.
ms.assetid: 72b11a00-6a34-4939-b1d0-e457b0c80c7f
keywords:
- MDM_Policy_Result01_Camera02-Klasse
- MDM_Policy_Result01_Camera02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Camera02
- MDM_Policy_Result01_Camera02.InstanceID
- MDM_Policy_Result01_Camera02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9a266e93740cda5afbbc9a8195907a2a40cff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475723"
---
# <a name="mdm_policy_result01_camera02-class"></a><span data-ttu-id="9dbe6-105">MDM- \_ Richtlinie \_ Result01 \_ Camera02-Klasse</span><span class="sxs-lookup"><span data-stu-id="9dbe6-105">MDM\_Policy\_Result01\_Camera02 class</span></span>

<span data-ttu-id="9dbe6-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9dbe6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9dbe6-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="9dbe6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9dbe6-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Camera02** -Klasse stellt die verfügbaren Kamera Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="9dbe6-108">The **MDM\_Policy\_Result01\_Camera02** class represents the camera policies available.</span></span>

<span data-ttu-id="9dbe6-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9dbe6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dbe6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dbe6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Camera02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCamera;
};
```

## <a name="members"></a><span data-ttu-id="9dbe6-111">Member</span><span class="sxs-lookup"><span data-stu-id="9dbe6-111">Members</span></span>

<span data-ttu-id="9dbe6-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Camera02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9dbe6-112">The **MDM\_Policy\_Result01\_Camera02** class has these types of members:</span></span>

-   [<span data-ttu-id="9dbe6-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dbe6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9dbe6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dbe6-114">Properties</span></span>

<span data-ttu-id="9dbe6-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Camera02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9dbe6-115">The **MDM\_Policy\_Result01\_Camera02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9dbe6-116">AllowCamera</span><span class="sxs-lookup"><span data-stu-id="9dbe6-116">AllowCamera</span></span>](/windows/client-management/mdm/policy-csp-camera#camera-allowcamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbe6-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9dbe6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9dbe6-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9dbe6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9dbe6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9dbe6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbe6-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbe6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbe6-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbe6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbe6-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9dbe6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9dbe6-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="9dbe6-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="9dbe6-124">Für diese Klasse ist die Zeichenfolge "Kamera".</span><span class="sxs-lookup"><span data-stu-id="9dbe6-124">For this class, the string is "Camera".</span></span>

</dd> <dt>

<span data-ttu-id="9dbe6-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9dbe6-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dbe6-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9dbe6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dbe6-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dbe6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dbe6-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9dbe6-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9dbe6-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="9dbe6-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="9dbe6-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="9dbe6-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9dbe6-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dbe6-131">Requirements</span></span>



| <span data-ttu-id="9dbe6-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dbe6-132">Requirement</span></span> | <span data-ttu-id="9dbe6-133">Wert</span><span class="sxs-lookup"><span data-stu-id="9dbe6-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dbe6-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dbe6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9dbe6-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dbe6-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9dbe6-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dbe6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9dbe6-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9dbe6-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9dbe6-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="9dbe6-138">Namespace</span></span><br/>                | <span data-ttu-id="9dbe6-139">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9dbe6-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9dbe6-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9dbe6-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dbe6-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9dbe6-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9dbe6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9dbe6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dbe6-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dbe6-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dbe6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dbe6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dbe6-145">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="9dbe6-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

