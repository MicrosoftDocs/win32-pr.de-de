---
title: MDM_Policy_Result01_LocalPoliciesSecurityOptions02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ LocalPoliciesSecurityOptions02-Klasse stellt die Sicherheitsoptionen für lokale Richtlinien dar.
ms.assetid: 75ac4789-781f-4722-8b0a-33e53b307296
keywords:
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02-Klasse
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ece3790bf5a6a6ac51310d04661366bbe9e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040492"
---
# <a name="mdm_policy_result01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="bc3bd-105">MDM- \_ Richtlinie \_ Result01 \_ LocalPoliciesSecurityOptions02-Klasse</span><span class="sxs-lookup"><span data-stu-id="bc3bd-105">MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="bc3bd-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc3bd-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="bc3bd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc3bd-108">Die MDM- \_ Richtlinie \_ Result01 \_ LocalPoliciesSecurityOptions02-Klasse stellt die Sicherheitsoptionen für lokale Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-108">The MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class represents the local policies security options.</span></span>

<span data-ttu-id="bc3bd-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3bd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc3bd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LocalPoliciesSecurityOptions02
{
  string InstanceID;
  string ParentID;
  sint32 Accounts_BlockMicrosoftAccounts;
  sint32 Accounts_EnableGuestAccountStatus;
  sint32 Accounts_EnableAdministratorAccountStatus;
  sint32 Accounts_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly;
  string Accounts_RenameAdministratorAccount;
  string Accounts_RenameGuestAccount;
  string Devices_RestrictCDROMAccessToLocallyLoggedOnUserOnly;
  sint32 Devices_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters;
  sint32 Devices_AllowUndockWithoutHavingToLogon;
  string Devices_AllowedToFormatAndEjectRemovableMedia;
  sint32 InteractiveLogon_DisplayUserInformationWhenTheSessionIsLocked;
  sint32 Interactivelogon_DoNotDisplayLastSignedIn;
  sint32 Interactivelogon_DoNotDisplayUsernameAtSignIn;
  sint32 Interactivelogon_DoNotRequireCTRLALTDEL;
  sint32 InteractiveLogon_MachineInactivityLimit;
  string InteractiveLogon_MessageTextForUsersAttemptingToLogOn;
  string InteractiveLogon_MessageTitleForUsersAttemptingToLogOn;
  sint32 NetworkAccess_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares;
  sint32 NetworkAccess_RestrictAnonymousAccessToNamedPipesAndShares;
  string NetworkAccess_RestrictClientsAllowedToMakeRemoteCallsToSAM;
  sint32 NetworkSecurity_AllowPKU2UAuthenticationRequests;
  sint32 RecoveryConsole_AllowAutomaticAdministrativeLogon;
  sint32 Shutdown_AllowSystemToBeShutDownWithoutHavingToLogOn;
  sint32 Shutdown_ClearVirtualMemoryPageFile;
  sint32 UserAccountControl_AllowUIAccessApplicationsToPromptForElevation;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForAdministrators;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForStandardUsers;
  sint32 UserAccountControl_DetectApplicationInstallationsAndPromptForElevation;
  sint32 UserAccountControl_OnlyElevateExecutableFilesThatAreSignedAndValidated;
  sint32 UserAccountControl_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations;
  sint32 UserAccountControl_RunAllAdministratorsInAdminApprovalMode;
  sint32 UserAccountControl_SwitchToTheSecureDesktopWhenPromptingForElevation;
  sint32 UserAccountControl_UseAdminApprovalMode;
  sint32 UserAccountControl_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations;
};
```

## <a name="members"></a><span data-ttu-id="bc3bd-111">Member</span><span class="sxs-lookup"><span data-stu-id="bc3bd-111">Members</span></span>

<span data-ttu-id="bc3bd-112">Die **MDM- \_ Richtlinie \_ Result01 \_ LocalPoliciesSecurityOptions02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bc3bd-112">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="bc3bd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc3bd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc3bd-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc3bd-114">Properties</span></span>

<span data-ttu-id="bc3bd-115">Die **MDM- \_ Richtlinie \_ Result01 \_ LocalPoliciesSecurityOptions02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-115">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bc3bd-116">Konten \_ blockmicrosoftaccounts</span><span class="sxs-lookup"><span data-stu-id="bc3bd-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc3bd-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="bc3bd-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc3bd-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="bc3bd-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-125">Konten \_ limitlocalaccountuseofblankpasswordstoconsolelogononly</span><span class="sxs-lookup"><span data-stu-id="bc3bd-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-128">Konten \_ RenameAdministratorAccount</span><span class="sxs-lookup"><span data-stu-id="bc3bd-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-131">Konten \_ renameguestaccount</span><span class="sxs-lookup"><span data-stu-id="bc3bd-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-134">Geräte "- \_ Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="bc3bd-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-137">Geräte " \_ zugewundockwithouthavingtologon"</span><span class="sxs-lookup"><span data-stu-id="bc3bd-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-140">Geräte \_ preventusersfrominstallingprinterdrivers\connectingdesharedprinter</span><span class="sxs-lookup"><span data-stu-id="bc3bd-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-143">Geräte \_ restrictcdromaccesstolocallyloggedonuseronly</span><span class="sxs-lookup"><span data-stu-id="bc3bd-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc3bd-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bc3bd-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-149">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc3bd-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-150">Interactivelogon \_ displayuserinformationwhenthesessionislock</span><span class="sxs-lookup"><span data-stu-id="bc3bd-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-151">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-153">Interactivelogon \_ donotdisplaylastsignetdin</span><span class="sxs-lookup"><span data-stu-id="bc3bd-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-154">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-156">Interactivelogon \_ donotdisplayusernameatsignin</span><span class="sxs-lookup"><span data-stu-id="bc3bd-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-157">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-159">Interactivelogon \_ donotrequirectrlaltdel</span><span class="sxs-lookup"><span data-stu-id="bc3bd-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-160">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-161">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-162">Interactivelogon \_ machineinactivitylimit</span><span class="sxs-lookup"><span data-stu-id="bc3bd-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-163">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-165">Interactivelogon \_ messagetextforusersattemptingtologon</span><span class="sxs-lookup"><span data-stu-id="bc3bd-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-167">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-168">Interactivelogon \_ messagetitleforusersattemptingtologon</span><span class="sxs-lookup"><span data-stu-id="bc3bd-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-171">Network Access \_ donotallowanonymousenproerationofsamaccountsandshares</span><span class="sxs-lookup"><span data-stu-id="bc3bd-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-172">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-174">Network Access \_ restrictanonymousaccesstonamedpipesandshares</span><span class="sxs-lookup"><span data-stu-id="bc3bd-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-175">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-176">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-177">Network Access \_ restrictclientsallowedtomakeremotecallstosam</span><span class="sxs-lookup"><span data-stu-id="bc3bd-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-179">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-180">Network Security \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="bc3bd-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-181">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-182">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc3bd-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bc3bd-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-186">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc3bd-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-187">Wiederherstellbarkeits Konsole \_ allowautomaticadministrativelogon</span><span class="sxs-lookup"><span data-stu-id="bc3bd-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-188">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-189">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-190">\_Allowsystempobeshutdownwithouthavingtologon Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="bc3bd-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-191">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-193">\_Clearvirtualmemorypagefile Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="bc3bd-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-194">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-195">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-196">UserAccountControl \_ zusicherungs-ID-Objekt</span><span class="sxs-lookup"><span data-stu-id="bc3bd-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-197">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-198">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-199">UserAccountControl \_ verhaltoferelevationpromptforadministrators</span><span class="sxs-lookup"><span data-stu-id="bc3bd-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-200">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-201">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-202">UserAccountControl \_ verhaltoferelevationpromptforstandardusers</span><span class="sxs-lookup"><span data-stu-id="bc3bd-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-203">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-204">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-205">UserAccountControl \_ detectapplicationinstallationsandpromptforelevation</span><span class="sxs-lookup"><span data-stu-id="bc3bd-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-206">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-207">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-208">UserAccountControl \_ onlyelevateexecutablefilesthataresignedandvalidieren</span><span class="sxs-lookup"><span data-stu-id="bc3bd-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-209">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-210">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-211">UserAccountControl \_ onlyelevateuiaccessapplicationsthatareinstalledinsecuumumsetzungen</span><span class="sxs-lookup"><span data-stu-id="bc3bd-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-212">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-213">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-214">UserAccountControl \_ RunAllAdministratorsInAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="bc3bd-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-215">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-216">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-217">UserAccountControl \_ switchtothesecuredesktop\promptingforelevation</span><span class="sxs-lookup"><span data-stu-id="bc3bd-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-218">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-219">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-220">UserAccountControl \_ useadminapprovalmode</span><span class="sxs-lookup"><span data-stu-id="bc3bd-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-221">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-222">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3bd-223">UserAccountControl \_ virtualizefileandregistryschreitefailurestoperuserlocations</span><span class="sxs-lookup"><span data-stu-id="bc3bd-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3bd-224">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3bd-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3bd-225">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bc3bd-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc3bd-226">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc3bd-226">Requirements</span></span>



| <span data-ttu-id="bc3bd-227">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc3bd-227">Requirement</span></span> | <span data-ttu-id="bc3bd-228">Wert</span><span class="sxs-lookup"><span data-stu-id="bc3bd-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3bd-229">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc3bd-229">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3bd-230">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc3bd-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc3bd-231">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc3bd-231">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3bd-232">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc3bd-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bc3bd-233">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc3bd-233">Namespace</span></span><br/>                | <span data-ttu-id="bc3bd-234">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bc3bd-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bc3bd-235">MOF</span><span class="sxs-lookup"><span data-stu-id="bc3bd-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc3bd-236"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bc3bd-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc3bd-237">DLL</span><span class="sxs-lookup"><span data-stu-id="bc3bd-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc3bd-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc3bd-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

