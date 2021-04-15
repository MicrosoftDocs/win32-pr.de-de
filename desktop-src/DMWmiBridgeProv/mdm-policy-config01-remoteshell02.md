---
title: MDM_Policy_Config01_RemoteShell02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ RemoteShell02-Klasse konfiguriert die remoteshellrichtlinien.
ms.assetid: 7026fadb-ec6a-4696-a24c-1b1e071b94b0
keywords:
- MDM_Policy_Config01_RemoteShell02-Klasse
- MDM_Policy_Config01_RemoteShell02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02.InstanceID
- MDM_Policy_Config01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c318b0c6f23e92d90091495fdc25993d6958ca56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476935"
---
# <a name="mdm_policy_config01_remoteshell02-class"></a><span data-ttu-id="60c24-105">MDM- \_ Richtlinie \_ Config01 \_ RemoteShell02-Klasse</span><span class="sxs-lookup"><span data-stu-id="60c24-105">MDM\_Policy\_Config01\_RemoteShell02 class</span></span>

<span data-ttu-id="60c24-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="60c24-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="60c24-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="60c24-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="60c24-108">Die MDM- \_ Richtlinie \_ Config01 \_ RemoteShell02-Klasse konfiguriert die remoteshellrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="60c24-108">The MDM\_Policy\_Config01\_RemoteShell02 class configures the remote shell policies.</span></span>

<span data-ttu-id="60c24-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="60c24-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c24-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="60c24-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteShell02
{
  string InstanceID;
  string ParentID;
  string AllowRemoteShellAccess;
  string MaxConcurrentUsers;
  string SpecifyIdleTimeout;
  string SpecifyMaxMemory;
  string SpecifyMaxProcesses;
  string SpecifyMaxRemoteShells;
  string SpecifyShellTimeout;
};
```

## <a name="members"></a><span data-ttu-id="60c24-111">Member</span><span class="sxs-lookup"><span data-stu-id="60c24-111">Members</span></span>

<span data-ttu-id="60c24-112">Die **MDM- \_ Richtlinie \_ Config01 \_ RemoteShell02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60c24-112">The **MDM\_Policy\_Config01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="60c24-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60c24-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60c24-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60c24-114">Properties</span></span>

<span data-ttu-id="60c24-115">Die **MDM- \_ Richtlinie \_ Config01 \_ RemoteShell02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60c24-115">The **MDM\_Policy\_Config01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="60c24-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="60c24-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60c24-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60c24-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="60c24-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60c24-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c24-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="60c24-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="60c24-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="60c24-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60c24-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60c24-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="60c24-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60c24-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c24-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="60c24-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="60c24-130">Specifyidletimeout</span><span class="sxs-lookup"><span data-stu-id="60c24-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60c24-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="60c24-133">Specifymaxmemory</span><span class="sxs-lookup"><span data-stu-id="60c24-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60c24-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="60c24-136">Specifymaxprocesses</span><span class="sxs-lookup"><span data-stu-id="60c24-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60c24-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="60c24-139">Specifymaxremoteshells</span><span class="sxs-lookup"><span data-stu-id="60c24-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60c24-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="60c24-142">Specifyshelltimeout</span><span class="sxs-lookup"><span data-stu-id="60c24-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c24-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60c24-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c24-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60c24-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60c24-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60c24-145">Requirements</span></span>



| <span data-ttu-id="60c24-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60c24-146">Requirement</span></span> | <span data-ttu-id="60c24-147">Wert</span><span class="sxs-lookup"><span data-stu-id="60c24-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c24-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60c24-148">Minimum supported client</span></span><br/> | <span data-ttu-id="60c24-149">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60c24-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60c24-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60c24-150">Minimum supported server</span></span><br/> | <span data-ttu-id="60c24-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="60c24-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="60c24-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="60c24-152">Namespace</span></span><br/>                | <span data-ttu-id="60c24-153">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="60c24-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="60c24-154">MOF</span><span class="sxs-lookup"><span data-stu-id="60c24-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60c24-155"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60c24-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="60c24-156">DLL</span><span class="sxs-lookup"><span data-stu-id="60c24-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c24-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c24-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

