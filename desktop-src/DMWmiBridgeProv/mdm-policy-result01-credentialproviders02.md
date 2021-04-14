---
title: MDM_Policy_Result01_CredentialProviders02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ CredentialProviders02-Klasse stellt die verfügbaren Richtlinien für Anmelde Informationsanbieter dar.
ms.assetid: dc9e276b-8813-46cf-8e5a-0d41a93331ea
keywords:
- MDM_Policy_Result01_CredentialProviders02-Klasse
- MDM_Policy_Result01_CredentialProviders02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_CredentialProviders02
- MDM_Policy_Result01_CredentialProviders02.InstanceID
- MDM_Policy_Result01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a2e6c0ababbf2706e82606ddb7c7c13a9087a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475720"
---
# <a name="mdm_policy_result01_credentialproviders02-class"></a><span data-ttu-id="d8527-105">MDM- \_ Richtlinie \_ Result01 \_ CredentialProviders02-Klasse</span><span class="sxs-lookup"><span data-stu-id="d8527-105">MDM\_Policy\_Result01\_CredentialProviders02 class</span></span>

<span data-ttu-id="d8527-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="d8527-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d8527-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="d8527-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d8527-108">Die MDM- \_ Richtlinie \_ Result01 \_ CredentialProviders02-Klasse stellt die verfügbaren Richtlinien für Anmelde Informationsanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="d8527-108">The MDM\_Policy\_Result01\_CredentialProviders02 class represents the available credential provider policies.</span></span>

<span data-ttu-id="d8527-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d8527-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8527-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8527-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="d8527-111">Member</span><span class="sxs-lookup"><span data-stu-id="d8527-111">Members</span></span>

<span data-ttu-id="d8527-112">Die **MDM- \_ Richtlinie \_ Result01 \_ CredentialProviders02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d8527-112">The **MDM\_Policy\_Result01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="d8527-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8527-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8527-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8527-114">Properties</span></span>

<span data-ttu-id="d8527-115">Die **MDM- \_ Richtlinie \_ Result01 \_ CredentialProviders02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8527-115">The **MDM\_Policy\_Result01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d8527-116">Allowpinlogon</span><span class="sxs-lookup"><span data-stu-id="d8527-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8527-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8527-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8527-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8527-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d8527-119">Blockpicturepassword</span><span class="sxs-lookup"><span data-stu-id="d8527-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8527-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8527-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8527-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8527-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d8527-122">Disableautomatikredeploymentanmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="d8527-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8527-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d8527-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8527-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d8527-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d8527-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8527-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8527-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8527-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8527-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8527-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8527-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8527-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d8527-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d8527-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8527-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d8527-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8527-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d8527-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8527-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8527-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8527-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8527-133">Requirements</span></span>



| <span data-ttu-id="d8527-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8527-134">Requirement</span></span> | <span data-ttu-id="d8527-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d8527-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8527-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8527-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d8527-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8527-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8527-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8527-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d8527-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8527-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d8527-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8527-140">Namespace</span></span><br/>                | <span data-ttu-id="d8527-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d8527-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d8527-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d8527-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8527-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d8527-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8527-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d8527-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8527-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8527-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

