---
title: MDM_Policy_Result01_LockDown02-Klasse
description: Die Result01 Lockdown02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Sperr Richtlinien dar.
ms.assetid: 78eab50e-b1a7-4b96-a848-b8a86a3b82c3
keywords:
- MDM_Policy_Result01_LockDown02-Klasse
- MDM_Policy_Result01_LockDown02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02.InstanceID
- MDM_Policy_Result01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159e2178e3e5600bef4fc366a0cf49b7856ce886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476272"
---
# <a name="mdm_policy_result01_lockdown02-class"></a><span data-ttu-id="0bfd1-105">MDM- \_ Richtlinie \_ Result01 \_ LockDown02-Klasse</span><span class="sxs-lookup"><span data-stu-id="0bfd1-105">MDM\_Policy\_Result01\_LockDown02 class</span></span>

<span data-ttu-id="0bfd1-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0bfd1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0bfd1-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0bfd1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0bfd1-108">Die **\_ \_ Result01 \_ Lockdown02-Klasse der MDM-Richtlinie** stellt die verfügbaren Sperr Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="0bfd1-108">The **MDM\_Policy\_Result01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="0bfd1-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0bfd1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bfd1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bfd1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="0bfd1-111">Member</span><span class="sxs-lookup"><span data-stu-id="0bfd1-111">Members</span></span>

<span data-ttu-id="0bfd1-112">Die **MDM- \_ Richtlinie \_ Result01 \_ LockDown02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0bfd1-112">The **MDM\_Policy\_Result01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="0bfd1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bfd1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bfd1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bfd1-114">Properties</span></span>

<span data-ttu-id="0bfd1-115">Die **MDM- \_ Richtlinie \_ Result01 \_ LockDown02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0bfd1-115">The **MDM\_Policy\_Result01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0bfd1-116">"Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="0bfd1-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfd1-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0bfd1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bfd1-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0bfd1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0bfd1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0bfd1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfd1-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0bfd1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bfd1-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0bfd1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfd1-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0bfd1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0bfd1-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="0bfd1-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="0bfd1-124">Für diese Klasse ist die Zeichenfolge "Lockdown".</span><span class="sxs-lookup"><span data-stu-id="0bfd1-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="0bfd1-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0bfd1-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfd1-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0bfd1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bfd1-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0bfd1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfd1-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0bfd1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0bfd1-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="0bfd1-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="0bfd1-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="0bfd1-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bfd1-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bfd1-131">Requirements</span></span>



| <span data-ttu-id="0bfd1-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bfd1-132">Requirement</span></span> | <span data-ttu-id="0bfd1-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0bfd1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bfd1-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bfd1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0bfd1-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bfd1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0bfd1-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bfd1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0bfd1-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0bfd1-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="0bfd1-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="0bfd1-138">Namespace</span></span><br/>                | <span data-ttu-id="0bfd1-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0bfd1-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="0bfd1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0bfd1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bfd1-141"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0bfd1-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="0bfd1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0bfd1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bfd1-143"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="0bfd1-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

