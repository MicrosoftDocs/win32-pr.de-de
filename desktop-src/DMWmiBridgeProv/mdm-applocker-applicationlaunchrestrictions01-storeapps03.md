---
title: MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03-Klasse
description: Mit der MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03-Klasse können Sie angeben, welche exe-Anwendungen für den Unternehmens Datenschutz zulässig oder nicht zulässig sind.
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03-Klasse
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342204"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a><span data-ttu-id="2f517-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03-Klasse</span><span class="sxs-lookup"><span data-stu-id="2f517-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03 class</span></span>

<span data-ttu-id="2f517-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2f517-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2f517-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2f517-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2f517-108">Mit der **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** -Klasse können Sie angeben, welche exe-Anwendungen für den Unternehmens Datenschutz zulässig oder nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2f517-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class allows you to specify which EXE applications are allowed or disallowed for Enterprise Data Protection.</span></span>

<span data-ttu-id="2f517-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2f517-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f517-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f517-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="2f517-111">Member</span><span class="sxs-lookup"><span data-stu-id="2f517-111">Members</span></span>

<span data-ttu-id="2f517-112">Die **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2f517-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="2f517-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f517-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f517-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f517-114">Properties</span></span>

<span data-ttu-id="2f517-115">Die **MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f517-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2f517-116">**Enforcementmode**</span><span class="sxs-lookup"><span data-stu-id="2f517-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f517-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f517-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f517-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2f517-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2f517-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f517-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f517-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f517-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f517-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f517-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f517-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f517-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f517-123">Legt Beschränkungen zum Ausführen von Apps vom Windows Store fest.</span><span class="sxs-lookup"><span data-stu-id="2f517-123">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="2f517-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2f517-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f517-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f517-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f517-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f517-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f517-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f517-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f517-128">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2f517-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="2f517-129">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Gruppierung*".</span><span class="sxs-lookup"><span data-stu-id="2f517-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="2f517-130">**Policy**</span><span class="sxs-lookup"><span data-stu-id="2f517-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f517-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2f517-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f517-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2f517-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f517-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f517-133">Requirements</span></span>



| <span data-ttu-id="2f517-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f517-134">Requirement</span></span> | <span data-ttu-id="2f517-135">Wert</span><span class="sxs-lookup"><span data-stu-id="2f517-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f517-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f517-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f517-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f517-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f517-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f517-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f517-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2f517-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2f517-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f517-140">Namespace</span></span><br/>                | <span data-ttu-id="2f517-141">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2f517-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="2f517-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2f517-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f517-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f517-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f517-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2f517-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f517-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f517-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f517-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f517-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f517-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="2f517-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

