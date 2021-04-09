---
title: MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03-Klasse
description: Mit der MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03-Klasse können Sie angeben, welche exe-Anwendungen gestartet werden dürfen.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03-Klasse
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858818"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a><span data-ttu-id="fefd7-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03-Klasse</span><span class="sxs-lookup"><span data-stu-id="fefd7-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03 class</span></span>

<span data-ttu-id="fefd7-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="fefd7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fefd7-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="fefd7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fefd7-108">Mit der **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** -Klasse können Sie angeben, welche exe-Anwendungen gestartet werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="fefd7-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class allows you to specify which EXE applications are allowed to launch.</span></span>

<span data-ttu-id="fefd7-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fefd7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fefd7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fefd7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="fefd7-111">Member</span><span class="sxs-lookup"><span data-stu-id="fefd7-111">Members</span></span>

<span data-ttu-id="fefd7-112">Die **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fefd7-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="fefd7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fefd7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fefd7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fefd7-114">Properties</span></span>

<span data-ttu-id="fefd7-115">Die **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fefd7-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fefd7-116">**Enforcementmode**</span><span class="sxs-lookup"><span data-stu-id="fefd7-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fefd7-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fefd7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fefd7-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fefd7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fefd7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fefd7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fefd7-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fefd7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fefd7-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fefd7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fefd7-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fefd7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fefd7-123">Definiert Einschränkungen für das Starten ausführbarer Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="fefd7-123">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

[<span data-ttu-id="fefd7-124">**Noninteractiveprocessenforcement**</span><span class="sxs-lookup"><span data-stu-id="fefd7-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fefd7-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fefd7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fefd7-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fefd7-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fefd7-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fefd7-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fefd7-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fefd7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fefd7-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fefd7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fefd7-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fefd7-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fefd7-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="fefd7-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="fefd7-132">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Gruppierung*".</span><span class="sxs-lookup"><span data-stu-id="fefd7-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="fefd7-133">**Policy**</span><span class="sxs-lookup"><span data-stu-id="fefd7-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fefd7-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fefd7-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fefd7-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fefd7-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fefd7-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fefd7-136">Requirements</span></span>



| <span data-ttu-id="fefd7-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fefd7-137">Requirement</span></span> | <span data-ttu-id="fefd7-138">Wert</span><span class="sxs-lookup"><span data-stu-id="fefd7-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fefd7-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fefd7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fefd7-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fefd7-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fefd7-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fefd7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fefd7-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fefd7-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fefd7-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="fefd7-143">Namespace</span></span><br/>                | <span data-ttu-id="fefd7-144">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fefd7-144">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fefd7-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fefd7-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fefd7-146"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fefd7-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fefd7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fefd7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fefd7-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fefd7-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fefd7-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fefd7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fefd7-150">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="fefd7-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

