---
title: MDM_Policy_Config01_ApplicationDefaults02-Klasse
description: Die \_ \_ Config01 ApplicationDefaults02-Klasse der MDM-Richtlinie \_ ermöglicht einem Administrator das Festlegen von Standard Dateityp-und Protokoll Zuordnungen. Wenn festgelegt, werden Standard Zuordnungen auf die Anmeldung beim PC angewendet.
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- MDM_Policy_Config01_ApplicationDefaults02-Klasse
- MDM_Policy_Config01_ApplicationDefaults02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476035"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a><span data-ttu-id="db815-106">MDM- \_ Richtlinie \_ Config01 \_ ApplicationDefaults02-Klasse</span><span class="sxs-lookup"><span data-stu-id="db815-106">MDM\_Policy\_Config01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="db815-107">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="db815-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="db815-108">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="db815-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="db815-109">Die \_ \_ Config01 ApplicationDefaults02-Klasse der MDM-Richtlinie \_ ermöglicht einem Administrator das Festlegen von Standard Dateityp-und Protokoll Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="db815-109">The MDM\_Policy\_Config01\_ApplicationDefaults02 class allows an administrator to set default file type and protocol associations.</span></span> <span data-ttu-id="db815-110">Wenn festgelegt, werden Standard Zuordnungen auf die Anmeldung beim PC angewendet.</span><span class="sxs-lookup"><span data-stu-id="db815-110">When set, default associations will be applied on sign-in to the PC.</span></span>

<span data-ttu-id="db815-111">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="db815-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="db815-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="db815-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="db815-113">Member</span><span class="sxs-lookup"><span data-stu-id="db815-113">Members</span></span>

<span data-ttu-id="db815-114">Die **MDM- \_ Richtlinie \_ Config01 \_ ApplicationDefaults02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="db815-114">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="db815-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db815-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db815-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="db815-116">Properties</span></span>

<span data-ttu-id="db815-117">Die **MDM- \_ Richtlinie \_ Config01 \_ ApplicationDefaults02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="db815-117">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="db815-118">Defaultassociationsconfiguration</span><span class="sxs-lookup"><span data-stu-id="db815-118">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db815-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="db815-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db815-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="db815-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="db815-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="db815-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db815-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="db815-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db815-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="db815-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db815-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="db815-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="db815-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="db815-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db815-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="db815-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db815-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="db815-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db815-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="db815-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db815-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db815-129">Requirements</span></span>



| <span data-ttu-id="db815-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db815-130">Requirement</span></span> | <span data-ttu-id="db815-131">Wert</span><span class="sxs-lookup"><span data-stu-id="db815-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db815-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db815-132">Minimum supported client</span></span><br/> | <span data-ttu-id="db815-133">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db815-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db815-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db815-134">Minimum supported server</span></span><br/> | <span data-ttu-id="db815-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db815-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="db815-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="db815-136">Namespace</span></span><br/>                | <span data-ttu-id="db815-137">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="db815-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="db815-138">MOF</span><span class="sxs-lookup"><span data-stu-id="db815-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db815-139"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="db815-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="db815-140">DLL</span><span class="sxs-lookup"><span data-stu-id="db815-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db815-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db815-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

