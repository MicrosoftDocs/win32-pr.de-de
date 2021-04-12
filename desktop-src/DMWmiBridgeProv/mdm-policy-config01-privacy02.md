---
title: MDM_Policy_Config01_Privacy02-Klasse
description: Die Config01 Privacy02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Such Richtlinien dar.
ms.assetid: 202213b9-5301-4c55-bbc6-6ce3daf705ad
keywords:
- MDM_Policy_Config01_Privacy02-Klasse
- MDM_Policy_Config01_Privacy02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Privacy02
- MDM_Policy_Config01_Privacy02.InstanceID
- MDM_Policy_Config01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca714dc17db60982e5ba047690886bc88aa79853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956447"
---
# <a name="mdm_policy_config01_privacy02-class"></a><span data-ttu-id="b2d83-105">MDM- \_ Richtlinie \_ Config01 \_ Privacy02-Klasse</span><span class="sxs-lookup"><span data-stu-id="b2d83-105">MDM\_Policy\_Config01\_Privacy02 class</span></span>

<span data-ttu-id="b2d83-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b2d83-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b2d83-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b2d83-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b2d83-108">Die **\_ \_ Config01 \_ Privacy02-Klasse der MDM-Richtlinie** stellt die verfügbaren Such Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="b2d83-108">The **MDM\_Policy\_Config01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="b2d83-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b2d83-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d83-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2d83-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Privacy02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAutoAcceptPairingAndPrivacyConsentPrompts;
  sint32 AllowInputPersonalization;
  string LetAppsSyncWithDevices_UserInControlOfTheseApps;
  sint32 PublishUserActivities;
  string LetAppsSyncWithDevices_ForceDenyTheseApps;
  string LetAppsSyncWithDevices_ForceAllowTheseApps;
  sint32 LetAppsSyncWithDevices;
  string LetAppsAccessTrustedDevices_UserInControlOfTheseApps;
  string LetAppsRunInBackground_UserInControlOfTheseApps;
  string LetAppsRunInBackground_ForceDenyTheseApps;
  string LetAppsRunInBackground_ForceAllowTheseApps;
  sint32 LetAppsRunInBackground;
  string LetAppsGetDiagnosticInfo_UserInControlOfTheseApps;
  string LetAppsGetDiagnosticInfo_ForceDenyTheseApps;
  string LetAppsGetDiagnosticInfo_ForceAllowTheseApps;
  sint32 LetAppsGetDiagnosticInfo;
  string LetAppsAccessTrustedDevices_ForceDenyTheseApps;
  string LetAppsAccessTrustedDevices_ForceAllowTheseApps;
  sint32 LetAppsAccessTrustedDevices;
  string LetAppsAccessRadios_UserInControlOfTheseApps;
  string LetAppsAccessTasks_UserInControlOfTheseApps;
  string LetAppsAccessTasks_ForceDenyTheseApps;
  string LetAppsAccessTasks_ForceAllowTheseApps;
  sint32 LetAppsAccessTasks;
  string LetAppsAccessRadios_ForceDenyTheseApps;
  string LetAppsAccessRadios_ForceAllowTheseApps;
  sint32 LetAppsAccessRadios;
  string LetAppsAccessPhone_UserInControlOfTheseApps;
  string LetAppsAccessPhone_ForceDenyTheseApps;
  string LetAppsAccessPhone_ForceAllowTheseApps;
  sint32 LetAppsAccessPhone;
  string LetAppsAccessMotion_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_ForceDenyTheseApps;
  string LetAppsAccessNotifications_ForceAllowTheseApps;
  sint32 LetAppsAccessNotifications;
  string LetAppsAccessMotion_ForceDenyTheseApps;
  string LetAppsAccessMotion_ForceAllowTheseApps;
  sint32 LetAppsAccessMotion;
  string LetAppsAccessMicrophone_UserInControlOfTheseApps;
  string LetAppsAccessMicrophone_ForceDenyTheseApps;
  string LetAppsAccessMicrophone_ForceAllowTheseApps;
  sint32 LetAppsAccessMicrophone;
  string LetAppsAccessMessaging_UserInControlOfTheseApps;
  string LetAppsAccessMessaging_ForceDenyTheseApps;
  string LetAppsAccessMessaging_ForceAllowTheseApps;
  sint32 LetAppsAccessMessaging;
  string LetAppsAccessLocation_UserInControlOfTheseApps;
  string LetAppsAccessLocation_ForceDenyTheseApps;
  string LetAppsAccessLocation_ForceAllowTheseApps;
  sint32 LetAppsAccessLocation;
  string LetAppsAccessEmail_UserInControlOfTheseApps;
  string LetAppsAccessEmail_ForceDenyTheseApps;
  string LetAppsAccessEmail_ForceAllowTheseApps;
  sint32 LetAppsAccessEmail;
  string LetAppsAccessContacts_UserInControlOfTheseApps;
  string LetAppsAccessContacts_ForceDenyTheseApps;
  string LetAppsAccessContacts_ForceAllowTheseApps;
  sint32 LetAppsAccessContacts;
  string LetAppsAccessCamera_UserInControlOfTheseApps;
  string LetAppsAccessCamera_ForceDenyTheseApps;
  string LetAppsAccessCamera_ForceAllowTheseApps;
  sint32 LetAppsAccessCamera;
  string LetAppsAccessCallHistory_UserInControlOfTheseApps;
  string LetAppsAccessCallHistory_ForceDenyTheseApps;
  string LetAppsAccessCallHistory_ForceAllowTheseApps;
  sint32 LetAppsAccessCallHistory;
  string LetAppsAccessCalendar_UserInControlOfTheseApps;
  string LetAppsAccessCalendar_ForceDenyTheseApps;
  string LetAppsAccessCalendar_ForceAllowTheseApps;
  sint32 LetAppsAccessCalendar;
  string LetAppsAccessAccountInfo_UserInControlOfTheseApps;
  string LetAppsAccessAccountInfo_ForceDenyTheseApps;
  string LetAppsAccessAccountInfo_ForceAllowTheseApps;
  sint32 LetAppsAccessAccountInfo;
  sint32 DisableAdvertisingId;
  sint32 EnableActivityFeed;
};
```

## <a name="members"></a><span data-ttu-id="b2d83-111">Member</span><span class="sxs-lookup"><span data-stu-id="b2d83-111">Members</span></span>

<span data-ttu-id="b2d83-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Privacy02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b2d83-112">The **MDM\_Policy\_Config01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="b2d83-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d83-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2d83-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2d83-114">Properties</span></span>

<span data-ttu-id="b2d83-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Privacy02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2d83-115">The **MDM\_Policy\_Config01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b2d83-116">Allowautoaccept tpuningandprivacyzustimmung</span><span class="sxs-lookup"><span data-stu-id="b2d83-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-119">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="b2d83-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-122">Disablewerbung</span><span class="sxs-lookup"><span data-stu-id="b2d83-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-125">Enableactivityfeed</span><span class="sxs-lookup"><span data-stu-id="b2d83-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b2d83-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b2d83-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2d83-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2d83-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2d83-132">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="b2d83-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="b2d83-133">Für diese Klasse ist die Zeichenfolge "Privacy".</span><span class="sxs-lookup"><span data-stu-id="b2d83-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="b2d83-134">Letappsaccessaccountinfo</span><span class="sxs-lookup"><span data-stu-id="b2d83-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-137">Letappsaccessaccountinfo \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-140">Letappsaccessaccountinfo \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-143">Letappsaccessaccountinfo \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-146">Letappsaccesscalendar</span><span class="sxs-lookup"><span data-stu-id="b2d83-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-149">Letappsaccesscalendar \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-152">Letappsaccesscalendar \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-155">Letappsaccesscalendar \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-158">Letappsaccesscallhistory</span><span class="sxs-lookup"><span data-stu-id="b2d83-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-161">Letappsaccesscallhistory \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-164">Letappsaccesscallhistory \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-167">Letappsaccesscallhistory \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-170">Letappsaccesscamera</span><span class="sxs-lookup"><span data-stu-id="b2d83-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-173">Letappsaccesscamera \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-176">Letappsaccesscamera \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-179">Letappsaccesscamera \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-182">Letappsaccesscontacts</span><span class="sxs-lookup"><span data-stu-id="b2d83-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-185">Letappsaccesscontacts \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-188">Letappsaccesscontacts \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-191">Letappsaccesscontacts \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-194">Letappsacceslmail</span><span class="sxs-lookup"><span data-stu-id="b2d83-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-195">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-196">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-197">Letappsacceslmail \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-200">Letappsacceslmail \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-203">Letappsacceslmail \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-206">Letappsaccesslocation</span><span class="sxs-lookup"><span data-stu-id="b2d83-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-209">Letappsaccesslocation \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-212">Letappsaccesslocation \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-215">Letappsaccesslocation \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-218">Letappsaccessmessaging</span><span class="sxs-lookup"><span data-stu-id="b2d83-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-219">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-221">Letappsaccessmessaging \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-224">Letappsaccessmessaging \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-227">Letappsaccessmessaging \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-230">Letappsaccessmikrofon</span><span class="sxs-lookup"><span data-stu-id="b2d83-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-231">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-233">Letappsaccessmikrofon \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-236">Letappsaccessmikrofon \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-239">Letappsaccessmikrofon \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-242">Letappsaccessmotion</span><span class="sxs-lookup"><span data-stu-id="b2d83-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-243">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-245">Letappsaccessmotion \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-248">Letappsaccessmotion \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-251">Letappsaccessmotion \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-254">Letappsaccessbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b2d83-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-255">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-257">Letappsaccessbenachrichtigungen \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-260">Letappsaccessbenachrichtigungen \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-263">Letappsaccessbenachrichtigungen \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-266">Letappsaccessphone</span><span class="sxs-lookup"><span data-stu-id="b2d83-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-267">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-269">Letappsaccessphone \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-271">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-272">Letappsaccessphone \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-274">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-275">Letappsaccessphone \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-277">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-278">Letappsaccessradios</span><span class="sxs-lookup"><span data-stu-id="b2d83-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-279">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-280">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-281">Letappsaccessradios \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-283">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-284">Letappsaccessradios \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-286">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-287">Letappsaccessradios \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-289">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-290">Letappsaccesstasks</span><span class="sxs-lookup"><span data-stu-id="b2d83-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-291">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-292">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-293">Letappsaccesstasks \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-295">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-296">Letappsaccesstasks \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-298">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-299">Letappsaccesstasks \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-301">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-302">Letappsaccesstrusteddevices</span><span class="sxs-lookup"><span data-stu-id="b2d83-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-303">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-304">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-305">Letappsaccesstrusteddevices \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-307">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-308">Letappsaccesstrusteddevices \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-310">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-311">Letappsaccesstrusteddevices \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-313">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-314">Letappsgetdiagnosticinfo</span><span class="sxs-lookup"><span data-stu-id="b2d83-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-315">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-316">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-317">Letappsgetdiagnosticinfo \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-319">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-320">Letappsgetdiagnosticinfo \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-322">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-323">Letappsgetdiagnosticinfo \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-325">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-326">Letappsruninbackground</span><span class="sxs-lookup"><span data-stu-id="b2d83-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-327">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-328">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-329">Letappsruninbackground \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-331">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-332">Letappsruninbackground \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-334">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-335">Letappsruninbackground \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-337">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-338">Letappssyncwithdevices</span><span class="sxs-lookup"><span data-stu-id="b2d83-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-339">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-340">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-341">Letappssyncwithdevices \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-343">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-344">Letappssyncwithdevices \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-346">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b2d83-347">Letappssyncwithdevices \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="b2d83-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-349">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b2d83-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b2d83-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-351">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b2d83-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b2d83-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-353">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2d83-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2d83-354">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="b2d83-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="b2d83-355">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="b2d83-355">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="b2d83-356">Publishuseractivities</span><span class="sxs-lookup"><span data-stu-id="b2d83-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d83-357">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b2d83-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2d83-358">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b2d83-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2d83-359">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2d83-359">Requirements</span></span>



| <span data-ttu-id="b2d83-360">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2d83-360">Requirement</span></span> | <span data-ttu-id="b2d83-361">Wert</span><span class="sxs-lookup"><span data-stu-id="b2d83-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d83-362">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2d83-362">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d83-363">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2d83-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2d83-364">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2d83-364">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d83-365">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b2d83-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b2d83-366">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2d83-366">Namespace</span></span><br/>                | <span data-ttu-id="b2d83-367">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b2d83-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b2d83-368">MOF</span><span class="sxs-lookup"><span data-stu-id="b2d83-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2d83-369"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b2d83-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2d83-370">DLL</span><span class="sxs-lookup"><span data-stu-id="b2d83-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2d83-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2d83-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d83-372">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2d83-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d83-373">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="b2d83-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

