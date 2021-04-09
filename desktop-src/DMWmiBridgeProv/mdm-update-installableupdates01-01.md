---
title: MDM_Update_InstallableUpdates01_01-Klasse
description: Die MDM \_ Update \_ InstallableUpdates01 \_ 01-Klasse wird verwendet, um das Rollout genehmigter Updates zu verwalten und zu steuern.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- MDM_Update_InstallableUpdates01_01-Klasse
- MDM_Update_InstallableUpdates01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bcb9dd3ec026e6894d4ba7155cc41f12bc01e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858670"
---
# <a name="mdm_update_installableupdates01_01-class"></a><span data-ttu-id="87b7e-105">MDM- \_ Update \_ InstallableUpdates01 01- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="87b7e-105">MDM\_Update\_InstallableUpdates01\_01 class</span></span>

<span data-ttu-id="87b7e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="87b7e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="87b7e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="87b7e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="87b7e-108">Die **MDM \_ Update \_ InstallableUpdates01 \_ 01** -Klasse wird verwendet, um das Rollout genehmigter Updates zu verwalten und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="87b7e-108">The **MDM\_Update\_InstallableUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="87b7e-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="87b7e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b7e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="87b7e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a><span data-ttu-id="87b7e-111">Member</span><span class="sxs-lookup"><span data-stu-id="87b7e-111">Members</span></span>

<span data-ttu-id="87b7e-112">Die **MDM- \_ Update- \_ InstallableUpdates01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="87b7e-112">The **MDM\_Update\_InstallableUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="87b7e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87b7e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87b7e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87b7e-114">Properties</span></span>

<span data-ttu-id="87b7e-115">Die **MDM-Update-Klasse \_ \_ InstallableUpdates01 \_ 01** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="87b7e-115">The **MDM\_Update\_InstallableUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87b7e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="87b7e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87b7e-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="87b7e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87b7e-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="87b7e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87b7e-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87b7e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="87b7e-120">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="87b7e-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="87b7e-121">Bei dieser Klasse ist die Zeichenfolge die GUID des genehmigten Updates.</span><span class="sxs-lookup"><span data-stu-id="87b7e-121">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="87b7e-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="87b7e-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87b7e-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="87b7e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87b7e-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="87b7e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87b7e-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87b7e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="87b7e-126">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="87b7e-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="87b7e-127">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Update/InstallableUpdates".</span><span class="sxs-lookup"><span data-stu-id="87b7e-127">For this class, the string is "./Vendor/MSFT/Update/InstallableUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="87b7e-128">RevisionNumber</span><span class="sxs-lookup"><span data-stu-id="87b7e-128">RevisionNumber</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="87b7e-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="87b7e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="87b7e-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="87b7e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="87b7e-131">Type</span><span class="sxs-lookup"><span data-stu-id="87b7e-131">Type</span></span>](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="87b7e-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="87b7e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="87b7e-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="87b7e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87b7e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87b7e-134">Requirements</span></span>



| <span data-ttu-id="87b7e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87b7e-135">Requirement</span></span> | <span data-ttu-id="87b7e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="87b7e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b7e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87b7e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="87b7e-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87b7e-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="87b7e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87b7e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="87b7e-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="87b7e-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="87b7e-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="87b7e-141">Namespace</span></span><br/>                | <span data-ttu-id="87b7e-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="87b7e-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="87b7e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="87b7e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87b7e-144"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="87b7e-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="87b7e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="87b7e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87b7e-146"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="87b7e-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

