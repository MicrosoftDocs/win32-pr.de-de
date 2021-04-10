---
title: MDM_Policy_Config01_Browser02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Browser02-Klasse stellt die verfügbaren Browser Richtlinien dar.
ms.assetid: 296e3be4-3bc1-4e06-9e31-532639a0b912
keywords:
- MDM_Policy_Config01_Browser02-Klasse
- MDM_Policy_Config01_Browser02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Browser02
- MDM_Policy_Config01_Browser02.InstanceID
- MDM_Policy_Config01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba68b4d3f6798a448447e7773dc299977c54434c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040416"
---
# <a name="mdm_policy_config01_browser02-class"></a><span data-ttu-id="8b458-105">MDM- \_ Richtlinie \_ Config01 \_ Browser02-Klasse</span><span class="sxs-lookup"><span data-stu-id="8b458-105">MDM\_Policy\_Config01\_Browser02 class</span></span>

<span data-ttu-id="8b458-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8b458-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8b458-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8b458-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8b458-108">Die **MDM- \_ Richtlinie \_ Config01 \_ Browser02** -Klasse stellt die verfügbaren Browser Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="8b458-108">The **MDM\_Policy\_Config01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="8b458-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8b458-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b458-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b458-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Browser02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddressBarDropdown;
  sint32 AllowAutofill;
  sint32 AllowCookies;
  sint32 AllowDeveloperTools;
  sint32 AllowInPrivate;
  sint32 AllowMicrosoftCompatibilityList;
  sint32 AllowDoNotTrack;
  sint32 AllowFlashClickToRun;
  sint32 AllowFlash;
  sint32 AllowExtensions;
  sint32 AllowPasswordManager;
  sint32 AllowPopups;
  sint32 AllowSearchEngineCustomization;
  sint32 AllowSearchSuggestionsinAddressBar;
  sint32 AllowSmartScreen;
  sint32 AlwaysEnableBooksLibrary;
  sint32 DisableLockdownOfStartPages;
  string ConfigureAdditionalSearchEngines;
  sint32 ClearBrowsingDataOnExit;
  string EnterpriseModeSiteList;
  string EnterpriseSiteListServiceUrl;
  string Homepages;
  sint32 LockdownFavorites;
  sint32 PreventAccessToAboutFlagsInMicrosoftEdge;
  sint32 PreventLiveTileDataCollection;
  sint32 PreventFirstRunPage;
  sint32 PreventSmartScreenPromptOverride;
  sint32 PreventSmartScreenPromptOverrideForFiles;
  sint32 PreventUsingLocalHostIPAddressForWebRTC;
  string ProvisionFavorites;
  sint32 SendIntranetTraffictoInternetExplorer;
  string SetDefaultSearchEngine;
  sint32 ShowMessageWhenOpeningSitesInInternetExplorer;
  sint32 SyncFavoritesBetweenIEAndMicrosoftEdge;
};
```

## <a name="members"></a><span data-ttu-id="8b458-111">Member</span><span class="sxs-lookup"><span data-stu-id="8b458-111">Members</span></span>

<span data-ttu-id="8b458-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Browser02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b458-112">The **MDM\_Policy\_Config01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="8b458-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b458-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b458-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b458-114">Properties</span></span>

<span data-ttu-id="8b458-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Browser02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b458-115">The **MDM\_Policy\_Config01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8b458-116">Allowaddressbardropdown</span><span class="sxs-lookup"><span data-stu-id="8b458-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="8b458-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="8b458-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="8b458-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="8b458-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="8b458-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-134">Allowflash</span><span class="sxs-lookup"><span data-stu-id="8b458-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-137">Allowflash clicktor UN</span><span class="sxs-lookup"><span data-stu-id="8b458-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="8b458-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-143">Allowmicrosoftcompatibilitylist</span><span class="sxs-lookup"><span data-stu-id="8b458-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="8b458-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="8b458-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-152">Allowsearchenginecustomization</span><span class="sxs-lookup"><span data-stu-id="8b458-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="8b458-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="8b458-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-161">Alwaysenablebookslibrary</span><span class="sxs-lookup"><span data-stu-id="8b458-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-164">Clearbrowsingdataonexit</span><span class="sxs-lookup"><span data-stu-id="8b458-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-167">Konfigurieren von "Read ditionalsearchengines"</span><span class="sxs-lookup"><span data-stu-id="8b458-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-170">Disablelockdownoberstartpages</span><span class="sxs-lookup"><span data-stu-id="8b458-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="8b458-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-176">Enterprisisitelistserviceurl</span><span class="sxs-lookup"><span data-stu-id="8b458-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-179">Startseiten</span><span class="sxs-lookup"><span data-stu-id="8b458-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b458-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8b458-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b458-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b458-185">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b458-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8b458-186">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="8b458-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="8b458-187">Für diese Klasse ist die Zeichenfolge "Browser".</span><span class="sxs-lookup"><span data-stu-id="8b458-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="8b458-188">Lockdownfavoriten</span><span class="sxs-lookup"><span data-stu-id="8b458-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-189">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b458-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8b458-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b458-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b458-194">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8b458-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8b458-195">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="8b458-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="8b458-196">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="8b458-196">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="8b458-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="8b458-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-198">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-200">Preventfirstrauunpage</span><span class="sxs-lookup"><span data-stu-id="8b458-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-201">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-203">Preventlivetiledatacollection</span><span class="sxs-lookup"><span data-stu-id="8b458-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-204">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="8b458-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="8b458-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-210">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-212">Preventusinglocalhostipaddressforwebrtc</span><span class="sxs-lookup"><span data-stu-id="8b458-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-213">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-215">Provisionfavoriten</span><span class="sxs-lookup"><span data-stu-id="8b458-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="8b458-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-219">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-221">Setdefaultsearchengine</span><span class="sxs-lookup"><span data-stu-id="8b458-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b458-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-224">Showmessageeingangs openingsitesininternetexplorer</span><span class="sxs-lookup"><span data-stu-id="8b458-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-225">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8b458-227">Syncfavoritesbetweenieandmikrosoftedge</span><span class="sxs-lookup"><span data-stu-id="8b458-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b458-228">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8b458-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b458-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8b458-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b458-230">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b458-230">Requirements</span></span>



| <span data-ttu-id="8b458-231">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b458-231">Requirement</span></span> | <span data-ttu-id="8b458-232">Wert</span><span class="sxs-lookup"><span data-stu-id="8b458-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b458-233">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b458-233">Minimum supported client</span></span><br/> | <span data-ttu-id="8b458-234">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b458-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b458-235">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b458-235">Minimum supported server</span></span><br/> | <span data-ttu-id="8b458-236">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8b458-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8b458-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b458-237">Namespace</span></span><br/>                | <span data-ttu-id="8b458-238">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8b458-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8b458-239">MOF</span><span class="sxs-lookup"><span data-stu-id="8b458-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b458-240"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b458-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b458-241">DLL</span><span class="sxs-lookup"><span data-stu-id="8b458-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b458-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b458-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b458-243">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b458-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b458-244">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="8b458-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

