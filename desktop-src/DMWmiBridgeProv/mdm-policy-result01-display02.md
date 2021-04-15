---
title: MDM_Policy_Result01_Display02-Klasse
description: Die Result01 Display02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Anzeige Richtlinien dar.
ms.assetid: 9f8675d6-1fd7-4269-8059-9159622f03cb
keywords:
- MDM_Policy_Result01_Display02-Klasse
- MDM_Policy_Result01_Display02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Display02
- MDM_Policy_Result01_Display02.InstanceID
- MDM_Policy_Result01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b8097d943e92343250802d63c4dfa2e5c77920
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476908"
---
# <a name="mdm_policy_result01_display02-class"></a><span data-ttu-id="c5c52-105">MDM- \_ Richtlinie \_ Result01 \_ Display02-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5c52-105">MDM\_Policy\_Result01\_Display02 class</span></span>

<span data-ttu-id="c5c52-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c5c52-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c5c52-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c5c52-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c5c52-108">Die Result01 Display02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Anzeige Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="c5c52-108">The MDM\_Policy\_Result01\_Display02 class represents the display policies.</span></span>

<span data-ttu-id="c5c52-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c5c52-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c52-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5c52-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="c5c52-111">Member</span><span class="sxs-lookup"><span data-stu-id="c5c52-111">Members</span></span>

<span data-ttu-id="c5c52-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Display02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c5c52-112">The **MDM\_Policy\_Result01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="c5c52-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5c52-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5c52-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5c52-114">Properties</span></span>

<span data-ttu-id="c5c52-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Display02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5c52-115">The **MDM\_Policy\_Result01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5c52-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c5c52-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c52-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5c52-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c52-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5c52-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5c52-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5c52-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c5c52-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c5c52-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c52-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5c52-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c52-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5c52-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5c52-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5c52-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c5c52-124">Turnoffgdidpiscalingforapps</span><span class="sxs-lookup"><span data-stu-id="c5c52-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c52-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5c52-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c52-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c5c52-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c5c52-127">Turnongdidpiscalingforapps</span><span class="sxs-lookup"><span data-stu-id="c5c52-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5c52-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5c52-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5c52-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c5c52-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5c52-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5c52-130">Requirements</span></span>



| <span data-ttu-id="c5c52-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5c52-131">Requirement</span></span> | <span data-ttu-id="c5c52-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c5c52-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c52-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5c52-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c52-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5c52-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5c52-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5c52-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c52-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c5c52-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c5c52-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5c52-137">Namespace</span></span><br/>                | <span data-ttu-id="c5c52-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c5c52-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c5c52-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c5c52-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5c52-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c5c52-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5c52-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c5c52-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5c52-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5c52-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

