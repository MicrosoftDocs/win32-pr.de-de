---
title: MDM_Policy_User_Config01_Start02-Klasse
description: Die Benutzer Config01 Start02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Start Richtlinien dar, die pro Benutzer festgelegt werden.
ms.assetid: bbb64553-4d93-433d-96e4-bfd3f5588138
keywords:
- MDM_Policy_User_Config01_Start02-Klasse
- MDM_Policy_User_Config01_Start02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02.InstanceID
- MDM_Policy_User_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b98b25ee0c3118f741d3a52bc9001c6106d86f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391944"
---
# <a name="mdm_policy_user_config01_start02-class"></a><span data-ttu-id="0decb-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ Start02-Klasse</span><span class="sxs-lookup"><span data-stu-id="0decb-105">MDM\_Policy\_User\_Config01\_Start02 class</span></span>

<span data-ttu-id="0decb-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0decb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0decb-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0decb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0decb-108">Die **\_ \_ Benutzer \_ Config01 \_ Start02-Klasse der MDM-Richtlinie** stellt die verfügbaren Start Richtlinien dar, die pro Benutzer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0decb-108">The **MDM\_Policy\_User\_Config01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="0decb-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0decb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0decb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0decb-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="0decb-111">Member</span><span class="sxs-lookup"><span data-stu-id="0decb-111">Members</span></span>

<span data-ttu-id="0decb-112">Die **\_ \_ Benutzer \_ Config01 \_ Start02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0decb-112">The **MDM\_Policy\_User\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="0decb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0decb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0decb-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0decb-114">Properties</span></span>

<span data-ttu-id="0decb-115">Die **\_ \_ Benutzer \_ Config01 \_ Start02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0decb-115">The **MDM\_Policy\_User\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0decb-116">Hidepeoplebar</span><span class="sxs-lookup"><span data-stu-id="0decb-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decb-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0decb-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0decb-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0decb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0decb-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0decb-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decb-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0decb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decb-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0decb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0decb-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0decb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0decb-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="0decb-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="0decb-124">Für diese Klasse ist die Zeichenfolge "Start".</span><span class="sxs-lookup"><span data-stu-id="0decb-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="0decb-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0decb-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decb-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0decb-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decb-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0decb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0decb-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0decb-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0decb-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="0decb-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="0decb-130">Für diese Klasse ist die Zeichenfolge "./User/Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="0decb-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="0decb-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="0decb-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decb-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0decb-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decb-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0decb-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0decb-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0decb-134">Requirements</span></span>



| <span data-ttu-id="0decb-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0decb-135">Requirement</span></span> | <span data-ttu-id="0decb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0decb-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0decb-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0decb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0decb-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0decb-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0decb-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0decb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0decb-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0decb-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0decb-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="0decb-141">Namespace</span></span><br/>                | <span data-ttu-id="0decb-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0decb-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0decb-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0decb-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0decb-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0decb-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0decb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0decb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0decb-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0decb-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0decb-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0decb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0decb-148">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="0decb-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

