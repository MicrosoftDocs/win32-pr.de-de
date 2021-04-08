---
title: MDM_Policy_Result01_ApplicationDefaults02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ ApplicationDefaults02-Klasse stellt die verfügbaren Anwendungsstandard Richtlinien dar.
ms.assetid: bf7df9a1-7af1-49a6-9456-3e6ec48234e2
keywords:
- MDM_Policy_Result01_ApplicationDefaults02-Klasse
- MDM_Policy_Result01_ApplicationDefaults02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationDefaults02
- MDM_Policy_Result01_ApplicationDefaults02.InstanceID
- MDM_Policy_Result01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10592ceb4e4f401ce9f64c24ef207a4e2e033e9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103886"
---
# <a name="mdm_policy_result01_applicationdefaults02-class"></a><span data-ttu-id="dacb7-105">MDM- \_ Richtlinie \_ Result01 \_ ApplicationDefaults02-Klasse</span><span class="sxs-lookup"><span data-stu-id="dacb7-105">MDM\_Policy\_Result01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="dacb7-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dacb7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dacb7-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="dacb7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dacb7-108">Die MDM- \_ Richtlinie \_ Result01 \_ ApplicationDefaults02-Klasse stellt die verfügbaren Anwendungsstandard Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="dacb7-108">The MDM\_Policy\_Result01\_ApplicationDefaults02 class represents the available application defaults policies.</span></span>

<span data-ttu-id="dacb7-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="dacb7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dacb7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dacb7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="dacb7-111">Member</span><span class="sxs-lookup"><span data-stu-id="dacb7-111">Members</span></span>

<span data-ttu-id="dacb7-112">Die **MDM- \_ Richtlinie \_ Result01 \_ ApplicationDefaults02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dacb7-112">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="dacb7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dacb7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dacb7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dacb7-114">Properties</span></span>

<span data-ttu-id="dacb7-115">Die **MDM- \_ Richtlinie \_ Result01 \_ ApplicationDefaults02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dacb7-115">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dacb7-116">Defaultassociationsconfiguration</span><span class="sxs-lookup"><span data-stu-id="dacb7-116">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dacb7-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dacb7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dacb7-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dacb7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dacb7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dacb7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dacb7-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dacb7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dacb7-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dacb7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dacb7-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dacb7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dacb7-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dacb7-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dacb7-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dacb7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dacb7-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dacb7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dacb7-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dacb7-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dacb7-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dacb7-127">Requirements</span></span>



| <span data-ttu-id="dacb7-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dacb7-128">Requirement</span></span> | <span data-ttu-id="dacb7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="dacb7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dacb7-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dacb7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dacb7-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dacb7-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dacb7-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dacb7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dacb7-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dacb7-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dacb7-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="dacb7-134">Namespace</span></span><br/>                | <span data-ttu-id="dacb7-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dacb7-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dacb7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="dacb7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dacb7-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dacb7-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dacb7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dacb7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dacb7-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dacb7-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

