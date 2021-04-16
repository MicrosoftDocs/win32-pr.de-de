---
title: MDM_Policy_User_Config01_Experience02-Klasse
description: Die Benutzer Config01 Experience02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Erfahrungs Richtlinien dar.
ms.assetid: 61a5f093-812a-4fcb-940d-d5f0de7f8c5f
keywords:
- MDM_Policy_User_Config01_Experience02-Klasse
- MDM_Policy_User_Config01_Experience02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Experience02
- MDM_Policy_User_Config01_Experience02.InstanceID
- MDM_Policy_User_Config01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a982728a3b2f2a899cdbdbd6239a29c5310a258e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477844"
---
# <a name="mdm_policy_user_config01_experience02-class"></a><span data-ttu-id="a7f04-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ Experience02-Klasse</span><span class="sxs-lookup"><span data-stu-id="a7f04-105">MDM\_Policy\_User\_Config01\_Experience02 class</span></span>

<span data-ttu-id="a7f04-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a7f04-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a7f04-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="a7f04-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a7f04-108">Die **\_ \_ Benutzer \_ Config01 \_ Experience02-Klasse der MDM-Richtlinie** stellt die verfügbaren Erfahrungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="a7f04-108">The **MDM\_Policy\_User\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="a7f04-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a7f04-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f04-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f04-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a><span data-ttu-id="a7f04-111">Member</span><span class="sxs-lookup"><span data-stu-id="a7f04-111">Members</span></span>

<span data-ttu-id="a7f04-112">Die **\_ \_ Benutzer \_ Config01 \_ Experience02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a7f04-112">The **MDM\_Policy\_User\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="a7f04-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7f04-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7f04-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7f04-114">Properties</span></span>

<span data-ttu-id="a7f04-115">Die **\_ \_ Benutzer \_ Config01 \_ Experience02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a7f04-115">The **MDM\_Policy\_User\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a7f04-116">Allowtailoredexperienceswithdiagnosticdata</span><span class="sxs-lookup"><span data-stu-id="a7f04-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7f04-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a7f04-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7f04-119">Allowthirdpartysuggestionsinwindowsspotlight</span><span class="sxs-lookup"><span data-stu-id="a7f04-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7f04-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a7f04-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7f04-122">Allowwindowsconsumerfeatures</span><span class="sxs-lookup"><span data-stu-id="a7f04-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7f04-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a7f04-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7f04-125">Allowwindowsspotlight</span><span class="sxs-lookup"><span data-stu-id="a7f04-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7f04-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a7f04-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7f04-128">Allowwindowsspotlightonaktioncenter</span><span class="sxs-lookup"><span data-stu-id="a7f04-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7f04-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a7f04-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7f04-131">Allowwindowsspotlightwindowswelcomeerlebnis</span><span class="sxs-lookup"><span data-stu-id="a7f04-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7f04-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a7f04-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7f04-134">Konfigurieren von "Konfigurieren von rewindowsspotlightonlockscreen"</span><span class="sxs-lookup"><span data-stu-id="a7f04-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7f04-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a7f04-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7f04-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7f04-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a7f04-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a7f04-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7f04-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7f04-141">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="a7f04-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="a7f04-142">Für diese Klasse ist die Zeichenfolge "erleben".</span><span class="sxs-lookup"><span data-stu-id="a7f04-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="a7f04-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a7f04-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f04-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a7f04-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a7f04-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7f04-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7f04-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7f04-147">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="a7f04-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="a7f04-148">Für diese Klasse ist die Zeichenfolge "./User/Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="a7f04-148">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7f04-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7f04-149">Requirements</span></span>



| <span data-ttu-id="a7f04-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7f04-150">Requirement</span></span> | <span data-ttu-id="a7f04-151">Wert</span><span class="sxs-lookup"><span data-stu-id="a7f04-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f04-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7f04-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f04-153">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7f04-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a7f04-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7f04-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f04-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a7f04-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a7f04-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7f04-156">Namespace</span></span><br/>                | <span data-ttu-id="a7f04-157">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a7f04-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a7f04-158">MOF</span><span class="sxs-lookup"><span data-stu-id="a7f04-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7f04-159"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a7f04-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="a7f04-160">DLL</span><span class="sxs-lookup"><span data-stu-id="a7f04-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7f04-161"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="a7f04-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

