---
title: MDM_Policy_Result01_Search02-Klasse
description: Die Result01 Search02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Such Richtlinien dar.
ms.assetid: 3025753f-a3cc-430c-bc73-438085ef5c51
keywords:
- MDM_Policy_Result01_Search02-Klasse
- MDM_Policy_Result01_Search02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Search02
- MDM_Policy_Result01_Search02.InstanceID
- MDM_Policy_Result01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a0e25e7f5aa47abcc2b39d9a30a764c5dc9c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040306"
---
# <a name="mdm_policy_result01_search02-class"></a><span data-ttu-id="ac1d9-105">MDM- \_ Richtlinie \_ Result01 \_ Search02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ac1d9-105">MDM\_Policy\_Result01\_Search02 class</span></span>

<span data-ttu-id="ac1d9-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac1d9-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ac1d9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac1d9-108">Die **\_ \_ Result01 \_ Search02-Klasse der MDM-Richtlinie** stellt die verfügbaren Such Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-108">The **MDM\_Policy\_Result01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="ac1d9-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1d9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac1d9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Search02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCloudSearch;
  sint32 AllowSearchToUseLocation;
  sint32 AllowStoringImagesFromVisionSearch;
  sint32 AlwaysUseAutoLangDetection;
  sint32 PreventRemoteQueries;
  sint32 PreventIndexingLowDiskSpaceMB;
  sint32 DisableRemovableDriveIndexing;
  sint32 DisableBackoff;
  sint32 AllowUsingDiacritics;
  sint32 AllowWindowsIndexer;
  sint32 AllowIndexingEncryptedStoresOrItems;
};
```

## <a name="members"></a><span data-ttu-id="ac1d9-111">Member</span><span class="sxs-lookup"><span data-stu-id="ac1d9-111">Members</span></span>

<span data-ttu-id="ac1d9-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Search02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ac1d9-112">The **MDM\_Policy\_Result01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac1d9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac1d9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac1d9-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac1d9-114">Properties</span></span>

<span data-ttu-id="ac1d9-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Search02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-115">The **MDM\_Policy\_Result01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac1d9-116">Allowcloudsearch</span><span class="sxs-lookup"><span data-stu-id="ac1d9-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-119">' Zubei ' zuder Zuweisung</span><span class="sxs-lookup"><span data-stu-id="ac1d9-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-122">Allowsearchtouselokation</span><span class="sxs-lookup"><span data-stu-id="ac1d9-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-125">Allowstoringimagesfromvisionsearch</span><span class="sxs-lookup"><span data-stu-id="ac1d9-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-128">"Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="ac1d9-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-131">Allowwindowsindexer</span><span class="sxs-lookup"><span data-stu-id="ac1d9-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-134">Alwaysusegautolangerkennung</span><span class="sxs-lookup"><span data-stu-id="ac1d9-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-137">Disablebackoff</span><span class="sxs-lookup"><span data-stu-id="ac1d9-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-140">Disableremovabledriveingedexing</span><span class="sxs-lookup"><span data-stu-id="ac1d9-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac1d9-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac1d9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-146">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac1d9-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac1d9-147">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="ac1d9-148">Für diese Klasse ist die Zeichenfolge "Search".</span><span class="sxs-lookup"><span data-stu-id="ac1d9-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="ac1d9-149">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac1d9-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac1d9-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac1d9-153">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="ac1d9-154">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="ac1d9-154">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="ac1d9-155">Preventindexinglowdiskspacemb</span><span class="sxs-lookup"><span data-stu-id="ac1d9-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac1d9-158">Preventremotequeries</span><span class="sxs-lookup"><span data-stu-id="ac1d9-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac1d9-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac1d9-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac1d9-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ac1d9-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac1d9-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac1d9-161">Requirements</span></span>



| <span data-ttu-id="ac1d9-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac1d9-162">Requirement</span></span> | <span data-ttu-id="ac1d9-163">Wert</span><span class="sxs-lookup"><span data-stu-id="ac1d9-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1d9-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac1d9-164">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1d9-165">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac1d9-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac1d9-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac1d9-166">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1d9-167">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ac1d9-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ac1d9-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac1d9-168">Namespace</span></span><br/>                | <span data-ttu-id="ac1d9-169">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ac1d9-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ac1d9-170">MOF</span><span class="sxs-lookup"><span data-stu-id="ac1d9-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac1d9-171"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d9-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac1d9-172">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1d9-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1d9-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d9-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac1d9-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac1d9-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1d9-175">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="ac1d9-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

