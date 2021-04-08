---
title: MDM_Policy_Result01_InternetExplorer02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ InternetExplorer02 stellt die Internet Explorer-Richtlinien dar.
ms.assetid: 4b14c9ea-2f4d-4e5a-8aab-3741f15b0b1e
keywords:
- MDM_Policy_Result01_InternetExplorer02-Klasse
- MDM_Policy_Result01_InternetExplorer02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02.InstanceID
- MDM_Policy_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63308b6100d6bd4ec924307a9dcd3892096fc0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949765"
---
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="be476-105">MDM- \_ Richtlinie \_ Result01 \_ InternetExplorer02-Klasse</span><span class="sxs-lookup"><span data-stu-id="be476-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="be476-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="be476-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="be476-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="be476-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="be476-108">Die MDM- \_ Richtlinie \_ Result01 \_ InternetExplorer02 stellt die Internet Explorer-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="be476-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="be476-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="be476-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be476-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="be476-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowFallbackToSSL3;
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
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DisableSecuritySettingsCheck;
  string DisableUpdateCheck;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DoNotAllowUsersToAddSites;
  string DoNotAllowUsersToChangePolicies;
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
  string SecurityZonesUseOnlyMachineSettings;
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

## <a name="members"></a><span data-ttu-id="be476-111">Member</span><span class="sxs-lookup"><span data-stu-id="be476-111">Members</span></span>

<span data-ttu-id="be476-112">Die **MDM- \_ Richtlinie \_ Result01 \_ InternetExplorer02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="be476-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="be476-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="be476-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be476-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="be476-114">Properties</span></span>

<span data-ttu-id="be476-115">Die **MDM- \_ Richtlinie \_ Result01 \_ InternetExplorer02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="be476-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="be476-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="be476-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-119">Allowactivexfiltering</span><span class="sxs-lookup"><span data-stu-id="be476-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-122">Allowaddonlist</span><span class="sxs-lookup"><span data-stu-id="be476-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-125">Allowcertificateaddressmismatchwarning</span><span class="sxs-lookup"><span data-stu-id="be476-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-128">Allowdelta etingbrowsinghistoryonexit</span><span class="sxs-lookup"><span data-stu-id="be476-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-131">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="be476-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-134">"Zuweisung von" "" "".</span><span class="sxs-lookup"><span data-stu-id="be476-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-137">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="be476-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="be476-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="be476-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-146">"Expwinternetexplorerstandardsmode"</span><span class="sxs-lookup"><span data-stu-id="be476-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-149">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="be476-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-152">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="be476-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-155">Allowlocalmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-158">Allowlockeddowninternetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-161">Allowlockeddownintranetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-164">Allowlockeddownloader calmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-167">Allowlockeddownrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-170">' Zugwonewordentry '</span><span class="sxs-lookup"><span data-stu-id="be476-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-173">Allowsiteononezuzuzustandliste</span><span class="sxs-lookup"><span data-stu-id="be476-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-176">Allowslockeddowntreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-179">Allowsoftware\signatureisinvalid</span><span class="sxs-lookup"><span data-stu-id="be476-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-182">Allowsrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-185">Allowvorschlags stedsites</span><span class="sxs-lookup"><span data-stu-id="be476-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-188">Allowtreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="be476-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-191">Checkservercertificaterevozierung</span><span class="sxs-lookup"><span data-stu-id="be476-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-194">Checksignaturesondownloader-dprogramme</span><span class="sxs-lookup"><span data-stu-id="be476-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-196">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-197">"Konsistentmimehandlinginternetexplorerprocesses"</span><span class="sxs-lookup"><span data-stu-id="be476-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-200">Disableadobeflash</span><span class="sxs-lookup"><span data-stu-id="be476-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-203">Disableblockingof outdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-206">Disablebypassofsmartscreenwarning</span><span class="sxs-lookup"><span data-stu-id="be476-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-209">Disablebypassofsmartscreenwarningsaboutuncommonfiles</span><span class="sxs-lookup"><span data-stu-id="be476-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-212">Disableconfiguringhistory</span><span class="sxs-lookup"><span data-stu-id="be476-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-215">Disablecrash-Erkennung</span><span class="sxs-lookup"><span data-stu-id="be476-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-218">Disablecustomerexperiendceimprovementprogramparticipation</span><span class="sxs-lookup"><span data-stu-id="be476-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-221">Disabledelta etinguservisitedwebsites</span><span class="sxs-lookup"><span data-stu-id="be476-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-224">Disablereclosuredownload</span><span class="sxs-lookup"><span data-stu-id="be476-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-227">Disableverschlüsseltionsupport</span><span class="sxs-lookup"><span data-stu-id="be476-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="be476-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-233">Disableflipheadfeature</span><span class="sxs-lookup"><span data-stu-id="be476-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-236">Disableignoringcertificateerrors</span><span class="sxs-lookup"><span data-stu-id="be476-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-239">Disableinprivatebrowsing</span><span class="sxs-lookup"><span data-stu-id="be476-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-242">Disableprocessesinenhancedprotectedmode</span><span class="sxs-lookup"><span data-stu-id="be476-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-245">Disableproxychange</span><span class="sxs-lookup"><span data-stu-id="be476-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-248">Disablesearchproviderchange</span><span class="sxs-lookup"><span data-stu-id="be476-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-251">Disablesecondaryhomepagechange</span><span class="sxs-lookup"><span data-stu-id="be476-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-254">Disablesecuritysettingscheck</span><span class="sxs-lookup"><span data-stu-id="be476-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-257">Disableupdatecheck</span><span class="sxs-lookup"><span data-stu-id="be476-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-260">Donotallowactivexcontrolsinprotectedmode</span><span class="sxs-lookup"><span data-stu-id="be476-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-263">Donotallowuserstoaddsites</span><span class="sxs-lookup"><span data-stu-id="be476-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-266">Donotallowuserstochangepolicies</span><span class="sxs-lookup"><span data-stu-id="be476-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-269">Donotblockoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-271">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-272">Donotblockoutdatedactivexcontrolsonspecificdomains</span><span class="sxs-lookup"><span data-stu-id="be476-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-274">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-275">Includezalllocalsites</span><span class="sxs-lookup"><span data-stu-id="be476-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-277">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-278">Includepallnetworkpath</span><span class="sxs-lookup"><span data-stu-id="be476-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-280">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="be476-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="be476-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be476-284">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be476-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-285">Internetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-287">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-288">Internetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-290">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-291">Internetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-293">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-294">Internetzoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="be476-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-296">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-297">Internetzoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="be476-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-299">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-300">Internetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-302">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-303">Internetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-305">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-306">Internetzoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="be476-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-308">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-309">Internetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-311">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-312">Internetzonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-314">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-315">Internetzonezugewonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="be476-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-317">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-318">Internetzoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="be476-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-320">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-321">Internetzoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="be476-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-323">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-324">Internetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-326">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-327">Internetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-329">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-330">Internetzoneallowupdatestostatus barviascript</span><span class="sxs-lookup"><span data-stu-id="be476-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-332">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-333">Internetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-335">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-336">Internetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-338">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-339">Internetzonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-341">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-342">Internetzonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-344">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-345">Internetzoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="be476-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-347">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-348">Internetzoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="be476-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-350">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-351">Internetzoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="be476-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-353">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-354">Internetzoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="be476-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-356">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-357">Internetzoneenableprotectedmode</span><span class="sxs-lookup"><span data-stu-id="be476-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-359">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-360">Internetzoneincludelta Update Server-Datei</span><span class="sxs-lookup"><span data-stu-id="be476-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-362">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-363">Internetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-365">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-366">Internetzonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-368">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-369">Internetzonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="be476-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-370">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-371">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-372">Internetzonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="be476-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-374">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-375">Internetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-377">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-378">Internetzonerunnetframeworkreliantcomponentsnotsignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="be476-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-380">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-381">Internetzonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="be476-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-383">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-384">Internetzoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="be476-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-385">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-386">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-387">Internetzoneuonpopupblocker</span><span class="sxs-lookup"><span data-stu-id="be476-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-389">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-390">Internetzonewebsitesinlessprivilegedzonescannavigateinonthiszone</span><span class="sxs-lookup"><span data-stu-id="be476-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-392">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-393">Intranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-394">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-395">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-396">Intranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-397">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-398">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-399">Intranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-401">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-402">Intranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-404">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-405">Intranetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-407">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-408">Intranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-409">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-410">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-411">Intranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-413">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-414">Intranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-416">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-417">Intranetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-419">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-420">Intranetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-422">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-423">Intranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-425">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-426">Intranetzoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="be476-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-428">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-429">Intranetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-431">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-432">Intranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-433">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-434">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-435">Localmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-437">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-438">Localmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-440">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-441">Localmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-443">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-444">Localmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-446">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-447">Localmachinezonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-449">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-450">Localmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-451">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-452">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-453">Localmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-454">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-455">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-456">Localmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-457">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-458">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-459">Localmachinezonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-460">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-461">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-462">Localmachinezonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-463">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-464">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-465">Localmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-466">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-467">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-468">Localmachinezonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-470">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-471">Localmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-472">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-473">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-474">Lockeddowninternetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-475">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-476">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-477">Lockeddowninternetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-478">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-479">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-480">Lockeddowninternetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-482">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-483">Lockeddowninternetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-484">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-485">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-486">Lockeddowninternetzonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="be476-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-488">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-489">Lockeddowninternetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-490">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-491">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-492">Lockeddowninternetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-493">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-494">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-495">Lockeddowninternetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-496">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-497">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-498">Lockeddowninternetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-499">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-500">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-501">Lockeddowninternetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-502">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-503">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-504">Lockeddowninternetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-505">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-506">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-507">Lockeddowninternetzonendavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-508">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-509">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-510">Lockeddownintranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-511">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-512">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-513">Lockeddownintranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-514">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-515">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-516">Lockeddownintranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-517">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-518">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-519">Lockeddownintranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-520">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-521">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-522">Lockeddownintranetzonezuden ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-524">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-525">Lockeddownintranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-526">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-527">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-528">Lockeddownintranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-529">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-530">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-531">Lockeddownintranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-532">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-533">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-534">Lockeddownintranetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-535">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-536">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-537">Lockeddownintranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-538">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-539">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-540">Lockeddownintranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-541">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-542">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-543">Lockeddownloader calmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-544">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-545">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-546">Lockeddownloader calmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-547">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-548">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-549">Lockeddownloader calmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-550">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-551">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-552">Lockeddownloader calmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-553">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-554">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-555">Lockeddownloader calmachinezonezuzugessprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-556">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-557">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-558">Lockeddownloader calmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-559">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-560">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-561">Lockeddownloader calmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-562">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-563">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-564">Lockeddownloader calmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-565">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-566">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-567">Lockeddownloader calmachinezonezuzugegenserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-568">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-569">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-570">Lockeddownloader calmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-571">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-572">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-573">Lockeddownloader calmachinezonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-574">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-575">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-576">Lockeddownloader calmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-577">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-578">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-579">Lockeddownrestrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-580">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-581">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-582">Lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-583">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-584">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-585">Lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-586">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-587">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-588">Lockeddownrestrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-589">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-590">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-591">Lockeddownrestrictedsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-592">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-593">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-594">Lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-595">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-596">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-597">Lockeddownrestrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-598">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-599">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-600">Lockeddownrestrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-601">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-602">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-603">Lockeddownrestrictedsiteszonezuzustuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-604">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-605">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-606">Lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-607">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-608">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-609">Lockeddownrestrictedsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-610">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-611">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-612">Lockeddownrestrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-613">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-614">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-615">Lockeddowntreuhänder dsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-616">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-617">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-618">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-619">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-620">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-621">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-622">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-623">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-624">Lockeddowntreuhänder dsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-625">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-626">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-627">Lockeddowntreuhänder dsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-628">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-629">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-630">Lockeddowntreuhänder dsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-631">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-632">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-633">Lockeddowntreuhänder dsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-634">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-635">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-636">Lockeddowntreuhänder dsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-637">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-638">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-639">Lockeddowntreuhänder dsiteszonezugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-640">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-641">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-642">Lockeddowntreuhänder dsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-643">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-644">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-645">Lockeddowntreudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-646">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-647">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-648">Lockeddowntreuhänder dsiteszoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-649">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-650">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-651">Mimesniffingsafetyfeatureinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="be476-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-652">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-653">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-654">Mkprotocolsecurityrestrictioninternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="be476-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-655">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-656">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-657">Notificationbarinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="be476-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-658">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-659">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="be476-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-661">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-662">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="be476-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be476-663">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be476-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-664">Preventmanagingsmartscreenfilter</span><span class="sxs-lookup"><span data-stu-id="be476-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-665">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-666">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-667">Preventperuserinstallationofaktivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-668">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-669">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-670">Schutzfromzoneelevationinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="be476-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-671">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-672">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-673">Removerunthistimebuttonforoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-674">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-675">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-676">Restrictactivexinstallinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="be476-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-677">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-678">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-679">Restrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-680">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-681">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-682">Restrictedsiteszoneallowactivescripting</span><span class="sxs-lookup"><span data-stu-id="be476-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-683">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-684">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-685">Restrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-686">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-687">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-688">Restrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-689">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-690">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-691">Restrictedsiteszoneallowbinaryandscriptverhaltensweisen</span><span class="sxs-lookup"><span data-stu-id="be476-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-692">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-693">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-694">Restrictedsiteszoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="be476-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-695">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-696">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-697">Restrictedsiteszoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="be476-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-698">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-699">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-700">Restrictedsiteszoneallowfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-701">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-702">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-703">Restrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-704">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-705">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-706">Restrictedsiteszonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="be476-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-707">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-708">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-709">Restrictedsiteszoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="be476-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-710">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-711">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-712">Restrictedsiteszoneallowmetarefresh</span><span class="sxs-lookup"><span data-stu-id="be476-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-713">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-714">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-715">Restrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-716">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-717">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-718">Restrictedsiteszonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-719">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-720">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-721">Restrictedsiteszonezuzugwonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="be476-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-722">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-723">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-724">Restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="be476-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-725">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-726">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-727">Restrictedsiteszoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="be476-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-728">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-729">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-730">Restrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-731">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-732">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-733">Restrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-734">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-735">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-736">Restrictedsiteszoneallowupdatestostatobarviascript</span><span class="sxs-lookup"><span data-stu-id="be476-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-737">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-738">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-739">Restrictedsiteszonezuzustandserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-740">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-741">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-742">Restrictedsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-743">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-744">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-745">Restrictedsiteszonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-746">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-747">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-748">Restrictedsiteszonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-749">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-750">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-751">Restrictedsiteszoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="be476-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-752">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-753">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-754">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="be476-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-755">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-756">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-757">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="be476-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-758">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-759">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-760">Restrictedsiteszoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="be476-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-761">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-762">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-763">Restrictedsiteszoneincluschocalpatheincluminguploadingfilestoserver</span><span class="sxs-lookup"><span data-stu-id="be476-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-764">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-765">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-766">Restrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-767">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-768">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-769">Restrictedsiteszonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-770">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-771">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-772">Einschränktedsiteszonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="be476-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-773">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-774">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-775">Restrictedsiteszonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="be476-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-776">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-777">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-778">Restrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-779">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-780">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-781">Restrictedsiteszonumavigatewindowsandframesacrossdomains</span><span class="sxs-lookup"><span data-stu-id="be476-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-782">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-783">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-784">Restrictedsiteszonerunactivexcontrolsandplugins</span><span class="sxs-lookup"><span data-stu-id="be476-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-785">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-786">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-787">Restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="be476-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-788">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-789">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-790">Restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting</span><span class="sxs-lookup"><span data-stu-id="be476-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-791">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-792">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-793">Restrictedsiteszonescriptingof JavaApplets</span><span class="sxs-lookup"><span data-stu-id="be476-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-794">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-795">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-796">Restrictedsiteszoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="be476-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-797">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-798">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-799">Restrictedsiteszonzname der crosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="be476-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-800">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-801">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-802">Restrictedsiteszuniturnonprotectedmode</span><span class="sxs-lookup"><span data-stu-id="be476-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-803">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-804">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-805">Restrictedsiteszoneul Popupblocker</span><span class="sxs-lookup"><span data-stu-id="be476-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-806">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-807">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-808">Restrictfiledownloadinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="be476-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-809">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-810">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-811">Scriptedwindowsecurityrestrictionsinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="be476-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-812">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-813">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-814">Searchproviderlist</span><span class="sxs-lookup"><span data-stu-id="be476-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-815">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-816">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-817">Securityzonesuseonlymachinesettings</span><span class="sxs-lookup"><span data-stu-id="be476-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-818">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-819">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-820">Specifyuseofaktivexinstallerservice</span><span class="sxs-lookup"><span data-stu-id="be476-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-821">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-822">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-823">Treuhändsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="be476-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-824">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-825">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-826">Treudsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-827">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-828">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-829">Treuhändsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="be476-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-830">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-831">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-832">Treuhändsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="be476-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-833">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-834">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-835">Treuhänder-siteszonezuzugssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="be476-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-836">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-837">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-838">Treuhändsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="be476-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-839">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-840">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-841">Treuhändsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="be476-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-842">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-843">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-844">Treuhändsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="be476-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-845">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-846">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-847">Treuhändsiteszonezuzugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="be476-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-848">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-849">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-850">Treuhändsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-851">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-852">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-853">Treuhändsiteszonedontrunantimalwareprogramsagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-854">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-855">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-856">Treuhändsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="be476-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-857">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-858">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-859">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedassafe</span><span class="sxs-lookup"><span data-stu-id="be476-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-860">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-861">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be476-862">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="be476-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-863">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-864">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-865">Treudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="be476-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-866">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-867">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="be476-868">Treuhändsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="be476-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="be476-869">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="be476-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be476-870">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="be476-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be476-871">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be476-871">Requirements</span></span>



| <span data-ttu-id="be476-872">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be476-872">Requirement</span></span> | <span data-ttu-id="be476-873">Wert</span><span class="sxs-lookup"><span data-stu-id="be476-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be476-874">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be476-874">Minimum supported client</span></span><br/> | <span data-ttu-id="be476-875">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be476-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be476-876">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be476-876">Minimum supported server</span></span><br/> | <span data-ttu-id="be476-877">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="be476-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="be476-878">Namespace</span><span class="sxs-lookup"><span data-stu-id="be476-878">Namespace</span></span><br/>                | <span data-ttu-id="be476-879">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="be476-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="be476-880">MOF</span><span class="sxs-lookup"><span data-stu-id="be476-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be476-881"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="be476-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="be476-882">DLL</span><span class="sxs-lookup"><span data-stu-id="be476-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be476-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be476-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

