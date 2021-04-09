---
title: MDM_Policy_Result01_Browser02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Browser02-Klasse stellt die verfügbaren Browser Richtlinien dar. MDM- \_ Richtlinie \_ Result01 \_ Browser02-Klasse stellt die verfügbaren Browser Richtlinien dar.
ms.assetid: 06dc9f68-d9ea-4eec-93cb-1f26e8a6050d
keywords:
- MDM_Policy_Result01_Browser02-Klasse
- MDM_Policy_Result01_Browser02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02.InstanceID
- MDM_Policy_Result01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d132c43b88b242864e248b705a0f6bca02e546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858674"
---
# <a name="mdm_policy_result01_browser02-class"></a><span data-ttu-id="59a5e-105">MDM- \_ Richtlinie \_ Result01 \_ Browser02-Klasse</span><span class="sxs-lookup"><span data-stu-id="59a5e-105">MDM\_Policy\_Result01\_Browser02 class</span></span>

<span data-ttu-id="59a5e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="59a5e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="59a5e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="59a5e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="59a5e-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Browser02** -Klasse stellt die verfügbaren Browser Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="59a5e-108">The **MDM\_Policy\_Result01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="59a5e-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="59a5e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a5e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="59a5e-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Browser02
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

## <a name="members"></a><span data-ttu-id="59a5e-111">Member</span><span class="sxs-lookup"><span data-stu-id="59a5e-111">Members</span></span>

<span data-ttu-id="59a5e-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Browser02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="59a5e-112">The **MDM\_Policy\_Result01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="59a5e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59a5e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59a5e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59a5e-114">Properties</span></span>

<span data-ttu-id="59a5e-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Browser02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="59a5e-115">The **MDM\_Policy\_Result01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="59a5e-116">Allowaddressbardropdown</span><span class="sxs-lookup"><span data-stu-id="59a5e-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="59a5e-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="59a5e-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="59a5e-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="59a5e-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="59a5e-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-134">Allowflash</span><span class="sxs-lookup"><span data-stu-id="59a5e-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-137">Allowflash clicktor UN</span><span class="sxs-lookup"><span data-stu-id="59a5e-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="59a5e-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-143">Allowmicrosoftcompatibilitylist</span><span class="sxs-lookup"><span data-stu-id="59a5e-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="59a5e-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="59a5e-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-152">Allowsearchenginecustomization</span><span class="sxs-lookup"><span data-stu-id="59a5e-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-153">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="59a5e-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-156">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="59a5e-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-161">Alwaysenablebookslibrary</span><span class="sxs-lookup"><span data-stu-id="59a5e-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-162">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-164">Clearbrowsingdataonexit</span><span class="sxs-lookup"><span data-stu-id="59a5e-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-167">Konfigurieren von "Read ditionalsearchengines"</span><span class="sxs-lookup"><span data-stu-id="59a5e-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-170">Disablelockdownoberstartpages</span><span class="sxs-lookup"><span data-stu-id="59a5e-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="59a5e-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-176">Enterprisisitelistserviceurl</span><span class="sxs-lookup"><span data-stu-id="59a5e-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-179">Startseiten</span><span class="sxs-lookup"><span data-stu-id="59a5e-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59a5e-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="59a5e-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="59a5e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-185">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59a5e-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="59a5e-186">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="59a5e-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="59a5e-187">Für diese Klasse ist die Zeichenfolge "Browser".</span><span class="sxs-lookup"><span data-stu-id="59a5e-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="59a5e-188">Lockdownfavoriten</span><span class="sxs-lookup"><span data-stu-id="59a5e-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-189">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59a5e-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="59a5e-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="59a5e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-194">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59a5e-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="59a5e-195">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="59a5e-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="59a5e-196">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="59a5e-196">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="59a5e-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="59a5e-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-198">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-200">Preventfirstrauunpage</span><span class="sxs-lookup"><span data-stu-id="59a5e-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-201">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-203">Preventlivetiledatacollection</span><span class="sxs-lookup"><span data-stu-id="59a5e-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-204">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="59a5e-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="59a5e-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-210">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-212">Preventusinglocalhostipaddressforwebrtc</span><span class="sxs-lookup"><span data-stu-id="59a5e-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-213">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-215">Provisionfavoriten</span><span class="sxs-lookup"><span data-stu-id="59a5e-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="59a5e-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-219">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-221">Setdefaultsearchengine</span><span class="sxs-lookup"><span data-stu-id="59a5e-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59a5e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-224">Showmessageeingangs openingsitesininternetexplorer</span><span class="sxs-lookup"><span data-stu-id="59a5e-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-225">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="59a5e-227">Syncfavoritesbetweenieandmikrosoftedge</span><span class="sxs-lookup"><span data-stu-id="59a5e-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59a5e-228">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="59a5e-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="59a5e-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59a5e-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59a5e-230">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59a5e-230">Requirements</span></span>



| <span data-ttu-id="59a5e-231">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59a5e-231">Requirement</span></span> | <span data-ttu-id="59a5e-232">Wert</span><span class="sxs-lookup"><span data-stu-id="59a5e-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a5e-233">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59a5e-233">Minimum supported client</span></span><br/> | <span data-ttu-id="59a5e-234">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59a5e-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59a5e-235">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59a5e-235">Minimum supported server</span></span><br/> | <span data-ttu-id="59a5e-236">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="59a5e-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="59a5e-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="59a5e-237">Namespace</span></span><br/>                | <span data-ttu-id="59a5e-238">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="59a5e-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="59a5e-239">MOF</span><span class="sxs-lookup"><span data-stu-id="59a5e-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59a5e-240"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="59a5e-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="59a5e-241">DLL</span><span class="sxs-lookup"><span data-stu-id="59a5e-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59a5e-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59a5e-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59a5e-243">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59a5e-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a5e-244">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="59a5e-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

