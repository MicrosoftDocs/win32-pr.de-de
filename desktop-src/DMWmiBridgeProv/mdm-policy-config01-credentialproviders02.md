---
title: MDM_Policy_Config01_CredentialProviders02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ CredentialProviders02-Klasse konfiguriert die verfügbaren Richtlinien für Anmelde Informationsanbieter.
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- MDM_Policy_Config01_CredentialProviders02-Klasse
- MDM_Policy_Config01_CredentialProviders02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476026"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a><span data-ttu-id="ba904-105">MDM- \_ Richtlinie \_ Config01 \_ CredentialProviders02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ba904-105">MDM\_Policy\_Config01\_CredentialProviders02 class</span></span>

<span data-ttu-id="ba904-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ba904-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ba904-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ba904-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ba904-108">Die MDM- \_ Richtlinie \_ Config01 \_ CredentialProviders02-Klasse konfiguriert die verfügbaren Richtlinien für Anmelde Informationsanbieter.</span><span class="sxs-lookup"><span data-stu-id="ba904-108">The MDM\_Policy\_Config01\_CredentialProviders02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="ba904-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ba904-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba904-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba904-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="ba904-111">Member</span><span class="sxs-lookup"><span data-stu-id="ba904-111">Members</span></span>

<span data-ttu-id="ba904-112">Die **MDM- \_ Richtlinie \_ Config01 \_ CredentialProviders02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ba904-112">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="ba904-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba904-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba904-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba904-114">Properties</span></span>

<span data-ttu-id="ba904-115">Die **MDM- \_ Richtlinie \_ Config01 \_ CredentialProviders02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba904-115">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ba904-116">Allowpinlogon</span><span class="sxs-lookup"><span data-stu-id="ba904-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba904-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ba904-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba904-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ba904-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba904-119">Blockpicturepassword</span><span class="sxs-lookup"><span data-stu-id="ba904-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba904-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ba904-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba904-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ba904-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba904-122">Disableautomatikredeploymentanmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="ba904-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba904-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ba904-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba904-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ba904-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ba904-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ba904-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba904-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ba904-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba904-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba904-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba904-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba904-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ba904-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ba904-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba904-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ba904-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba904-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba904-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba904-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba904-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba904-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba904-133">Requirements</span></span>



| <span data-ttu-id="ba904-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba904-134">Requirement</span></span> | <span data-ttu-id="ba904-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ba904-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba904-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba904-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ba904-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba904-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba904-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba904-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ba904-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ba904-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ba904-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba904-140">Namespace</span></span><br/>                | <span data-ttu-id="ba904-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ba904-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ba904-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ba904-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba904-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ba904-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba904-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ba904-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba904-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba904-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

