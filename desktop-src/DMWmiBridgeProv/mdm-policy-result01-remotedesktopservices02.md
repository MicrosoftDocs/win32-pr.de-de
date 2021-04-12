---
title: MDM_Policy_Result01_RemoteDesktopServices02-Klasse
description: Die MDM \_ -Richtlinie \_ Result01 \_ RemoteDesktopServices02-Klasse stellt die Remote Desktop Dienste-Richtlinien dar.
ms.assetid: 015fe30d-2b76-4df5-a81f-65e488db3526
keywords:
- MDM_Policy_Result01_RemoteDesktopServices02-Klasse
- MDM_Policy_Result01_RemoteDesktopServices02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteDesktopServices02
- MDM_Policy_Result01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Result01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0488308a557f1b872de299bda12487287e1081c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949453"
---
# <a name="mdm_policy_result01_remotedesktopservices02-class"></a><span data-ttu-id="14c4e-105">MDM- \_ Richtlinie \_ Result01 \_ RemoteDesktopServices02-Klasse</span><span class="sxs-lookup"><span data-stu-id="14c4e-105">MDM\_Policy\_Result01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="14c4e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="14c4e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="14c4e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="14c4e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="14c4e-108">Die MDM \_ -Richtlinie \_ Result01 \_ RemoteDesktopServices02-Klasse stellt die Remote Desktop Dienste-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="14c4e-108">The MDM\_Policy\_Result01\_RemoteDesktopServices02 class represents the remote desktop services policies.</span></span>

<span data-ttu-id="14c4e-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="14c4e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c4e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="14c4e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteDesktopServices02
{
  string InstanceID;
  string ParentID;
  string AllowUsersToConnectRemotely;
  string ClientConnectionEncryptionLevel;
  string DoNotAllowDriveRedirection;
  string DoNotAllowPasswordSaving;
  string PromptForPasswordUponConnection;
  string RequireSecureRPCCommunication;
};
```

## <a name="members"></a><span data-ttu-id="14c4e-111">Member</span><span class="sxs-lookup"><span data-stu-id="14c4e-111">Members</span></span>

<span data-ttu-id="14c4e-112">Die **MDM- \_ Richtlinie \_ Result01 \_ RemoteDesktopServices02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14c4e-112">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="14c4e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14c4e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14c4e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14c4e-114">Properties</span></span>

<span data-ttu-id="14c4e-115">Die **MDM- \_ Richtlinie \_ Result01 \_ RemoteDesktopServices02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14c4e-115">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="14c4e-116">Zuordnung von "zugebeserstoconnectremutly"</span><span class="sxs-lookup"><span data-stu-id="14c4e-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="14c4e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="14c4e-119">Clientconnectionverschlüsselunglevel</span><span class="sxs-lookup"><span data-stu-id="14c4e-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="14c4e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="14c4e-122">Donotallowdriveredirection</span><span class="sxs-lookup"><span data-stu-id="14c4e-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="14c4e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="14c4e-125">Donotallowpasswordsave</span><span class="sxs-lookup"><span data-stu-id="14c4e-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="14c4e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="14c4e-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="14c4e-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14c4e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14c4e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="14c4e-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="14c4e-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14c4e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14c4e-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="14c4e-136">Promptforpassworduponconnection</span><span class="sxs-lookup"><span data-stu-id="14c4e-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="14c4e-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="14c4e-139">Requirements securerpccommunication</span><span class="sxs-lookup"><span data-stu-id="14c4e-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c4e-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14c4e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c4e-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="14c4e-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14c4e-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14c4e-142">Requirements</span></span>



| <span data-ttu-id="14c4e-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14c4e-143">Requirement</span></span> | <span data-ttu-id="14c4e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="14c4e-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c4e-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14c4e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="14c4e-146">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14c4e-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14c4e-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14c4e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="14c4e-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="14c4e-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="14c4e-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="14c4e-149">Namespace</span></span><br/>                | <span data-ttu-id="14c4e-150">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="14c4e-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="14c4e-151">MOF</span><span class="sxs-lookup"><span data-stu-id="14c4e-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14c4e-152"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="14c4e-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="14c4e-153">DLL</span><span class="sxs-lookup"><span data-stu-id="14c4e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14c4e-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14c4e-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

