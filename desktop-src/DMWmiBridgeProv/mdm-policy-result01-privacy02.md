---
title: MDM_Policy_Result01_Privacy02-Klasse
description: Die Result01 Privacy02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Such Richtlinien dar.
ms.assetid: 40aa1b74-bdec-471d-a7d4-89e59bf8637c
keywords:
- MDM_Policy_Result01_Privacy02-Klasse
- MDM_Policy_Result01_Privacy02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Privacy02
- MDM_Policy_Result01_Privacy02.InstanceID
- MDM_Policy_Result01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bbe28d1c0bc1258ec3c9fb57fd592a97c96026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475324"
---
# <a name="mdm_policy_result01_privacy02-class"></a><span data-ttu-id="d75f3-105">MDM- \_ Richtlinie \_ Result01 \_ Privacy02-Klasse</span><span class="sxs-lookup"><span data-stu-id="d75f3-105">MDM\_Policy\_Result01\_Privacy02 class</span></span>

<span data-ttu-id="d75f3-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d75f3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d75f3-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d75f3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d75f3-108">Die **\_ \_ Result01 \_ Privacy02-Klasse der MDM-Richtlinie** stellt die verfügbaren Such Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="d75f3-108">The **MDM\_Policy\_Result01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="d75f3-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d75f3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75f3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d75f3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Privacy02
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

## <a name="members"></a><span data-ttu-id="d75f3-111">Member</span><span class="sxs-lookup"><span data-stu-id="d75f3-111">Members</span></span>

<span data-ttu-id="d75f3-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Privacy02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d75f3-112">The **MDM\_Policy\_Result01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="d75f3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d75f3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d75f3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d75f3-114">Properties</span></span>

<span data-ttu-id="d75f3-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Privacy02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d75f3-115">The **MDM\_Policy\_Result01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d75f3-116">Allowautoaccept tpuningandprivacyzustimmung</span><span class="sxs-lookup"><span data-stu-id="d75f3-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-119">Zuordnung von "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="d75f3-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-122">Disablewerbung</span><span class="sxs-lookup"><span data-stu-id="d75f3-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-125">Enableactivityfeed</span><span class="sxs-lookup"><span data-stu-id="d75f3-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d75f3-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d75f3-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d75f3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d75f3-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d75f3-132">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="d75f3-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="d75f3-133">Für diese Klasse ist die Zeichenfolge "Privacy".</span><span class="sxs-lookup"><span data-stu-id="d75f3-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="d75f3-134">Letappsaccessaccountinfo</span><span class="sxs-lookup"><span data-stu-id="d75f3-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-137">Letappsaccessaccountinfo \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-140">Letappsaccessaccountinfo \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-143">Letappsaccessaccountinfo \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-146">Letappsaccesscalendar</span><span class="sxs-lookup"><span data-stu-id="d75f3-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-149">Letappsaccesscalendar \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-152">Letappsaccesscalendar \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-154">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-155">Letappsaccesscalendar \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-158">Letappsaccesscallhistory</span><span class="sxs-lookup"><span data-stu-id="d75f3-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-159">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-160">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-161">Letappsaccesscallhistory \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-164">Letappsaccesscallhistory \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-167">Letappsaccesscallhistory \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-169">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-170">Letappsaccesscamera</span><span class="sxs-lookup"><span data-stu-id="d75f3-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-171">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-172">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-173">Letappsaccesscamera \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-176">Letappsaccesscamera \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-178">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-179">Letappsaccesscamera \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-182">Letappsaccesscontacts</span><span class="sxs-lookup"><span data-stu-id="d75f3-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-183">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-185">Letappsaccesscontacts \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-187">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-188">Letappsaccesscontacts \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-190">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-191">Letappsaccesscontacts \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-193">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-194">Letappsacceslmail</span><span class="sxs-lookup"><span data-stu-id="d75f3-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-195">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-196">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-197">Letappsacceslmail \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-199">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-200">Letappsacceslmail \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-202">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-203">Letappsacceslmail \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-204">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-205">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-206">Letappsaccesslocation</span><span class="sxs-lookup"><span data-stu-id="d75f3-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-207">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-208">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-209">Letappsaccesslocation \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-211">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-212">Letappsaccesslocation \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-214">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-215">Letappsaccesslocation \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-217">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-218">Letappsaccessmessaging</span><span class="sxs-lookup"><span data-stu-id="d75f3-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-219">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-220">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-221">Letappsaccessmessaging \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-223">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-224">Letappsaccessmessaging \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-227">Letappsaccessmessaging \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-229">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-230">Letappsaccessmikrofon</span><span class="sxs-lookup"><span data-stu-id="d75f3-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-231">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-232">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-233">Letappsaccessmikrofon \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-236">Letappsaccessmikrofon \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-238">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-239">Letappsaccessmikrofon \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-241">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-242">Letappsaccessmotion</span><span class="sxs-lookup"><span data-stu-id="d75f3-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-243">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-245">Letappsaccessmotion \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-247">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-248">Letappsaccessmotion \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-250">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-251">Letappsaccessmotion \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-254">Letappsaccessbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d75f3-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-255">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-256">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-257">Letappsaccessbenachrichtigungen \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-259">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-260">Letappsaccessbenachrichtigungen \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-263">Letappsaccessbenachrichtigungen \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-264">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-265">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-266">Letappsaccessphone</span><span class="sxs-lookup"><span data-stu-id="d75f3-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-267">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-269">Letappsaccessphone \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-270">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-271">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-272">Letappsaccessphone \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-274">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-275">Letappsaccessphone \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-277">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-278">Letappsaccessradios</span><span class="sxs-lookup"><span data-stu-id="d75f3-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-279">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-280">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-281">Letappsaccessradios \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-282">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-283">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-284">Letappsaccessradios \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-286">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-287">Letappsaccessradios \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-289">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-290">Letappsaccesstasks</span><span class="sxs-lookup"><span data-stu-id="d75f3-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-291">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-292">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-293">Letappsaccesstasks \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-294">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-295">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-296">Letappsaccesstasks \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-298">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-299">Letappsaccesstasks \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-301">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-302">Letappsaccesstrusteddevices</span><span class="sxs-lookup"><span data-stu-id="d75f3-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-303">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-304">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-305">Letappsaccesstrusteddevices \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-306">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-307">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-308">Letappsaccesstrusteddevices \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-310">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-311">Letappsaccesstrusteddevices \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-313">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-314">Letappsgetdiagnosticinfo</span><span class="sxs-lookup"><span data-stu-id="d75f3-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-315">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-316">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-317">Letappsgetdiagnosticinfo \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-319">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-320">Letappsgetdiagnosticinfo \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-322">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-323">Letappsgetdiagnosticinfo \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-325">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-326">Letappsruninbackground</span><span class="sxs-lookup"><span data-stu-id="d75f3-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-327">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-328">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-329">Letappsruninbackground \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-331">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-332">Letappsruninbackground \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-334">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-335">Letappsruninbackground \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-337">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-338">Letappssyncwithdevices</span><span class="sxs-lookup"><span data-stu-id="d75f3-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-339">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-340">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-341">Letappssyncwithdevices \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-343">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-344">Letappssyncwithdevices \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-346">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d75f3-347">Letappssyncwithdevices \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="d75f3-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-349">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d75f3-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d75f3-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-351">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d75f3-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d75f3-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-353">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d75f3-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d75f3-354">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="d75f3-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="d75f3-355">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="d75f3-355">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="d75f3-356">Publishuseractivities</span><span class="sxs-lookup"><span data-stu-id="d75f3-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d75f3-357">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d75f3-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d75f3-358">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d75f3-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d75f3-359">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d75f3-359">Requirements</span></span>



| <span data-ttu-id="d75f3-360">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d75f3-360">Requirement</span></span> | <span data-ttu-id="d75f3-361">Wert</span><span class="sxs-lookup"><span data-stu-id="d75f3-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d75f3-362">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d75f3-362">Minimum supported client</span></span><br/> | <span data-ttu-id="d75f3-363">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d75f3-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d75f3-364">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d75f3-364">Minimum supported server</span></span><br/> | <span data-ttu-id="d75f3-365">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d75f3-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d75f3-366">Namespace</span><span class="sxs-lookup"><span data-stu-id="d75f3-366">Namespace</span></span><br/>                | <span data-ttu-id="d75f3-367">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d75f3-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d75f3-368">MOF</span><span class="sxs-lookup"><span data-stu-id="d75f3-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d75f3-369"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d75f3-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d75f3-370">DLL</span><span class="sxs-lookup"><span data-stu-id="d75f3-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d75f3-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d75f3-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75f3-372">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d75f3-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75f3-373">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="d75f3-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

