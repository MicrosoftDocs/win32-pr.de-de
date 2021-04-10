---
title: MDM_Policy_Result01_Licensing02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Licensing02-Klasse stellt die verfügbaren Lizenzierungsrichtlinien dar.
ms.assetid: 0f3faa78-c9ed-4166-a860-b5096b33772a
keywords:
- MDM_Policy_Result01_Licensing02-Klasse
- MDM_Policy_Result01_Licensing02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Licensing02
- MDM_Policy_Result01_Licensing02.InstanceID
- MDM_Policy_Result01_Licensing02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa40b1aa0ff64ddd360a304f5366f961fc2c993c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040493"
---
# <a name="mdm_policy_result01_licensing02-class"></a><span data-ttu-id="54d2c-105">MDM- \_ Richtlinie \_ Result01 \_ Licensing02-Klasse</span><span class="sxs-lookup"><span data-stu-id="54d2c-105">MDM\_Policy\_Result01\_Licensing02 class</span></span>

<span data-ttu-id="54d2c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="54d2c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="54d2c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="54d2c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="54d2c-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Licensing02** -Klasse stellt die verfügbaren Lizenzierungsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="54d2c-108">The **MDM\_Policy\_Result01\_Licensing02** class represents the licensing policies available.</span></span>

<span data-ttu-id="54d2c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="54d2c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d2c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="54d2c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Licensing02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsEntitlementReactivation;
  sint32 DisallowKMSClientOnlineAVSValidation;
};
```

## <a name="members"></a><span data-ttu-id="54d2c-111">Member</span><span class="sxs-lookup"><span data-stu-id="54d2c-111">Members</span></span>

<span data-ttu-id="54d2c-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Licensing02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="54d2c-112">The **MDM\_Policy\_Result01\_Licensing02** class has these types of members:</span></span>

-   [<span data-ttu-id="54d2c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54d2c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54d2c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54d2c-114">Properties</span></span>

<span data-ttu-id="54d2c-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Licensing02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54d2c-115">The **MDM\_Policy\_Result01\_Licensing02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="54d2c-116">Allowwindowsentitlementreactivation</span><span class="sxs-lookup"><span data-stu-id="54d2c-116">AllowWindowsEntitlementReactivation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-allowwindowsentitlementreactivation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d2c-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="54d2c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54d2c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54d2c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54d2c-119">Disallowkmsclientonlineavsvalidation</span><span class="sxs-lookup"><span data-stu-id="54d2c-119">DisallowKMSClientOnlineAVSValidation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-disallowkmsclientonlineavsvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d2c-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="54d2c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54d2c-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="54d2c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="54d2c-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="54d2c-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d2c-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54d2c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54d2c-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54d2c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d2c-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54d2c-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54d2c-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="54d2c-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="54d2c-127">Für diese Klasse ist die Zeichenfolge "Licensing".</span><span class="sxs-lookup"><span data-stu-id="54d2c-127">For this class, the string is "Licensing".</span></span>

</dd> <dt>

<span data-ttu-id="54d2c-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="54d2c-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54d2c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54d2c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54d2c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54d2c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54d2c-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54d2c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54d2c-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="54d2c-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="54d2c-133">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="54d2c-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54d2c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54d2c-134">Requirements</span></span>



| <span data-ttu-id="54d2c-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54d2c-135">Requirement</span></span> | <span data-ttu-id="54d2c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="54d2c-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d2c-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54d2c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="54d2c-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54d2c-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="54d2c-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54d2c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="54d2c-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="54d2c-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="54d2c-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="54d2c-141">Namespace</span></span><br/>                | <span data-ttu-id="54d2c-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="54d2c-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="54d2c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="54d2c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54d2c-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="54d2c-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="54d2c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="54d2c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54d2c-146"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="54d2c-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

