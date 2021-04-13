---
title: MDM_Policy_Result01_CredentialsUI02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ CredentialsUI02-Klasse stellt die verfügbaren Anmelde Informationsrichtlinien dar.
ms.assetid: d50a4cc5-e87f-44a5-9345-744126615d04
keywords:
- MDM_Policy_Result01_CredentialsUI02-Klasse
- MDM_Policy_Result01_CredentialsUI02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_CredentialsUI02
- MDM_Policy_Result01_CredentialsUI02.InstanceID
- MDM_Policy_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e444e36f2602fa30ca51601e6cd08e7fa8e30c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475717"
---
# <a name="mdm_policy_result01_credentialsui02-class"></a><span data-ttu-id="ab01d-105">MDM- \_ Richtlinie \_ Result01 \_ CredentialsUI02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ab01d-105">MDM\_Policy\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="ab01d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ab01d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ab01d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ab01d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ab01d-108">Die MDM- \_ Richtlinie \_ Result01 \_ CredentialsUI02-Klasse stellt die verfügbaren Anmelde Informationsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="ab01d-108">The MDM\_Policy\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="ab01d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ab01d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab01d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab01d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="ab01d-111">Member</span><span class="sxs-lookup"><span data-stu-id="ab01d-111">Members</span></span>

<span data-ttu-id="ab01d-112">Die **MDM- \_ Richtlinie \_ Result01 \_ CredentialsUI02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ab01d-112">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="ab01d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab01d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab01d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab01d-114">Properties</span></span>

<span data-ttu-id="ab01d-115">Die **MDM- \_ Richtlinie \_ Result01 \_ CredentialsUI02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab01d-115">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ab01d-116">Disablepasswordreveal</span><span class="sxs-lookup"><span data-stu-id="ab01d-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab01d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab01d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab01d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab01d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ab01d-119">Enumerateadministrators</span><span class="sxs-lookup"><span data-stu-id="ab01d-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab01d-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab01d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab01d-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab01d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab01d-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ab01d-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab01d-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab01d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab01d-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab01d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab01d-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab01d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab01d-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ab01d-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab01d-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ab01d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab01d-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ab01d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab01d-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab01d-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab01d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab01d-130">Requirements</span></span>



| <span data-ttu-id="ab01d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab01d-131">Requirement</span></span> | <span data-ttu-id="ab01d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ab01d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab01d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab01d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ab01d-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab01d-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab01d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab01d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ab01d-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ab01d-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ab01d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab01d-137">Namespace</span></span><br/>                | <span data-ttu-id="ab01d-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ab01d-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ab01d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ab01d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab01d-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ab01d-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab01d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ab01d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab01d-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab01d-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

