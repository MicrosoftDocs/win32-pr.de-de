---
title: MDM_Policy_Result01_WindowsInkWorkspace02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ WindowsInkWorkspace02-Klasse stellt die verfügbaren frei Hand arbeitsbereichrichtlinien dar
ms.assetid: a3bb85e5-554f-4f41-8e65-e221f8adc947
keywords:
- MDM_Policy_Result01_WindowsInkWorkspace02-Klasse
- MDM_Policy_Result01_WindowsInkWorkspace02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsInkWorkspace02
- MDM_Policy_Result01_WindowsInkWorkspace02.InstanceID
- MDM_Policy_Result01_WindowsInkWorkspace02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d64100ec0566b7cd996840d012d018b8dbc75aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858672"
---
# <a name="mdm_policy_result01_windowsinkworkspace02-class"></a><span data-ttu-id="39204-105">MDM- \_ Richtlinie \_ Result01 \_ WindowsInkWorkspace02-Klasse</span><span class="sxs-lookup"><span data-stu-id="39204-105">MDM\_Policy\_Result01\_WindowsInkWorkspace02 class</span></span>

<span data-ttu-id="39204-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="39204-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="39204-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="39204-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="39204-108">Die [**MDM- \_ Richtlinie \_ Result01 \_ WindowsInkWorkspace02**](mdm-policy-config01-windowsinkworkspace02.md) -Klasse stellt die verfügbaren frei Hand arbeitsbereichrichtlinien dar</span><span class="sxs-lookup"><span data-stu-id="39204-108">The [**MDM\_Policy\_Result01\_WindowsInkWorkspace02**](mdm-policy-config01-windowsinkworkspace02.md) class represents the ink workspace policies available.</span></span>

<span data-ttu-id="39204-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="39204-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39204-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="39204-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsInkWorkspace02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsInkWorkspace;
  sint32 AllowSuggestedAppsInWindowsInkWorkspace;
};
```

## <a name="members"></a><span data-ttu-id="39204-111">Member</span><span class="sxs-lookup"><span data-stu-id="39204-111">Members</span></span>

<span data-ttu-id="39204-112">Die **MDM- \_ Richtlinie \_ Result01 \_ WindowsInkWorkspace02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="39204-112">The **MDM\_Policy\_Result01\_WindowsInkWorkspace02** class has these types of members:</span></span>

-   [<span data-ttu-id="39204-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39204-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39204-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39204-114">Properties</span></span>

<span data-ttu-id="39204-115">Die **MDM- \_ Richtlinie \_ Result01 \_ WindowsInkWorkspace02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="39204-115">The **MDM\_Policy\_Result01\_WindowsInkWorkspace02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="39204-116">Allowvorschlags stedappsinwindowsinkworkspace</span><span class="sxs-lookup"><span data-stu-id="39204-116">AllowSuggestedAppsInWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowsuggestedappsinwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39204-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39204-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39204-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="39204-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39204-119">Allowwindowsinkworkspace</span><span class="sxs-lookup"><span data-stu-id="39204-119">AllowWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39204-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39204-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39204-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="39204-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39204-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="39204-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39204-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39204-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39204-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39204-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39204-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39204-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="39204-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="39204-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="39204-127">Für diese Klasse ist die Zeichenfolge "windowsink Workspace".</span><span class="sxs-lookup"><span data-stu-id="39204-127">For this class, the string is "WindowsInkWorkspace".</span></span>

</dd> <dt>

<span data-ttu-id="39204-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="39204-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39204-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="39204-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39204-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="39204-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39204-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39204-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="39204-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="39204-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="39204-133">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="39204-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39204-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39204-134">Requirements</span></span>



| <span data-ttu-id="39204-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39204-135">Requirement</span></span> | <span data-ttu-id="39204-136">Wert</span><span class="sxs-lookup"><span data-stu-id="39204-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39204-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39204-137">Minimum supported client</span></span><br/> | <span data-ttu-id="39204-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39204-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="39204-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39204-139">Minimum supported server</span></span><br/> | <span data-ttu-id="39204-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="39204-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="39204-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="39204-141">Namespace</span></span><br/>                | <span data-ttu-id="39204-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="39204-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="39204-143">MOF</span><span class="sxs-lookup"><span data-stu-id="39204-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39204-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="39204-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="39204-145">DLL</span><span class="sxs-lookup"><span data-stu-id="39204-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39204-146"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="39204-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

