---
title: MDM_Policy_Result01_Autoplay02-Klasse
description: Die MDM \_ Policy \_ Result01 \_ Autoplay02-Klasse stellt die verfügbaren automatische Wiedergabe-Richtlinien dar.
ms.assetid: f116015d-f10e-4d17-9c0b-7253894e6c0f
keywords:
- MDM_Policy_Result01_Autoplay02-Klasse
- MDM_Policy_Result01_Autoplay02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Autoplay02
- MDM_Policy_Result01_Autoplay02.InstanceID
- MDM_Policy_Result01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abf48754cff1513d6d373c9addb34b8ec9acc26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106130"
---
# <a name="mdm_policy_result01_autoplay02-class"></a><span data-ttu-id="29e67-105">MDM- \_ Richtlinie \_ Result01 \_ Autoplay02-Klasse</span><span class="sxs-lookup"><span data-stu-id="29e67-105">MDM\_Policy\_Result01\_Autoplay02 class</span></span>

<span data-ttu-id="29e67-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="29e67-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="29e67-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="29e67-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="29e67-108">Die MDM \_ Policy \_ Result01 \_ Autoplay02-Klasse stellt die verfügbaren automatische Wiedergabe-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="29e67-108">The MDM\_Policy\_Result01\_Autoplay02 class represents the available autoplay policies.</span></span>

<span data-ttu-id="29e67-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="29e67-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e67-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="29e67-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="29e67-111">Member</span><span class="sxs-lookup"><span data-stu-id="29e67-111">Members</span></span>

<span data-ttu-id="29e67-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Autoplay02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="29e67-112">The **MDM\_Policy\_Result01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="29e67-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29e67-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29e67-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29e67-114">Properties</span></span>

<span data-ttu-id="29e67-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Autoplay02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="29e67-115">The **MDM\_Policy\_Result01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="29e67-116">Disallowautoplayfornonvolumedevices</span><span class="sxs-lookup"><span data-stu-id="29e67-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29e67-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29e67-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29e67-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29e67-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29e67-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="29e67-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29e67-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29e67-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29e67-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29e67-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29e67-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="29e67-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29e67-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="29e67-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29e67-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29e67-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29e67-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="29e67-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29e67-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="29e67-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29e67-127">Setdefaultautor unbehavior</span><span class="sxs-lookup"><span data-stu-id="29e67-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29e67-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29e67-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29e67-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29e67-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29e67-130">Turnoffautoplay</span><span class="sxs-lookup"><span data-stu-id="29e67-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29e67-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="29e67-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29e67-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="29e67-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29e67-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29e67-133">Requirements</span></span>



| <span data-ttu-id="29e67-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29e67-134">Requirement</span></span> | <span data-ttu-id="29e67-135">Wert</span><span class="sxs-lookup"><span data-stu-id="29e67-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e67-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29e67-136">Minimum supported client</span></span><br/> | <span data-ttu-id="29e67-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29e67-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="29e67-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29e67-138">Minimum supported server</span></span><br/> | <span data-ttu-id="29e67-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="29e67-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="29e67-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="29e67-140">Namespace</span></span><br/>                | <span data-ttu-id="29e67-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="29e67-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="29e67-142">MOF</span><span class="sxs-lookup"><span data-stu-id="29e67-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29e67-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="29e67-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="29e67-144">DLL</span><span class="sxs-lookup"><span data-stu-id="29e67-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29e67-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29e67-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

