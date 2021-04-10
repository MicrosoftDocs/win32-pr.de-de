---
title: MDM_Policy_User_Config01_InternetExplorer02-Klasse
description: Die MDM- \_ Richtlinie \_ User \_ Config01 \_ InternetExplorer02-Klasse stellt die verfügbaren Internet Explorer-Richtlinien dar.
ms.assetid: 2b155e65-5a81-4916-815f-23763759bb9a
keywords:
- MDM_Policy_User_Config01_InternetExplorer02-Klasse
- MDM_Policy_User_Config01_InternetExplorer02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02.InstanceID
- MDM_Policy_User_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f79c00505037508307e93120f9e2545b135678
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040656"
---
# <a name="mdm_policy_user_config01_internetexplorer02-class"></a><span data-ttu-id="05e03-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ InternetExplorer02-Klasse</span><span class="sxs-lookup"><span data-stu-id="05e03-105">MDM\_Policy\_User\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="05e03-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="05e03-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="05e03-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="05e03-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="05e03-108">Die MDM- \_ Richtlinie \_ User \_ Config01 \_ InternetExplorer02-Klasse stellt die verfügbaren Internet Explorer-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="05e03-108">The MDM\_Policy\_User\_Config01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="05e03-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="05e03-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e03-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="05e03-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="05e03-111">Member</span><span class="sxs-lookup"><span data-stu-id="05e03-111">Members</span></span>

<span data-ttu-id="05e03-112">Die **\_ \_ Benutzer \_ Config01 \_ InternetExplorer02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="05e03-112">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="05e03-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05e03-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05e03-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05e03-114">Properties</span></span>

<span data-ttu-id="05e03-115">Die **\_ \_ Benutzer \_ Config01 \_ InternetExplorer02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05e03-115">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="05e03-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="05e03-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-119">Allowactivexfiltering</span><span class="sxs-lookup"><span data-stu-id="05e03-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-122">Allowaddonlist</span><span class="sxs-lookup"><span data-stu-id="05e03-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-125">Allowautocomplete</span><span class="sxs-lookup"><span data-stu-id="05e03-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-128">Allowcertificateaddressmismatchwarning</span><span class="sxs-lookup"><span data-stu-id="05e03-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-131">Allowdelta etingbrowsinghistoryonexit</span><span class="sxs-lookup"><span data-stu-id="05e03-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-134">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="05e03-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-137">"Zuweisung von" "" "".</span><span class="sxs-lookup"><span data-stu-id="05e03-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-140">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="05e03-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="05e03-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-146">"Expwinternetexplorerstandardsmode"</span><span class="sxs-lookup"><span data-stu-id="05e03-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-149">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="05e03-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-152">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="05e03-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-155">Allowlocalmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-158">Allowlockeddowninternetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-161">Allowlockeddownintranetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-164">Allowlockeddownloader calmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-167">Allowlockeddownrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-170">' Zugwonewordentry '</span><span class="sxs-lookup"><span data-stu-id="05e03-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-173">Allowsiteononezuzuzustandliste</span><span class="sxs-lookup"><span data-stu-id="05e03-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-176">Allowslockeddowntreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-179">Allowsoftware\signatureisinvalid</span><span class="sxs-lookup"><span data-stu-id="05e03-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-182">Allowsrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-185">Allowvorschlags stedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-188">Allowtreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="05e03-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-191">Checkservercertificaterevozierung</span><span class="sxs-lookup"><span data-stu-id="05e03-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-194">Checksignaturesondownloader-dprogramme</span><span class="sxs-lookup"><span data-stu-id="05e03-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-196">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-197">"Konsistentmimehandlinginternetexplorerprocesses"</span><span class="sxs-lookup"><span data-stu-id="05e03-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-200">Disableadobeflash</span><span class="sxs-lookup"><span data-stu-id="05e03-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-203">Disableblockingof outdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-206">Disablebypassofsmartscreenwarning</span><span class="sxs-lookup"><span data-stu-id="05e03-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-209">Disablebypassofsmartscreenwarningsaboutuncommonfiles</span><span class="sxs-lookup"><span data-stu-id="05e03-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-212">Disableconfiguringhistory</span><span class="sxs-lookup"><span data-stu-id="05e03-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-215">Disablecrash-Erkennung</span><span class="sxs-lookup"><span data-stu-id="05e03-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-218">Disablecustomerexperiendceimprovementprogramparticipation</span><span class="sxs-lookup"><span data-stu-id="05e03-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-221">Disabledelta etinguservisitedwebsites</span><span class="sxs-lookup"><span data-stu-id="05e03-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-224">Disablereclosuredownload</span><span class="sxs-lookup"><span data-stu-id="05e03-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-227">Disableverschlüsseltionsupport</span><span class="sxs-lookup"><span data-stu-id="05e03-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="05e03-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-233">Disableflipheadfeature</span><span class="sxs-lookup"><span data-stu-id="05e03-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-236">Disablehomepagechange</span><span class="sxs-lookup"><span data-stu-id="05e03-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-239">Disableignoringcertificateerrors</span><span class="sxs-lookup"><span data-stu-id="05e03-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-242">Disableinprivatebrowsing</span><span class="sxs-lookup"><span data-stu-id="05e03-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-245">Disableprocessesinenhancedprotectedmode</span><span class="sxs-lookup"><span data-stu-id="05e03-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-248">Disableproxychange</span><span class="sxs-lookup"><span data-stu-id="05e03-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-251">Disablesearchproviderchange</span><span class="sxs-lookup"><span data-stu-id="05e03-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-254">Disablesecondaryhomepagechange</span><span class="sxs-lookup"><span data-stu-id="05e03-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-257">Disablesecuritysettingscheck</span><span class="sxs-lookup"><span data-stu-id="05e03-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-260">Donotallowactivexcontrolsinprotectedmode</span><span class="sxs-lookup"><span data-stu-id="05e03-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-263">Donotblockoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-266">Donotblockoutdatedactivexcontrolsonspecificdomains</span><span class="sxs-lookup"><span data-stu-id="05e03-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-269">Includezalllocalsites</span><span class="sxs-lookup"><span data-stu-id="05e03-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-271">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-272">Includepallnetworkpath</span><span class="sxs-lookup"><span data-stu-id="05e03-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-274">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="05e03-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05e03-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05e03-278">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="05e03-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-279">Internetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-281">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-282">Internetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-283">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-284">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-285">Internetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-287">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-288">Internetzoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="05e03-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-290">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-291">Internetzoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="05e03-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-293">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-294">Internetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-296">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-297">Internetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-299">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-300">Internetzoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="05e03-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-302">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-303">Internetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-305">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-306">Internetzonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-308">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-309">Internetzonezugewonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="05e03-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-311">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-312">Internetzoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-314">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-315">Internetzoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="05e03-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-317">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-318">Internetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-320">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-321">Internetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-323">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-324">Internetzoneallowupdatestostatus barviascript</span><span class="sxs-lookup"><span data-stu-id="05e03-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-326">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-327">Internetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-329">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-330">Internetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-332">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-333">Internetzonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-335">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-336">Internetzonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-338">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-339">Internetzoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="05e03-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-341">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-342">Internetzoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="05e03-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-344">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-345">Internetzoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="05e03-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-347">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-348">Internetzoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="05e03-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-350">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-351">Internetzoneenableprotectedmode</span><span class="sxs-lookup"><span data-stu-id="05e03-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-353">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-354">Internetzoneincludelta Update Server-Datei</span><span class="sxs-lookup"><span data-stu-id="05e03-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-356">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-357">Internetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-359">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-360">Internetzonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-362">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-363">Internetzonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="05e03-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-365">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-366">Internetzonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="05e03-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-368">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-369">Internetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-370">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-371">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-372">Internetzonerunnetframeworkreliantcomponentsnotsignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="05e03-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-374">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-375">Internetzonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="05e03-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-377">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-378">Internetzoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="05e03-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-380">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-381">Internetzoneuonpopupblocker</span><span class="sxs-lookup"><span data-stu-id="05e03-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-383">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-384">Internetzonewebsitesinlessprivilegedzonescannavigateinonthiszone</span><span class="sxs-lookup"><span data-stu-id="05e03-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-385">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-386">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-387">Intranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-389">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-390">Intranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-392">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-393">Intranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-394">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-395">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-396">Intranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-397">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-398">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-399">Intranetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-401">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-402">Intranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-404">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-405">Intranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-407">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-408">Intranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-409">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-410">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-411">Intranetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-413">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-414">Intranetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-416">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-417">Intranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-419">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-420">Intranetzoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="05e03-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-422">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-423">Intranetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-425">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-426">Intranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-428">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-429">Localmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-431">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-432">Localmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-433">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-434">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-435">Localmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-437">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-438">Localmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-440">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-441">Localmachinezonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-443">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-444">Localmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-446">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-447">Localmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-449">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-450">Localmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-451">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-452">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-453">Localmachinezonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-454">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-455">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-456">Localmachinezonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-457">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-458">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-459">Localmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-460">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-461">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-462">Localmachinezonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-463">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-464">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-465">Localmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-466">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-467">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-468">Lockeddowninternetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-470">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-471">Lockeddowninternetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-472">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-473">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-474">Lockeddowninternetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-475">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-476">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-477">Lockeddowninternetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-478">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-479">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-480">Lockeddowninternetzonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="05e03-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-482">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-483">Lockeddowninternetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-484">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-485">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-486">Lockeddowninternetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-488">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-489">Lockeddowninternetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-490">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-491">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-492">Lockeddowninternetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-493">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-494">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-495">Lockeddowninternetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-496">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-497">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-498">Lockeddowninternetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-499">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-500">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-501">Lockeddowninternetzonendavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-502">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-503">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-504">Lockeddownintranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-505">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-506">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-507">Lockeddownintranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-508">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-509">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-510">Lockeddownintranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-511">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-512">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-513">Lockeddownintranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-514">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-515">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-516">Lockeddownintranetzonezuden ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-517">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-518">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-519">Lockeddownintranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-520">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-521">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-522">Lockeddownintranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-524">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-525">Lockeddownintranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-526">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-527">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-528">Lockeddownintranetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-529">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-530">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-531">Lockeddownintranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-532">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-533">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-534">Lockeddownintranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-535">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-536">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-537">Lockeddownloader calmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-538">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-539">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-540">Lockeddownloader calmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-541">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-542">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-543">Lockeddownloader calmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-544">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-545">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-546">Lockeddownloader calmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-547">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-548">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-549">Lockeddownloader calmachinezonezuzugessprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-550">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-551">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-552">Lockeddownloader calmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-553">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-554">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-555">Lockeddownloader calmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-556">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-557">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-558">Lockeddownloader calmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-559">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-560">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-561">Lockeddownloader calmachinezonezuzugegenserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-562">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-563">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-564">Lockeddownloader calmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-565">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-566">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-567">Lockeddownloader calmachinezonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-568">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-569">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-570">Lockeddownloader calmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-571">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-572">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-573">Lockeddownrestrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-574">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-575">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-576">Lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-577">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-578">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-579">Lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-580">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-581">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-582">Lockeddownrestrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-583">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-584">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-585">Lockeddownrestrictedsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-586">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-587">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-588">Lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-589">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-590">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-591">Lockeddownrestrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-592">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-593">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-594">Lockeddownrestrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-595">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-596">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-597">Lockeddownrestrictedsiteszonezuzustuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-598">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-599">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-600">Lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-601">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-602">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-603">Lockeddownrestrictedsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-604">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-605">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-606">Lockeddownrestrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-607">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-608">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-609">Lockeddowntreuhänder dsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-610">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-611">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-612">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-613">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-614">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-615">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-616">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-617">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-618">Lockeddowntreuhänder dsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-619">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-620">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-621">Lockeddowntreuhänder dsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-622">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-623">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-624">Lockeddowntreuhänder dsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-625">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-626">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-627">Lockeddowntreuhänder dsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-628">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-629">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-630">Lockeddowntreuhänder dsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-631">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-632">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-633">Lockeddowntreuhänder dsiteszonezugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-634">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-635">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-636">Lockeddowntreuhänder dsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-637">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-638">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-639">Lockeddowntreudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-640">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-641">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-642">Lockeddowntreuhänder dsiteszoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-643">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-644">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-645">Mimesniffingsafetyfeatureinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="05e03-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-646">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-647">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-648">Mkprotocolsecurityrestrictioninternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="05e03-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-649">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-650">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-651">Notificationbarinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="05e03-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-652">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-653">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="05e03-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-655">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-656">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05e03-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05e03-657">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="05e03-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-658">Preventmanagingsmartscreenfilter</span><span class="sxs-lookup"><span data-stu-id="05e03-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-659">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-660">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-661">Preventperuserinstallationofaktivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-662">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-663">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-664">Schutzfromzoneelevationinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="05e03-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-665">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-666">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-667">Removerunthistimebuttonforoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-668">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-669">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-670">Restrictactivexinstallinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="05e03-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-671">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-672">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-673">Restrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-674">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-675">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-676">Restrictedsiteszoneallowactivescripting</span><span class="sxs-lookup"><span data-stu-id="05e03-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-677">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-678">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-679">Restrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-680">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-681">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-682">Restrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-683">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-684">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-685">Restrictedsiteszoneallowbinaryandscriptverhaltensweisen</span><span class="sxs-lookup"><span data-stu-id="05e03-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-686">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-687">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-688">Restrictedsiteszoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="05e03-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-689">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-690">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-691">Restrictedsiteszoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="05e03-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-692">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-693">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-694">Restrictedsiteszoneallowfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-695">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-696">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-697">Restrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-698">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-699">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-700">Restrictedsiteszonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="05e03-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-701">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-702">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-703">Restrictedsiteszoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="05e03-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-704">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-705">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-706">Restrictedsiteszoneallowmetarefresh</span><span class="sxs-lookup"><span data-stu-id="05e03-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-707">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-708">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-709">Restrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-710">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-711">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-712">Restrictedsiteszonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-713">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-714">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-715">Restrictedsiteszonezuzugwonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="05e03-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-716">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-717">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-718">Restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-719">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-720">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-721">Restrictedsiteszoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="05e03-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-722">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-723">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-724">Restrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-725">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-726">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-727">Restrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-728">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-729">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-730">Restrictedsiteszoneallowupdatestostatobarviascript</span><span class="sxs-lookup"><span data-stu-id="05e03-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-731">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-732">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-733">Restrictedsiteszonezuzustandserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-734">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-735">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-736">Restrictedsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-737">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-738">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-739">Restrictedsiteszonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-740">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-741">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-742">Restrictedsiteszonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-743">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-744">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-745">Restrictedsiteszoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="05e03-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-746">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-747">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-748">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="05e03-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-749">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-750">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-751">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="05e03-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-752">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-753">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-754">Restrictedsiteszoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="05e03-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-755">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-756">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-757">Restrictedsiteszoneincluschocalpatheincluminguploadingfilestoserver</span><span class="sxs-lookup"><span data-stu-id="05e03-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-758">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-759">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-760">Restrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-761">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-762">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-763">Restrictedsiteszonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-764">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-765">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-766">Einschränktedsiteszonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="05e03-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-767">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-768">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-769">Restrictedsiteszonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="05e03-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-770">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-771">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-772">Restrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-773">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-774">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-775">Restrictedsiteszonumavigatewindowsandframesacrossdomains</span><span class="sxs-lookup"><span data-stu-id="05e03-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-776">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-777">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-778">Restrictedsiteszonerunactivexcontrolsandplugins</span><span class="sxs-lookup"><span data-stu-id="05e03-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-779">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-780">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-781">Restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="05e03-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-782">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-783">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-784">Restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting</span><span class="sxs-lookup"><span data-stu-id="05e03-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-785">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-786">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-787">Restrictedsiteszonescriptingof JavaApplets</span><span class="sxs-lookup"><span data-stu-id="05e03-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-788">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-789">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-790">Restrictedsiteszoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="05e03-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-791">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-792">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-793">Restrictedsiteszonzname der crosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="05e03-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-794">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-795">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-796">Restrictedsiteszuniturnonprotectedmode</span><span class="sxs-lookup"><span data-stu-id="05e03-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-797">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-798">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-799">Restrictedsiteszoneul Popupblocker</span><span class="sxs-lookup"><span data-stu-id="05e03-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-800">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-801">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-802">Restrictfiledownloadinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="05e03-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-803">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-804">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-805">Scriptedwindowsecurityrestrictionsinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="05e03-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-806">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-807">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-808">Searchproviderlist</span><span class="sxs-lookup"><span data-stu-id="05e03-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-809">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-810">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-811">Specifyuseofaktivexinstallerservice</span><span class="sxs-lookup"><span data-stu-id="05e03-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-812">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-813">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-814">Treuhändsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="05e03-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-815">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-816">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-817">Treudsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-818">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-819">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-820">Treuhändsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-821">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-822">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-823">Treuhändsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="05e03-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-824">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-825">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-826">Treuhänder-siteszonezuzugssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="05e03-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-827">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-828">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-829">Treuhändsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="05e03-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-830">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-831">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-832">Treuhändsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="05e03-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-833">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-834">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-835">Treuhändsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="05e03-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-836">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-837">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-838">Treuhändsiteszonezuzugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="05e03-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-839">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-840">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-841">Treuhändsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-842">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-843">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-844">Treuhändsiteszonedontrunantimalwareprogramsagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-845">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-846">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-847">Treuhändsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="05e03-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-848">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-849">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-850">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedassafe</span><span class="sxs-lookup"><span data-stu-id="05e03-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-851">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-852">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05e03-853">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="05e03-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-854">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-855">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-856">Treudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="05e03-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-857">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-858">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="05e03-859">Treuhändsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="05e03-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="05e03-860">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="05e03-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05e03-861">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="05e03-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05e03-862">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05e03-862">Requirements</span></span>



| <span data-ttu-id="05e03-863">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05e03-863">Requirement</span></span> | <span data-ttu-id="05e03-864">Wert</span><span class="sxs-lookup"><span data-stu-id="05e03-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05e03-865">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05e03-865">Minimum supported client</span></span><br/> | <span data-ttu-id="05e03-866">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05e03-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05e03-867">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05e03-867">Minimum supported server</span></span><br/> | <span data-ttu-id="05e03-868">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05e03-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="05e03-869">Namespace</span><span class="sxs-lookup"><span data-stu-id="05e03-869">Namespace</span></span><br/>                | <span data-ttu-id="05e03-870">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="05e03-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="05e03-871">MOF</span><span class="sxs-lookup"><span data-stu-id="05e03-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05e03-872"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="05e03-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="05e03-873">DLL</span><span class="sxs-lookup"><span data-stu-id="05e03-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05e03-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05e03-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

