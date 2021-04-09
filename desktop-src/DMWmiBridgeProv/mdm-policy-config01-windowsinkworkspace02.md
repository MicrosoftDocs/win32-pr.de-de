---
title: MDM_Policy_Config01_WindowsInkWorkspace02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ WindowsInkWorkspace02-Klasse stellt die verfügbaren frei Hand arbeitsbereichrichtlinien dar
ms.assetid: 676a459f-25b0-4cf7-bf64-635ac4a93f59
keywords:
- MDM_Policy_Config01_WindowsInkWorkspace02-Klasse
- MDM_Policy_Config01_WindowsInkWorkspace02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsInkWorkspace02
- MDM_Policy_Config01_WindowsInkWorkspace02.InstanceID
- MDM_Policy_Config01_WindowsInkWorkspace02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f654326b0a44ed40faa06dfe80d933dc2c52c4f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956531"
---
# <a name="mdm_policy_config01_windowsinkworkspace02-class"></a><span data-ttu-id="2e4cd-105">MDM- \_ Richtlinie \_ Config01 \_ WindowsInkWorkspace02-Klasse</span><span class="sxs-lookup"><span data-stu-id="2e4cd-105">MDM\_Policy\_Config01\_WindowsInkWorkspace02 class</span></span>

<span data-ttu-id="2e4cd-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2e4cd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2e4cd-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2e4cd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2e4cd-108">Die **MDM- \_ Richtlinie \_ Config01 \_ WindowsInkWorkspace02** -Klasse stellt die verfügbaren frei Hand arbeitsbereichrichtlinien dar</span><span class="sxs-lookup"><span data-stu-id="2e4cd-108">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class represents the ink workspace policies available.</span></span>

<span data-ttu-id="2e4cd-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2e4cd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4cd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e4cd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsInkWorkspace02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsInkWorkspace;
  sint32 AllowSuggestedAppsInWindowsInkWorkspace;
};
```

## <a name="members"></a><span data-ttu-id="2e4cd-111">Member</span><span class="sxs-lookup"><span data-stu-id="2e4cd-111">Members</span></span>

<span data-ttu-id="2e4cd-112">Die **MDM- \_ Richtlinie \_ Config01 \_ WindowsInkWorkspace02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2e4cd-112">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these types of members:</span></span>

-   [<span data-ttu-id="2e4cd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e4cd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e4cd-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e4cd-114">Properties</span></span>

<span data-ttu-id="2e4cd-115">Die **MDM- \_ Richtlinie \_ Config01 \_ WindowsInkWorkspace02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e4cd-115">The **MDM\_Policy\_Config01\_WindowsInkWorkspace02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2e4cd-116">Allowvorschlags stedappsinwindowsinkworkspace</span><span class="sxs-lookup"><span data-stu-id="2e4cd-116">AllowSuggestedAppsInWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowsuggestedappsinwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4cd-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e4cd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e4cd-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e4cd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e4cd-119">Allowwindowsinkworkspace</span><span class="sxs-lookup"><span data-stu-id="2e4cd-119">AllowWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4cd-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e4cd-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e4cd-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2e4cd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e4cd-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2e4cd-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4cd-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e4cd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e4cd-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e4cd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e4cd-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e4cd-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e4cd-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2e4cd-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="2e4cd-127">Für diese Klasse ist die Zeichenfolge "windowsink Workspace".</span><span class="sxs-lookup"><span data-stu-id="2e4cd-127">For this class, the string is "WindowsInkWorkspace".</span></span>

</dd> <dt>

<span data-ttu-id="2e4cd-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2e4cd-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4cd-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e4cd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e4cd-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e4cd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e4cd-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e4cd-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e4cd-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2e4cd-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="2e4cd-133">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="2e4cd-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e4cd-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e4cd-134">Requirements</span></span>



| <span data-ttu-id="2e4cd-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e4cd-135">Requirement</span></span> | <span data-ttu-id="2e4cd-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2e4cd-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4cd-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e4cd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4cd-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e4cd-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2e4cd-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e4cd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4cd-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2e4cd-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2e4cd-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e4cd-141">Namespace</span></span><br/>                | <span data-ttu-id="2e4cd-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2e4cd-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="2e4cd-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2e4cd-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e4cd-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e4cd-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="2e4cd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2e4cd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e4cd-146"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="2e4cd-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

