---
title: MDM_Policy_Result01_DataUsage02-Klasse
description: Die Result01 DataUsage02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Daten Verwendungs Richtlinien dar.
ms.assetid: 4efcab61-2060-44dc-bc3c-7b23802fa284
keywords:
- MDM_Policy_Result01_DataUsage02-Klasse
- MDM_Policy_Result01_DataUsage02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DataUsage02
- MDM_Policy_Result01_DataUsage02.InstanceID
- MDM_Policy_Result01_DataUsage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d97bcfba122bd3d974025975a69ba6a5be9c8ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478054"
---
# <a name="mdm_policy_result01_datausage02-class"></a><span data-ttu-id="e51f3-105">MDM- \_ Richtlinie \_ Result01 \_ DataUsage02-Klasse</span><span class="sxs-lookup"><span data-stu-id="e51f3-105">MDM\_Policy\_Result01\_DataUsage02 class</span></span>

<span data-ttu-id="e51f3-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e51f3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e51f3-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e51f3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e51f3-108">Die Result01 DataUsage02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Daten Verwendungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="e51f3-108">The MDM\_Policy\_Result01\_DataUsage02 class represents the available data usage policies.</span></span>

<span data-ttu-id="e51f3-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e51f3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51f3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e51f3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DataUsage02
{
  string InstanceID;
  string ParentID;
  string SetCost3G;
  string SetCost4G;
};
```

## <a name="members"></a><span data-ttu-id="e51f3-111">Member</span><span class="sxs-lookup"><span data-stu-id="e51f3-111">Members</span></span>

<span data-ttu-id="e51f3-112">Die **MDM- \_ Richtlinie \_ Result01 \_ DataUsage02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e51f3-112">The **MDM\_Policy\_Result01\_DataUsage02** class has these types of members:</span></span>

-   [<span data-ttu-id="e51f3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e51f3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e51f3-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e51f3-114">Properties</span></span>

<span data-ttu-id="e51f3-115">Die **MDM- \_ Richtlinie \_ Result01 \_ DataUsage02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e51f3-115">The **MDM\_Policy\_Result01\_DataUsage02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e51f3-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e51f3-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e51f3-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e51f3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e51f3-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e51f3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e51f3-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e51f3-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e51f3-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e51f3-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e51f3-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e51f3-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e51f3-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e51f3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e51f3-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e51f3-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e51f3-124">SetCost3G</span><span class="sxs-lookup"><span data-stu-id="e51f3-124">SetCost3G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost3g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e51f3-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e51f3-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e51f3-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e51f3-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e51f3-127">SetCost4G</span><span class="sxs-lookup"><span data-stu-id="e51f3-127">SetCost4G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost4g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e51f3-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e51f3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e51f3-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e51f3-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e51f3-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e51f3-130">Requirements</span></span>



| <span data-ttu-id="e51f3-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e51f3-131">Requirement</span></span> | <span data-ttu-id="e51f3-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e51f3-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51f3-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e51f3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e51f3-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e51f3-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e51f3-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e51f3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e51f3-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e51f3-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e51f3-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="e51f3-137">Namespace</span></span><br/>                | <span data-ttu-id="e51f3-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e51f3-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e51f3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e51f3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e51f3-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e51f3-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e51f3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e51f3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e51f3-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e51f3-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

