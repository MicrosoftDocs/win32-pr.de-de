---
title: MDM_Policy_Config01_DeviceGuard02-Klasse
description: Mit der MDM- \_ Richtlinie \_ Config01 \_ DeviceGuard02 werden die Device Guard-Richtlinien konfiguriert.
ms.assetid: b8edf906-2486-4d8d-9410-d216bacf1728
keywords:
- MDM_Policy_Config01_DeviceGuard02-Klasse
- MDM_Policy_Config01_DeviceGuard02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceGuard02
- MDM_Policy_Config01_DeviceGuard02.InstanceID
- MDM_Policy_Config01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebcc8f3d929708cdff3ada8fe440f49a1aeb1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040155"
---
# <a name="mdm_policy_config01_deviceguard02-class"></a><span data-ttu-id="68615-105">MDM- \_ Richtlinie \_ Config01 \_ DeviceGuard02-Klasse</span><span class="sxs-lookup"><span data-stu-id="68615-105">MDM\_Policy\_Config01\_DeviceGuard02 class</span></span>

<span data-ttu-id="68615-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="68615-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="68615-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="68615-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="68615-108">Mit der MDM- \_ Richtlinie \_ Config01 \_ DeviceGuard02 werden die Device Guard-Richtlinien konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="68615-108">The MDM\_Policy\_Config01\_DeviceGuard02 configures the Device Guard policies.</span></span>

<span data-ttu-id="68615-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="68615-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68615-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="68615-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="68615-111">Member</span><span class="sxs-lookup"><span data-stu-id="68615-111">Members</span></span>

<span data-ttu-id="68615-112">Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceGuard02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="68615-112">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="68615-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68615-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68615-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68615-114">Properties</span></span>

<span data-ttu-id="68615-115">Die **MDM- \_ Richtlinie \_ Config01 \_ DeviceGuard02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68615-115">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="68615-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="68615-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="68615-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="68615-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="68615-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="68615-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68615-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="68615-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68615-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="68615-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68615-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68615-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68615-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="68615-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="68615-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="68615-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="68615-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="68615-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="68615-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="68615-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68615-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="68615-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68615-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="68615-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68615-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68615-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68615-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="68615-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="68615-130">Requirements platformsecurityfeatures</span><span class="sxs-lookup"><span data-stu-id="68615-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="68615-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="68615-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="68615-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="68615-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68615-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68615-133">Requirements</span></span>



| <span data-ttu-id="68615-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68615-134">Requirement</span></span> | <span data-ttu-id="68615-135">Wert</span><span class="sxs-lookup"><span data-stu-id="68615-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68615-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68615-136">Minimum supported client</span></span><br/> | <span data-ttu-id="68615-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68615-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68615-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68615-138">Minimum supported server</span></span><br/> | <span data-ttu-id="68615-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="68615-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="68615-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="68615-140">Namespace</span></span><br/>                | <span data-ttu-id="68615-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="68615-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="68615-142">MOF</span><span class="sxs-lookup"><span data-stu-id="68615-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68615-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="68615-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="68615-144">DLL</span><span class="sxs-lookup"><span data-stu-id="68615-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68615-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68615-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

