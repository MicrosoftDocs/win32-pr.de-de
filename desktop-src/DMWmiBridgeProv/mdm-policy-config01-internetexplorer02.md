---
title: MDM_Policy_Config01_InternetExplorer02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ InternetExplorer02-Klasse konfiguriert die Internet Explorer-Richtlinien.
ms.assetid: 32cc6a64-3008-4add-96e8-33b31beb207f
keywords:
- MDM_Policy_Config01_InternetExplorer02-Klasse
- MDM_Policy_Config01_InternetExplorer02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02.InstanceID
- MDM_Policy_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a448b0034e3f4658f1c13b238abf455bf413a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476617"
---
# <a name="mdm_policy_config01_internetexplorer02-class"></a><span data-ttu-id="589d8-105">MDM- \_ Richtlinie \_ Config01 \_ InternetExplorer02-Klasse</span><span class="sxs-lookup"><span data-stu-id="589d8-105">MDM\_Policy\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="589d8-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="589d8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="589d8-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="589d8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="589d8-108">Die MDM- \_ Richtlinie \_ Config01 \_ InternetExplorer02-Klasse konfiguriert die Internet Explorer-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="589d8-108">The MDM\_Policy\_Config01\_InternetExplorer02 class configures the Internet Explorer policies.</span></span>

<span data-ttu-id="589d8-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="589d8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="589d8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="589d8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="589d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="589d8-111">Members</span></span>

<span data-ttu-id="589d8-112">Die **MDM- \_ Richtlinie \_ Config01 \_ InternetExplorer02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="589d8-112">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="589d8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="589d8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="589d8-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="589d8-114">Properties</span></span>

<span data-ttu-id="589d8-115">Die **MDM- \_ Richtlinie \_ Config01 \_ InternetExplorer02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="589d8-115">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="589d8-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="589d8-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-119">Allowactivexfiltering</span><span class="sxs-lookup"><span data-stu-id="589d8-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-122">Allowaddonlist</span><span class="sxs-lookup"><span data-stu-id="589d8-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-125">Allowcertificateaddressmismatchwarning</span><span class="sxs-lookup"><span data-stu-id="589d8-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-128">Allowdelta etingbrowsinghistoryonexit</span><span class="sxs-lookup"><span data-stu-id="589d8-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-131">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="589d8-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-134">"Zuweisung von" "" "".</span><span class="sxs-lookup"><span data-stu-id="589d8-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-137">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="589d8-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="589d8-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="589d8-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-146">"Expwinternetexplorerstandardsmode"</span><span class="sxs-lookup"><span data-stu-id="589d8-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-149">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="589d8-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-152">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="589d8-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-155">Allowlocalmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-158">Allowlockeddowninternetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-161">Allowlockeddownintranetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-164">Allowlockeddownloader calmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-167">Allowlockeddownrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-170">' Zugwonewordentry '</span><span class="sxs-lookup"><span data-stu-id="589d8-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-173">Allowsiteononezuzuzustandliste</span><span class="sxs-lookup"><span data-stu-id="589d8-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-176">Allowslockeddowntreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-179">Allowsoftware\signatureisinvalid</span><span class="sxs-lookup"><span data-stu-id="589d8-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-182">Allowsrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-185">Allowvorschlags stedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-188">Allowtreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="589d8-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-191">Checkservercertificaterevozierung</span><span class="sxs-lookup"><span data-stu-id="589d8-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-194">Checksignaturesondownloader-dprogramme</span><span class="sxs-lookup"><span data-stu-id="589d8-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-196">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-197">"Konsistentmimehandlinginternetexplorerprocesses"</span><span class="sxs-lookup"><span data-stu-id="589d8-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-200">Disableadobeflash</span><span class="sxs-lookup"><span data-stu-id="589d8-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-203">Disableblockingof outdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-206">Disablebypassofsmartscreenwarning</span><span class="sxs-lookup"><span data-stu-id="589d8-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-209">Disablebypassofsmartscreenwarningsaboutuncommonfiles</span><span class="sxs-lookup"><span data-stu-id="589d8-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-212">Disableconfiguringhistory</span><span class="sxs-lookup"><span data-stu-id="589d8-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-215">Disablecrash-Erkennung</span><span class="sxs-lookup"><span data-stu-id="589d8-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-218">Disablecustomerexperiendceimprovementprogramparticipation</span><span class="sxs-lookup"><span data-stu-id="589d8-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-221">Disabledelta etinguservisitedwebsites</span><span class="sxs-lookup"><span data-stu-id="589d8-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-224">Disablereclosuredownload</span><span class="sxs-lookup"><span data-stu-id="589d8-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-227">Disableverschlüsseltionsupport</span><span class="sxs-lookup"><span data-stu-id="589d8-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="589d8-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-233">Disableflipheadfeature</span><span class="sxs-lookup"><span data-stu-id="589d8-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-236">Disableignoringcertificateerrors</span><span class="sxs-lookup"><span data-stu-id="589d8-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-239">Disableinprivatebrowsing</span><span class="sxs-lookup"><span data-stu-id="589d8-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-242">Disableprocessesinenhancedprotectedmode</span><span class="sxs-lookup"><span data-stu-id="589d8-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-245">Disableproxychange</span><span class="sxs-lookup"><span data-stu-id="589d8-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-248">Disablesearchproviderchange</span><span class="sxs-lookup"><span data-stu-id="589d8-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-251">Disablesecondaryhomepagechange</span><span class="sxs-lookup"><span data-stu-id="589d8-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-254">Disablesecuritysettingscheck</span><span class="sxs-lookup"><span data-stu-id="589d8-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-257">Disableupdatecheck</span><span class="sxs-lookup"><span data-stu-id="589d8-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-260">Donotallowactivexcontrolsinprotectedmode</span><span class="sxs-lookup"><span data-stu-id="589d8-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-263">Donotallowuserstoaddsites</span><span class="sxs-lookup"><span data-stu-id="589d8-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-266">Donotallowuserstochangepolicies</span><span class="sxs-lookup"><span data-stu-id="589d8-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-269">Donotblockoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-271">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-272">Donotblockoutdatedactivexcontrolsonspecificdomains</span><span class="sxs-lookup"><span data-stu-id="589d8-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-274">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-275">Includezalllocalsites</span><span class="sxs-lookup"><span data-stu-id="589d8-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-277">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-278">Includepallnetworkpath</span><span class="sxs-lookup"><span data-stu-id="589d8-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-280">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="589d8-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="589d8-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589d8-284">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="589d8-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-285">Internetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-287">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-288">Internetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-290">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-291">Internetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-293">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-294">Internetzoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="589d8-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-296">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-297">Internetzoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="589d8-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-299">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-300">Internetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-302">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-303">Internetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-305">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-306">Internetzoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="589d8-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-308">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-309">Internetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-311">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-312">Internetzonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-314">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-315">Internetzonezugewonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="589d8-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-317">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-318">Internetzoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-320">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-321">Internetzoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="589d8-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-323">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-324">Internetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-326">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-327">Internetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-329">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-330">Internetzoneallowupdatestostatus barviascript</span><span class="sxs-lookup"><span data-stu-id="589d8-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-332">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-333">Internetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-335">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-336">Internetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-338">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-339">Internetzonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-341">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-342">Internetzonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-344">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-345">Internetzoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="589d8-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-347">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-348">Internetzoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="589d8-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-350">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-351">Internetzoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="589d8-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-353">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-354">Internetzoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="589d8-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-356">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-357">Internetzoneenableprotectedmode</span><span class="sxs-lookup"><span data-stu-id="589d8-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-359">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-360">Internetzoneincludelta Update Server-Datei</span><span class="sxs-lookup"><span data-stu-id="589d8-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-362">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-363">Internetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-365">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-366">Internetzonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-368">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-369">Internetzonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="589d8-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-370">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-371">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-372">Internetzonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="589d8-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-374">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-375">Internetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-377">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-378">Internetzonerunnetframeworkreliantcomponentsnotsignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="589d8-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-380">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-381">Internetzonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="589d8-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-383">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-384">Internetzoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="589d8-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-385">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-386">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-387">Internetzoneuonpopupblocker</span><span class="sxs-lookup"><span data-stu-id="589d8-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-389">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-390">Internetzonewebsitesinlessprivilegedzonescannavigateinonthiszone</span><span class="sxs-lookup"><span data-stu-id="589d8-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-392">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-393">Intranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-394">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-395">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-396">Intranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-397">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-398">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-399">Intranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-401">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-402">Intranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-404">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-405">Intranetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-407">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-408">Intranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-409">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-410">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-411">Intranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-413">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-414">Intranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-416">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-417">Intranetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-419">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-420">Intranetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-422">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-423">Intranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-425">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-426">Intranetzoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="589d8-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-428">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-429">Intranetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-431">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-432">Intranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-433">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-434">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-435">Localmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-437">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-438">Localmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-440">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-441">Localmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-443">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-444">Localmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-446">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-447">Localmachinezonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-449">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-450">Localmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-451">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-452">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-453">Localmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-454">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-455">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-456">Localmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-457">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-458">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-459">Localmachinezonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-460">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-461">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-462">Localmachinezonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-463">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-464">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-465">Localmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-466">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-467">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-468">Localmachinezonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-470">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-471">Localmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-472">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-473">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-474">Lockeddowninternetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-475">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-476">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-477">Lockeddowninternetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-478">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-479">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-480">Lockeddowninternetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-482">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-483">Lockeddowninternetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-484">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-485">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-486">Lockeddowninternetzonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="589d8-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-488">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-489">Lockeddowninternetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-490">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-491">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-492">Lockeddowninternetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-493">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-494">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-495">Lockeddowninternetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-496">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-497">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-498">Lockeddowninternetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-499">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-500">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-501">Lockeddowninternetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-502">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-503">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-504">Lockeddowninternetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-505">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-506">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-507">Lockeddowninternetzonendavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-508">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-509">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-510">Lockeddownintranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-511">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-512">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-513">Lockeddownintranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-514">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-515">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-516">Lockeddownintranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-517">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-518">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-519">Lockeddownintranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-520">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-521">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-522">Lockeddownintranetzonezuden ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-524">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-525">Lockeddownintranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-526">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-527">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-528">Lockeddownintranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-529">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-530">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-531">Lockeddownintranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-532">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-533">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-534">Lockeddownintranetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-535">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-536">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-537">Lockeddownintranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-538">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-539">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-540">Lockeddownintranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-541">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-542">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-543">Lockeddownloader calmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-544">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-545">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-546">Lockeddownloader calmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-547">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-548">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-549">Lockeddownloader calmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-550">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-551">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-552">Lockeddownloader calmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-553">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-554">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-555">Lockeddownloader calmachinezonezuzugessprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-556">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-557">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-558">Lockeddownloader calmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-559">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-560">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-561">Lockeddownloader calmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-562">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-563">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-564">Lockeddownloader calmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-565">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-566">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-567">Lockeddownloader calmachinezonezuzugegenserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-568">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-569">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-570">Lockeddownloader calmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-571">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-572">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-573">Lockeddownloader calmachinezonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-574">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-575">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-576">Lockeddownloader calmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-577">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-578">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-579">Lockeddownrestrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-580">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-581">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-582">Lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-583">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-584">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-585">Lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-586">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-587">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-588">Lockeddownrestrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-589">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-590">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-591">Lockeddownrestrictedsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-592">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-593">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-594">Lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-595">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-596">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-597">Lockeddownrestrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-598">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-599">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-600">Lockeddownrestrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-601">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-602">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-603">Lockeddownrestrictedsiteszonezuzustuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-604">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-605">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-606">Lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-607">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-608">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-609">Lockeddownrestrictedsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-610">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-611">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-612">Lockeddownrestrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-613">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-614">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-615">Lockeddowntreuhänder dsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-616">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-617">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-618">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-619">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-620">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-621">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-622">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-623">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-624">Lockeddowntreuhänder dsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-625">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-626">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-627">Lockeddowntreuhänder dsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-628">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-629">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-630">Lockeddowntreuhänder dsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-631">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-632">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-633">Lockeddowntreuhänder dsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-634">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-635">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-636">Lockeddowntreuhänder dsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-637">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-638">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-639">Lockeddowntreuhänder dsiteszonezugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-640">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-641">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-642">Lockeddowntreuhänder dsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-643">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-644">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-645">Lockeddowntreudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-646">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-647">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-648">Lockeddowntreuhänder dsiteszoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-649">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-650">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-651">Mimesniffingsafetyfeatureinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="589d8-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-652">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-653">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-654">Mkprotocolsecurityrestrictioninternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="589d8-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-655">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-656">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-657">Notificationbarinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="589d8-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-658">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-659">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="589d8-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-661">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-662">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="589d8-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="589d8-663">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="589d8-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-664">Preventmanagingsmartscreenfilter</span><span class="sxs-lookup"><span data-stu-id="589d8-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-665">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-666">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-667">Preventperuserinstallationofaktivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-668">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-669">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-670">Schutzfromzoneelevationinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="589d8-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-671">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-672">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-673">Removerunthistimebuttonforoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-674">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-675">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-676">Restrictactivexinstallinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="589d8-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-677">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-678">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-679">Restrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-680">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-681">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-682">Restrictedsiteszoneallowactivescripting</span><span class="sxs-lookup"><span data-stu-id="589d8-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-683">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-684">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-685">Restrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-686">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-687">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-688">Restrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-689">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-690">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-691">Restrictedsiteszoneallowbinaryandscriptverhaltensweisen</span><span class="sxs-lookup"><span data-stu-id="589d8-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-692">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-693">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-694">Restrictedsiteszoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="589d8-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-695">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-696">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-697">Restrictedsiteszoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="589d8-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-698">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-699">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-700">Restrictedsiteszoneallowfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-701">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-702">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-703">Restrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-704">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-705">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-706">Restrictedsiteszonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="589d8-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-707">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-708">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-709">Restrictedsiteszoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="589d8-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-710">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-711">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-712">Restrictedsiteszoneallowmetarefresh</span><span class="sxs-lookup"><span data-stu-id="589d8-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-713">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-714">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-715">Restrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-716">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-717">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-718">Restrictedsiteszonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-719">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-720">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-721">Restrictedsiteszonezuzugwonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="589d8-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-722">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-723">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-724">Restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-725">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-726">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-727">Restrictedsiteszoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="589d8-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-728">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-729">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-730">Restrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-731">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-732">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-733">Restrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-734">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-735">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-736">Restrictedsiteszoneallowupdatestostatobarviascript</span><span class="sxs-lookup"><span data-stu-id="589d8-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-737">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-738">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-739">Restrictedsiteszonezuzustandserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-740">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-741">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-742">Restrictedsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-743">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-744">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-745">Restrictedsiteszonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-746">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-747">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-748">Restrictedsiteszonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-749">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-750">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-751">Restrictedsiteszoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="589d8-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-752">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-753">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-754">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="589d8-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-755">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-756">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-757">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="589d8-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-758">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-759">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-760">Restrictedsiteszoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="589d8-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-761">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-762">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-763">Restrictedsiteszoneincluschocalpatheincluminguploadingfilestoserver</span><span class="sxs-lookup"><span data-stu-id="589d8-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-764">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-765">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-766">Restrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-767">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-768">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-769">Restrictedsiteszonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-770">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-771">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-772">Einschränktedsiteszonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="589d8-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-773">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-774">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-775">Restrictedsiteszonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="589d8-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-776">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-777">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-778">Restrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-779">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-780">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-781">Restrictedsiteszonumavigatewindowsandframesacrossdomains</span><span class="sxs-lookup"><span data-stu-id="589d8-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-782">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-783">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-784">Restrictedsiteszonerunactivexcontrolsandplugins</span><span class="sxs-lookup"><span data-stu-id="589d8-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-785">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-786">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-787">Restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="589d8-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-788">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-789">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-790">Restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting</span><span class="sxs-lookup"><span data-stu-id="589d8-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-791">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-792">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-793">Restrictedsiteszonescriptingof JavaApplets</span><span class="sxs-lookup"><span data-stu-id="589d8-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-794">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-795">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-796">Restrictedsiteszoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="589d8-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-797">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-798">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-799">Restrictedsiteszonzname der crosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="589d8-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-800">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-801">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-802">Restrictedsiteszuniturnonprotectedmode</span><span class="sxs-lookup"><span data-stu-id="589d8-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-803">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-804">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-805">Restrictedsiteszoneul Popupblocker</span><span class="sxs-lookup"><span data-stu-id="589d8-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-806">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-807">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-808">Restrictfiledownloadinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="589d8-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-809">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-810">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-811">Scriptedwindowsecurityrestrictionsinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="589d8-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-812">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-813">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-814">Searchproviderlist</span><span class="sxs-lookup"><span data-stu-id="589d8-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-815">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-816">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-817">Securityzonesuseonlymachinesettings</span><span class="sxs-lookup"><span data-stu-id="589d8-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-818">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-819">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-820">Specifyuseofaktivexinstallerservice</span><span class="sxs-lookup"><span data-stu-id="589d8-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-821">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-822">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-823">Treuhändsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="589d8-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-824">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-825">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-826">Treudsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-827">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-828">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-829">Treuhändsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-830">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-831">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-832">Treuhändsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="589d8-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-833">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-834">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-835">Treuhänder-siteszonezuzugssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="589d8-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-836">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-837">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-838">Treuhändsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="589d8-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-839">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-840">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-841">Treuhändsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="589d8-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-842">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-843">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-844">Treuhändsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="589d8-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-845">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-846">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-847">Treuhändsiteszonezuzugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="589d8-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-848">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-849">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-850">Treuhändsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-851">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-852">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-853">Treuhändsiteszonedontrunantimalwareprogramsagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-854">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-855">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-856">Treuhändsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="589d8-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-857">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-858">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-859">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedassafe</span><span class="sxs-lookup"><span data-stu-id="589d8-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-860">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-861">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="589d8-862">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="589d8-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-863">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-864">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-865">Treudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="589d8-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-866">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-867">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="589d8-868">Treuhändsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="589d8-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="589d8-869">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="589d8-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="589d8-870">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="589d8-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="589d8-871">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="589d8-871">Requirements</span></span>



| <span data-ttu-id="589d8-872">Anforderung</span><span class="sxs-lookup"><span data-stu-id="589d8-872">Requirement</span></span> | <span data-ttu-id="589d8-873">Wert</span><span class="sxs-lookup"><span data-stu-id="589d8-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589d8-874">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="589d8-874">Minimum supported client</span></span><br/> | <span data-ttu-id="589d8-875">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="589d8-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="589d8-876">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="589d8-876">Minimum supported server</span></span><br/> | <span data-ttu-id="589d8-877">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="589d8-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="589d8-878">Namespace</span><span class="sxs-lookup"><span data-stu-id="589d8-878">Namespace</span></span><br/>                | <span data-ttu-id="589d8-879">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="589d8-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="589d8-880">MOF</span><span class="sxs-lookup"><span data-stu-id="589d8-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="589d8-881"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="589d8-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="589d8-882">DLL</span><span class="sxs-lookup"><span data-stu-id="589d8-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="589d8-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="589d8-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

