---
title: MDM_Policy_Config01_Display02-Klasse
description: Die Config01 Display02-Klasse der MDM- \_ Richtlinie \_ \_ konfiguriert die Anzeige Richtlinien.
ms.assetid: 106eecc5-ede0-4d66-ba51-967a8f7bcb66
keywords:
- MDM_Policy_Config01_Display02-Klasse
- MDM_Policy_Config01_Display02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Display02
- MDM_Policy_Config01_Display02.InstanceID
- MDM_Policy_Config01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e79861a911d03f1d9174053dc8ec7c62824fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103306"
---
# <a name="mdm_policy_config01_display02-class"></a><span data-ttu-id="c98b4-105">MDM- \_ Richtlinie \_ Config01 \_ Display02-Klasse</span><span class="sxs-lookup"><span data-stu-id="c98b4-105">MDM\_Policy\_Config01\_Display02 class</span></span>

<span data-ttu-id="c98b4-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c98b4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c98b4-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c98b4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c98b4-108">Die Config01 Display02-Klasse der MDM- \_ Richtlinie \_ \_ konfiguriert die Anzeige Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="c98b4-108">The MDM\_Policy\_Config01\_Display02 class configures the display policies.</span></span>

<span data-ttu-id="c98b4-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c98b4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c98b4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c98b4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="c98b4-111">Member</span><span class="sxs-lookup"><span data-stu-id="c98b4-111">Members</span></span>

<span data-ttu-id="c98b4-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Display02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c98b4-112">The **MDM\_Policy\_Config01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="c98b4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c98b4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c98b4-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c98b4-114">Properties</span></span>

<span data-ttu-id="c98b4-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Display02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c98b4-115">The **MDM\_Policy\_Config01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c98b4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c98b4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98b4-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c98b4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98b4-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c98b4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98b4-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c98b4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c98b4-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c98b4-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98b4-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c98b4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98b4-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c98b4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98b4-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c98b4-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c98b4-124">Turnoffgdidpiscalingforapps</span><span class="sxs-lookup"><span data-stu-id="c98b4-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98b4-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c98b4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98b4-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c98b4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c98b4-127">Turnongdidpiscalingforapps</span><span class="sxs-lookup"><span data-stu-id="c98b4-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98b4-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c98b4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98b4-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c98b4-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c98b4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c98b4-130">Requirements</span></span>



| <span data-ttu-id="c98b4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c98b4-131">Requirement</span></span> | <span data-ttu-id="c98b4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c98b4-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c98b4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c98b4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c98b4-134">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c98b4-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c98b4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c98b4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c98b4-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c98b4-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c98b4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c98b4-137">Namespace</span></span><br/>                | <span data-ttu-id="c98b4-138">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c98b4-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c98b4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c98b4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c98b4-140"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c98b4-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c98b4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c98b4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c98b4-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c98b4-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

