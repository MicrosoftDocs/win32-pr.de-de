---
title: MDM_Policy_User_Result01_InternetExplorer02-Klasse
description: Die MDM- \_ Richtlinie \_ User \_ Result01 \_ InternetExplorer02-Klasse stellt die verfügbaren Internet Explorer-Richtlinien dar.
ms.assetid: efd999aa-4aa8-486d-82d4-20af7e2005fe
keywords:
- MDM_Policy_User_Result01_InternetExplorer02-Klasse
- MDM_Policy_User_Result01_InternetExplorer02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02.InstanceID
- MDM_Policy_User_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8693720c7a973cc6bc689abbf76a4674f185e23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475309"
---
# <a name="mdm_policy_user_result01_internetexplorer02-class"></a><span data-ttu-id="510da-105">MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ InternetExplorer02-Klasse</span><span class="sxs-lookup"><span data-stu-id="510da-105">MDM\_Policy\_User\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="510da-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="510da-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="510da-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="510da-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="510da-108">Die MDM- \_ Richtlinie \_ User \_ Result01 \_ InternetExplorer02-Klasse stellt die verfügbaren Internet Explorer-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="510da-108">The MDM\_Policy\_User\_Result01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="510da-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="510da-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="510da-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="510da-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="510da-111">Member</span><span class="sxs-lookup"><span data-stu-id="510da-111">Members</span></span>

<span data-ttu-id="510da-112">Die **\_ \_ Benutzer \_ Result01 \_ InternetExplorer02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="510da-112">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="510da-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="510da-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="510da-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="510da-114">Properties</span></span>

<span data-ttu-id="510da-115">Die **\_ \_ Benutzer \_ Result01 \_ InternetExplorer02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="510da-115">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="510da-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="510da-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-119">Allowactivexfiltering</span><span class="sxs-lookup"><span data-stu-id="510da-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-122">Allowaddonlist</span><span class="sxs-lookup"><span data-stu-id="510da-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-125">Allowautocomplete</span><span class="sxs-lookup"><span data-stu-id="510da-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-128">Allowcertificateaddressmismatchwarning</span><span class="sxs-lookup"><span data-stu-id="510da-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-131">Allowdelta etingbrowsinghistoryonexit</span><span class="sxs-lookup"><span data-stu-id="510da-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-134">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="510da-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-137">"Zuweisung von" "" "".</span><span class="sxs-lookup"><span data-stu-id="510da-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-140">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="510da-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="510da-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-146">"Expwinternetexplorerstandardsmode"</span><span class="sxs-lookup"><span data-stu-id="510da-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-149">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="510da-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-152">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="510da-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-155">Allowlocalmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-158">Allowlockeddowninternetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-161">Allowlockeddownintranetzonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-164">Allowlockeddownloader calmachinezonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-167">Allowlockeddownrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-170">' Zugwonewordentry '</span><span class="sxs-lookup"><span data-stu-id="510da-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-173">Allowsiteononezuzuzustandliste</span><span class="sxs-lookup"><span data-stu-id="510da-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-176">Allowslockeddowntreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-179">Allowsoftware\signatureisinvalid</span><span class="sxs-lookup"><span data-stu-id="510da-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-182">Allowsrestrictedsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-185">Allowvorschlags stedsites</span><span class="sxs-lookup"><span data-stu-id="510da-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-188">Allowtreuhändsiteszonetemplate</span><span class="sxs-lookup"><span data-stu-id="510da-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-191">Checkservercertificaterevozierung</span><span class="sxs-lookup"><span data-stu-id="510da-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-194">Checksignaturesondownloader-dprogramme</span><span class="sxs-lookup"><span data-stu-id="510da-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-196">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-197">"Konsistentmimehandlinginternetexplorerprocesses"</span><span class="sxs-lookup"><span data-stu-id="510da-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-200">Disableadobeflash</span><span class="sxs-lookup"><span data-stu-id="510da-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-203">Disableblockingof outdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-206">Disablebypassofsmartscreenwarning</span><span class="sxs-lookup"><span data-stu-id="510da-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-209">Disablebypassofsmartscreenwarningsaboutuncommonfiles</span><span class="sxs-lookup"><span data-stu-id="510da-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-212">Disableconfiguringhistory</span><span class="sxs-lookup"><span data-stu-id="510da-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-215">Disablecrash-Erkennung</span><span class="sxs-lookup"><span data-stu-id="510da-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-218">Disablecustomerexperiendceimprovementprogramparticipation</span><span class="sxs-lookup"><span data-stu-id="510da-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-221">Disabledelta etinguservisitedwebsites</span><span class="sxs-lookup"><span data-stu-id="510da-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-224">Disablereclosuredownload</span><span class="sxs-lookup"><span data-stu-id="510da-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-227">Disableverschlüsseltionsupport</span><span class="sxs-lookup"><span data-stu-id="510da-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="510da-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-233">Disableflipheadfeature</span><span class="sxs-lookup"><span data-stu-id="510da-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-236">Disablehomepagechange</span><span class="sxs-lookup"><span data-stu-id="510da-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-239">Disableignoringcertificateerrors</span><span class="sxs-lookup"><span data-stu-id="510da-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-242">Disableinprivatebrowsing</span><span class="sxs-lookup"><span data-stu-id="510da-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-245">Disableprocessesinenhancedprotectedmode</span><span class="sxs-lookup"><span data-stu-id="510da-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-248">Disableproxychange</span><span class="sxs-lookup"><span data-stu-id="510da-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-251">Disablesearchproviderchange</span><span class="sxs-lookup"><span data-stu-id="510da-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-254">Disablesecondaryhomepagechange</span><span class="sxs-lookup"><span data-stu-id="510da-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-257">Disablesecuritysettingscheck</span><span class="sxs-lookup"><span data-stu-id="510da-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-260">Donotallowactivexcontrolsinprotectedmode</span><span class="sxs-lookup"><span data-stu-id="510da-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-263">Donotblockoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-266">Donotblockoutdatedactivexcontrolsonspecificdomains</span><span class="sxs-lookup"><span data-stu-id="510da-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-269">Includezalllocalsites</span><span class="sxs-lookup"><span data-stu-id="510da-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-271">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-272">Includepallnetworkpath</span><span class="sxs-lookup"><span data-stu-id="510da-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-274">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="510da-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="510da-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="510da-278">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="510da-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-279">Internetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-281">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-282">Internetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-283">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-284">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-285">Internetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-287">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-288">Internetzoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="510da-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-290">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-291">Internetzoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="510da-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-293">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-294">Internetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-296">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-297">Internetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-299">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-300">Internetzoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="510da-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-302">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-303">Internetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-305">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-306">Internetzonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-308">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-309">Internetzonezugewonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="510da-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-311">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-312">Internetzoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="510da-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-314">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-315">Internetzoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="510da-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-317">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-318">Internetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-320">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-321">Internetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-322">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-323">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-324">Internetzoneallowupdatestostatus barviascript</span><span class="sxs-lookup"><span data-stu-id="510da-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-326">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-327">Internetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-329">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-330">Internetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-332">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-333">Internetzonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-334">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-335">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-336">Internetzonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-338">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-339">Internetzoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="510da-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-341">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-342">Internetzoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="510da-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-344">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-345">Internetzoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="510da-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-347">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-348">Internetzoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="510da-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-350">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-351">Internetzoneenableprotectedmode</span><span class="sxs-lookup"><span data-stu-id="510da-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-353">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-354">Internetzoneincludelta Update Server-Datei</span><span class="sxs-lookup"><span data-stu-id="510da-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-356">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-357">Internetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-358">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-359">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-360">Internetzonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-362">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-363">Internetzonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="510da-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-365">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-366">Internetzonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="510da-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-367">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-368">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-369">Internetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-370">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-371">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-372">Internetzonerunnetframeworkreliantcomponentsnotsignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="510da-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-373">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-374">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-375">Internetzonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="510da-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-377">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-378">Internetzoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="510da-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-380">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-381">Internetzoneuonpopupblocker</span><span class="sxs-lookup"><span data-stu-id="510da-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-383">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-384">Internetzonewebsitesinlessprivilegedzonescannavigateinonthiszone</span><span class="sxs-lookup"><span data-stu-id="510da-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-385">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-386">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-387">Intranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-389">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-390">Intranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-391">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-392">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-393">Intranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-394">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-395">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-396">Intranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-397">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-398">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-399">Intranetzonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-400">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-401">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-402">Intranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-403">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-404">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-405">Intranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-407">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-408">Intranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-409">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-410">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-411">Intranetzonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-412">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-413">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-414">Intranetzonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-416">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-417">Intranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-419">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-420">Intranetzoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="510da-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-421">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-422">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-423">Intranetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-425">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-426">Intranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-428">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-429">Localmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-431">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-432">Localmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-433">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-434">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-435">Localmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-437">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-438">Localmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-440">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-441">Localmachinezonezuweisung-ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-442">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-443">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-444">Localmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-446">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-447">Localmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-448">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-449">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-450">Localmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-451">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-452">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-453">Localmachinezonezugewiesene wuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-454">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-455">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-456">Localmachinezonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-457">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-458">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-459">Localmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-460">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-461">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-462">Localmachinezonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-463">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-464">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-465">Localmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-466">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-467">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-468">Lockeddowninternetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-469">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-470">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-471">Lockeddowninternetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-472">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-473">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-474">Lockeddowninternetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-475">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-476">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-477">Lockeddowninternetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-478">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-479">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-480">Lockeddowninternetzonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="510da-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-482">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-483">Lockeddowninternetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-484">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-485">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-486">Lockeddowninternetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-488">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-489">Lockeddowninternetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-490">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-491">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-492">Lockeddowninternetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-493">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-494">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-495">Lockeddowninternetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-496">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-497">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-498">Lockeddowninternetzonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-499">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-500">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-501">Lockeddowninternetzonendavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-502">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-503">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-504">Lockeddownintranetzoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-505">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-506">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-507">Lockeddownintranetzoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-508">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-509">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-510">Lockeddownintranetzoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-511">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-512">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-513">Lockeddownintranetzoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-514">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-515">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-516">Lockeddownintranetzonezuden ssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-517">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-518">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-519">Lockeddownintranetzoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-520">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-521">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-522">Lockeddownintranetzoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-524">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-525">Lockeddownintranetzoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-526">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-527">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-528">Lockeddownintranetzonezuzuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-529">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-530">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-531">Lockeddownintranetzoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-532">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-533">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-534">Lockeddownintranetzoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-535">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-536">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-537">Lockeddownloader calmachinezoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-538">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-539">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-540">Lockeddownloader calmachinezoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-541">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-542">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-543">Lockeddownloader calmachinezoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-544">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-545">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-546">Lockeddownloader calmachinezoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-547">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-548">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-549">Lockeddownloader calmachinezonezuzugessprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-550">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-551">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-552">Lockeddownloader calmachinezoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-553">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-554">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-555">Lockeddownloader calmachinezoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-556">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-557">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-558">Lockeddownloader calmachinezoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-559">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-560">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-561">Lockeddownloader calmachinezonezuzugegenserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-562">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-563">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-564">Lockeddownloader calmachinezoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-565">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-566">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-567">Lockeddownloader calmachinezonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-568">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-569">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-570">Lockeddownloader calmachinezonesavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-571">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-572">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-573">Lockeddownrestrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-574">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-575">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-576">Lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-577">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-578">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-579">Lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-580">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-581">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-582">Lockeddownrestrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-583">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-584">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-585">Lockeddownrestrictedsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-586">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-587">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-588">Lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-589">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-590">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-591">Lockeddownrestrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-592">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-593">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-594">Lockeddownrestrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-595">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-596">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-597">Lockeddownrestrictedsiteszonezuzustuserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-598">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-599">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-600">Lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-601">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-602">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-603">Lockeddownrestrictedsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-604">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-605">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-606">Lockeddownrestrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-607">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-608">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-609">Lockeddowntreuhänder dsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-610">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-611">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-612">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-613">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-614">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-615">Lockeddowntreuhänder dsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-616">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-617">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-618">Lockeddowntreuhänder dsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-619">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-620">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-621">Lockeddowntreuhänder dsiteszonezuzussprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-622">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-623">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-624">Lockeddowntreuhänder dsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-625">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-626">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-627">Lockeddowntreuhänder dsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-628">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-629">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-630">Lockeddowntreuhänder dsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-631">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-632">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-633">Lockeddowntreuhänder dsiteszonezugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-634">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-635">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-636">Lockeddowntreuhänder dsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-637">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-638">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-639">Lockeddowntreudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-640">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-641">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-642">Lockeddowntreuhänder dsiteszoneinavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-643">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-644">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-645">Mimesniffingsafetyfeatureinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="510da-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-646">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-647">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-648">Mkprotocolsecurityrestrictioninternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="510da-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-649">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-650">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-651">Notificationbarinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="510da-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-652">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-653">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="510da-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-655">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-656">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="510da-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="510da-657">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="510da-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-658">Preventmanagingsmartscreenfilter</span><span class="sxs-lookup"><span data-stu-id="510da-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-659">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-660">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-661">Preventperuserinstallationofaktivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-662">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-663">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-664">Schutzfromzoneelevationinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="510da-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-665">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-666">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-667">Removerunthistimebuttonforoutdatedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-668">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-669">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-670">Restrictactivexinstallinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="510da-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-671">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-672">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-673">Restrictedsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-674">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-675">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-676">Restrictedsiteszoneallowactivescripting</span><span class="sxs-lookup"><span data-stu-id="510da-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-677">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-678">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-679">Restrictedsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-680">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-681">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-682">Restrictedsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-683">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-684">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-685">Restrictedsiteszoneallowbinaryandscriptverhaltensweisen</span><span class="sxs-lookup"><span data-stu-id="510da-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-686">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-687">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-688">Restrictedsiteszoneallowcopypasteviascript</span><span class="sxs-lookup"><span data-stu-id="510da-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-689">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-690">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-691">Restrictedsiteszoneallowdraganddropcopyandpastefiles</span><span class="sxs-lookup"><span data-stu-id="510da-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-692">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-693">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-694">Restrictedsiteszoneallowfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-695">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-696">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-697">Restrictedsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-698">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-699">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-700">Restrictedsiteszonezuzuweisung</span><span class="sxs-lookup"><span data-stu-id="510da-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-701">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-702">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-703">Restrictedsiteszoneallowloadingofxamlfiles</span><span class="sxs-lookup"><span data-stu-id="510da-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-704">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-705">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-706">Restrictedsiteszoneallowmetarefresh</span><span class="sxs-lookup"><span data-stu-id="510da-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-707">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-708">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-709">Restrictedsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-710">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-711">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-712">Restrictedsiteszonezuweiwonlyapproveddomainstoulactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-713">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-714">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-715">Restrictedsiteszonezuzugwonlyapproveddomainstousetdcactivexcontrol</span><span class="sxs-lookup"><span data-stu-id="510da-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-716">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-717">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-718">Restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols</span><span class="sxs-lookup"><span data-stu-id="510da-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-719">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-720">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-721">Restrictedsiteszoneallowscriptinitiatedwindows</span><span class="sxs-lookup"><span data-stu-id="510da-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-722">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-723">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-724">Restrictedsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-725">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-726">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-727">Restrictedsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-728">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-729">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-730">Restrictedsiteszoneallowupdatestostatobarviascript</span><span class="sxs-lookup"><span data-stu-id="510da-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-731">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-732">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-733">Restrictedsiteszonezuzustandserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-734">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-735">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-736">Restrictedsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-737">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-738">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-739">Restrictedsiteszonedownloadsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-740">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-741">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-742">Restrictedsiteszonedownloadunsignedactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-743">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-744">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-745">Restrictedsiteszoneenablecrosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="510da-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-746">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-747">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-748">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainsacrosswindows</span><span class="sxs-lookup"><span data-stu-id="510da-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-749">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-750">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-751">Restrictedsiteszoneenabledraggingof contentfromdifferenentdomainswithinwindows</span><span class="sxs-lookup"><span data-stu-id="510da-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-752">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-753">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-754">Restrictedsiteszoneenablemimesniffing</span><span class="sxs-lookup"><span data-stu-id="510da-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-755">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-756">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-757">Restrictedsiteszoneincluschocalpatheincluminguploadingfilestoserver</span><span class="sxs-lookup"><span data-stu-id="510da-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-758">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-759">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-760">Restrictedsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-761">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-762">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-763">Restrictedsiteszonejavaberechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-764">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-765">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-766">Einschränktedsiteszonelaunchingapplicationsandfilesiniframe</span><span class="sxs-lookup"><span data-stu-id="510da-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-767">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-768">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-769">Restrictedsiteszonelogonoptions</span><span class="sxs-lookup"><span data-stu-id="510da-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-770">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-771">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-772">Restrictedsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-773">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-774">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-775">Restrictedsiteszonumavigatewindowsandframesacrossdomains</span><span class="sxs-lookup"><span data-stu-id="510da-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-776">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-777">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-778">Restrictedsiteszonerunactivexcontrolsandplugins</span><span class="sxs-lookup"><span data-stu-id="510da-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-779">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-780">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-781">Restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode</span><span class="sxs-lookup"><span data-stu-id="510da-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-782">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-783">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-784">Restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting</span><span class="sxs-lookup"><span data-stu-id="510da-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-785">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-786">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-787">Restrictedsiteszonescriptingof JavaApplets</span><span class="sxs-lookup"><span data-stu-id="510da-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-788">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-789">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-790">Restrictedsiteszoneshowsecuritywarningforpotenallyunsafefiles</span><span class="sxs-lookup"><span data-stu-id="510da-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-791">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-792">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-793">Restrictedsiteszonzname der crosssitescriptingfilter</span><span class="sxs-lookup"><span data-stu-id="510da-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-794">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-795">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-796">Restrictedsiteszuniturnonprotectedmode</span><span class="sxs-lookup"><span data-stu-id="510da-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-797">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-798">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-799">Restrictedsiteszoneul Popupblocker</span><span class="sxs-lookup"><span data-stu-id="510da-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-800">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-801">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-802">Restrictfiledownloadinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="510da-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-803">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-804">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-805">Scriptedwindowsecurityrestrictionsinternetexplorerprocesses</span><span class="sxs-lookup"><span data-stu-id="510da-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-806">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-807">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-808">Searchproviderlist</span><span class="sxs-lookup"><span data-stu-id="510da-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-809">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-810">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-811">Specifyuseofaktivexinstallerservice</span><span class="sxs-lookup"><span data-stu-id="510da-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-812">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-813">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-814">Treuhändsiteszoneallowaccesstodatasources</span><span class="sxs-lookup"><span data-stu-id="510da-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-815">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-816">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-817">Treudsiteszoneallowautomaticpromptingforactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-818">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-819">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-820">Treuhändsiteszoneallowautomaticpromptingforfiledownloads</span><span class="sxs-lookup"><span data-stu-id="510da-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-821">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-822">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-823">Treuhändsiteszoneallowfontdownloads</span><span class="sxs-lookup"><span data-stu-id="510da-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-824">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-825">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-826">Treuhänder-siteszonezuzugssprivilegedsites</span><span class="sxs-lookup"><span data-stu-id="510da-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-827">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-828">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-829">Treuhändsiteszoneallownetframeworkreliantcomponents</span><span class="sxs-lookup"><span data-stu-id="510da-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-830">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-831">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-832">Treuhändsiteszoneallowscriptlets</span><span class="sxs-lookup"><span data-stu-id="510da-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-833">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-834">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-835">Treuhändsiteszoneallowsmartscreenie</span><span class="sxs-lookup"><span data-stu-id="510da-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-836">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-837">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-838">Treuhändsiteszonezuzugserdatapersistenz</span><span class="sxs-lookup"><span data-stu-id="510da-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-839">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-840">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-841">Treuhändsiteszonedonotrunantimalwareagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-842">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-843">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-844">Treuhändsiteszonedontrunantimalwareprogramsagainstactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-845">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-846">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-847">Treuhändsiteszoneinitializeandscriptactivexcontrols</span><span class="sxs-lookup"><span data-stu-id="510da-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-848">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-849">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-850">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedassafe</span><span class="sxs-lookup"><span data-stu-id="510da-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-851">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-852">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="510da-853">Treuhändsiteszoneinitializeandscriptactivexcontrolsnotmarkedsafe</span><span class="sxs-lookup"><span data-stu-id="510da-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-854">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-855">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-856">Treudsiteszonejava-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="510da-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-857">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-858">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="510da-859">Treuhändsiteszonumavigatewindowsandframes</span><span class="sxs-lookup"><span data-stu-id="510da-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="510da-860">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="510da-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="510da-861">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="510da-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="510da-862">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="510da-862">Requirements</span></span>



| <span data-ttu-id="510da-863">Anforderung</span><span class="sxs-lookup"><span data-stu-id="510da-863">Requirement</span></span> | <span data-ttu-id="510da-864">Wert</span><span class="sxs-lookup"><span data-stu-id="510da-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="510da-865">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="510da-865">Minimum supported client</span></span><br/> | <span data-ttu-id="510da-866">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="510da-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="510da-867">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="510da-867">Minimum supported server</span></span><br/> | <span data-ttu-id="510da-868">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="510da-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="510da-869">Namespace</span><span class="sxs-lookup"><span data-stu-id="510da-869">Namespace</span></span><br/>                | <span data-ttu-id="510da-870">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="510da-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="510da-871">MOF</span><span class="sxs-lookup"><span data-stu-id="510da-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="510da-872"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="510da-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="510da-873">DLL</span><span class="sxs-lookup"><span data-stu-id="510da-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="510da-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="510da-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

