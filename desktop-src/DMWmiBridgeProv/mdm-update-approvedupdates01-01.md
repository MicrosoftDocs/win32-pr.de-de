---
title: MDM_Update_ApprovedUpdates01_01-Klasse
description: Die MDM \_ Update \_ ApprovedUpdates01 \_ 01-Klasse wird verwendet, um das Rollout genehmigter Updates zu verwalten und zu steuern.
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- MDM_Update_ApprovedUpdates01_01-Klasse
- MDM_Update_ApprovedUpdates01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949446"
---
# <a name="mdm_update_approvedupdates01_01-class"></a><span data-ttu-id="663aa-105">MDM- \_ Update \_ ApprovedUpdates01 01- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="663aa-105">MDM\_Update\_ApprovedUpdates01\_01 class</span></span>

<span data-ttu-id="663aa-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="663aa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="663aa-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="663aa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="663aa-108">Die **MDM \_ Update \_ ApprovedUpdates01 \_ 01** -Klasse wird verwendet, um das Rollout genehmigter Updates zu verwalten und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="663aa-108">The **MDM\_Update\_ApprovedUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="663aa-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="663aa-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="663aa-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="663aa-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a><span data-ttu-id="663aa-111">Member</span><span class="sxs-lookup"><span data-stu-id="663aa-111">Members</span></span>

<span data-ttu-id="663aa-112">Die **MDM- \_ Update- \_ ApprovedUpdates01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="663aa-112">The **MDM\_Update\_ApprovedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="663aa-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="663aa-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="663aa-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="663aa-114">Properties</span></span>

<span data-ttu-id="663aa-115">Die **MDM-Update-Klasse \_ \_ ApprovedUpdates01 \_ 01** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="663aa-115">The **MDM\_Update\_ApprovedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="663aa-116">Approvedtime</span><span class="sxs-lookup"><span data-stu-id="663aa-116">ApprovedTime</span></span>](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="663aa-117">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="663aa-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="663aa-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="663aa-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="663aa-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="663aa-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="663aa-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="663aa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="663aa-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="663aa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="663aa-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="663aa-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="663aa-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="663aa-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="663aa-124">Bei dieser Klasse ist die Zeichenfolge die GUID des genehmigten Updates.</span><span class="sxs-lookup"><span data-stu-id="663aa-124">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="663aa-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="663aa-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="663aa-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="663aa-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="663aa-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="663aa-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="663aa-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="663aa-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="663aa-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="663aa-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="663aa-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Update/ApprovedUpdates".</span><span class="sxs-lookup"><span data-stu-id="663aa-130">For this class, the string is "./Vendor/MSFT/Update/ApprovedUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="663aa-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="663aa-131">Requirements</span></span>



| <span data-ttu-id="663aa-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="663aa-132">Requirement</span></span> | <span data-ttu-id="663aa-133">Wert</span><span class="sxs-lookup"><span data-stu-id="663aa-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="663aa-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="663aa-134">Minimum supported client</span></span><br/> | <span data-ttu-id="663aa-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="663aa-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="663aa-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="663aa-136">Minimum supported server</span></span><br/> | <span data-ttu-id="663aa-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="663aa-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="663aa-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="663aa-138">Namespace</span></span><br/>                | <span data-ttu-id="663aa-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="663aa-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="663aa-140">MOF</span><span class="sxs-lookup"><span data-stu-id="663aa-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="663aa-141"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="663aa-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="663aa-142">DLL</span><span class="sxs-lookup"><span data-stu-id="663aa-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="663aa-143"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="663aa-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

