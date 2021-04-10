---
title: MDM_Policy_Result01_DeviceGuard02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ DeviceGuard02-Klasse konfiguriert die Device Guard-Richtlinien.
ms.assetid: ba21d324-85dc-4cb5-8123-196413e457eb
keywords:
- MDM_Policy_Result01_DeviceGuard02-Klasse
- MDM_Policy_Result01_DeviceGuard02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceGuard02
- MDM_Policy_Result01_DeviceGuard02.InstanceID
- MDM_Policy_Result01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e206a732628e442a391cb8b29f7712f5a5ec8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040344"
---
# <a name="mdm_policy_result01_deviceguard02-class"></a><span data-ttu-id="e4ba2-105">MDM- \_ Richtlinie \_ Result01 \_ DeviceGuard02-Klasse</span><span class="sxs-lookup"><span data-stu-id="e4ba2-105">MDM\_Policy\_Result01\_DeviceGuard02 class</span></span>

<span data-ttu-id="e4ba2-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e4ba2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e4ba2-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="e4ba2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e4ba2-108">Die MDM- \_ Richtlinie \_ Result01 \_ DeviceGuard02-Klasse konfiguriert die Device Guard-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="e4ba2-108">The MDM\_Policy\_Result01\_DeviceGuard02 class configures the Device Guard policies.</span></span>

<span data-ttu-id="e4ba2-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e4ba2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ba2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ba2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="e4ba2-111">Member</span><span class="sxs-lookup"><span data-stu-id="e4ba2-111">Members</span></span>

<span data-ttu-id="e4ba2-112">Die **MDM- \_ Richtlinie \_ Result01 \_ DeviceGuard02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e4ba2-112">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="e4ba2-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4ba2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4ba2-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4ba2-114">Properties</span></span>

<span data-ttu-id="e4ba2-115">Die **MDM- \_ Richtlinie \_ Result01 \_ DeviceGuard02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e4ba2-115">The **MDM\_Policy\_Result01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e4ba2-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="e4ba2-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4ba2-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4ba2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4ba2-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4ba2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4ba2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e4ba2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4ba2-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4ba2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4ba2-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4ba2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4ba2-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4ba2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e4ba2-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="e4ba2-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4ba2-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4ba2-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4ba2-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4ba2-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4ba2-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e4ba2-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4ba2-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e4ba2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4ba2-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e4ba2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4ba2-129">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4ba2-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e4ba2-130">Requirements platformsecurityfeatures</span><span class="sxs-lookup"><span data-stu-id="e4ba2-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4ba2-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e4ba2-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4ba2-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e4ba2-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4ba2-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4ba2-133">Requirements</span></span>



| <span data-ttu-id="e4ba2-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4ba2-134">Requirement</span></span> | <span data-ttu-id="e4ba2-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e4ba2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ba2-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4ba2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ba2-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4ba2-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4ba2-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4ba2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ba2-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e4ba2-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e4ba2-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4ba2-140">Namespace</span></span><br/>                | <span data-ttu-id="e4ba2-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e4ba2-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e4ba2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e4ba2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4ba2-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e4ba2-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4ba2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e4ba2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4ba2-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4ba2-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

