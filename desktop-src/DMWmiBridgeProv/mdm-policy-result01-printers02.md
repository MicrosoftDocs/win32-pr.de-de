---
title: MDM_Policy_Result01_Printers02-Klasse
description: Die Result01 Printers02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Drucker Richtlinien dar.
ms.assetid: f64fbb03-c62c-4f8e-97ad-e08e068a31d1
keywords:
- MDM_Policy_Result01_Printers02-Klasse
- MDM_Policy_Result01_Printers02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Printers02
- MDM_Policy_Result01_Printers02.InstanceID
- MDM_Policy_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042820825441928aa04d499a06df3a05ced3889d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391646"
---
# <a name="mdm_policy_result01_printers02-class"></a><span data-ttu-id="94753-105">MDM- \_ Richtlinie \_ Result01 \_ Printers02-Klasse</span><span class="sxs-lookup"><span data-stu-id="94753-105">MDM\_Policy\_Result01\_Printers02 class</span></span>

<span data-ttu-id="94753-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="94753-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="94753-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="94753-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="94753-108">Die Result01 Printers02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Drucker Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="94753-108">The MDM\_Policy\_Result01\_Printers02 class represents the printer policies.</span></span>

<span data-ttu-id="94753-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="94753-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94753-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="94753-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions;
  string PublishPrinters;
};
```

## <a name="members"></a><span data-ttu-id="94753-111">Member</span><span class="sxs-lookup"><span data-stu-id="94753-111">Members</span></span>

<span data-ttu-id="94753-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Printers02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="94753-112">The **MDM\_Policy\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="94753-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94753-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94753-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94753-114">Properties</span></span>

<span data-ttu-id="94753-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Printers02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="94753-115">The **MDM\_Policy\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94753-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="94753-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94753-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="94753-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94753-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94753-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94753-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="94753-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94753-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="94753-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94753-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="94753-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94753-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94753-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94753-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="94753-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94753-124">Pointandprintrestrictions</span><span class="sxs-lookup"><span data-stu-id="94753-124">PointAndPrintRestrictions</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94753-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="94753-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94753-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="94753-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94753-127">Publishprinter</span><span class="sxs-lookup"><span data-stu-id="94753-127">PublishPrinters</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-publishprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94753-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="94753-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94753-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="94753-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94753-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94753-130">Requirements</span></span>



| <span data-ttu-id="94753-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94753-131">Requirement</span></span> | <span data-ttu-id="94753-132">Wert</span><span class="sxs-lookup"><span data-stu-id="94753-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94753-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94753-133">Minimum supported client</span></span><br/> | <span data-ttu-id="94753-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94753-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94753-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94753-135">Minimum supported server</span></span><br/> | <span data-ttu-id="94753-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="94753-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="94753-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="94753-137">Namespace</span></span><br/>                | <span data-ttu-id="94753-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="94753-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="94753-139">MOF</span><span class="sxs-lookup"><span data-stu-id="94753-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94753-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="94753-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="94753-141">DLL</span><span class="sxs-lookup"><span data-stu-id="94753-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94753-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94753-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

