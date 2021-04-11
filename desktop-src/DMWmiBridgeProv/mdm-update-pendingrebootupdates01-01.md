---
title: MDM_Update_PendingRebootUpdates01_01-Klasse
description: Die Klasse MDM \_ Update \_ PendingRebootUpdates01 \_ 01 wird zum Verwalten von Updates verwendet, die beim Neustart ausstehend sind.
ms.assetid: 752cdaaa-7883-43d4-be7d-7da9ad15d041
keywords:
- MDM_Update_PendingRebootUpdates01_01-Klasse
- MDM_Update_PendingRebootUpdates01_01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01.InstanceID
- MDM_Update_PendingRebootUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca640a4de00ea9eb115b999129a16dd0bf930cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105717"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a><span data-ttu-id="71f3d-105">MDM- \_ Update \_ PendingRebootUpdates01 01- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="71f3d-105">MDM\_Update\_PendingRebootUpdates01\_01 class</span></span>

<span data-ttu-id="71f3d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="71f3d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="71f3d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="71f3d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="71f3d-108">Die Klasse **MDM \_ Update \_ PendingRebootUpdates01 \_ 01** wird zum Verwalten von Updates verwendet, die beim Neustart ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="71f3d-108">The **MDM\_Update\_PendingRebootUpdates01\_01** class is used to manage updates that are pending on reboot.</span></span>

<span data-ttu-id="71f3d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="71f3d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f3d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="71f3d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_PendingRebootUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime InstalledTime;
};
```

## <a name="members"></a><span data-ttu-id="71f3d-111">Member</span><span class="sxs-lookup"><span data-stu-id="71f3d-111">Members</span></span>

<span data-ttu-id="71f3d-112">Die **MDM- \_ Update- \_ PendingRebootUpdates01 \_ 01** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="71f3d-112">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="71f3d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71f3d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71f3d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71f3d-114">Properties</span></span>

<span data-ttu-id="71f3d-115">Die **MDM-Update-Klasse \_ \_ PendingRebootUpdates01 \_ 01** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="71f3d-115">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="71f3d-116">Installedtime</span><span class="sxs-lookup"><span data-stu-id="71f3d-116">InstalledTime</span></span>](/windows/client-management/mdm/update-csp#pendingrebootupdates-pending-reboot-update-guid-installedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f3d-117">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="71f3d-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71f3d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="71f3d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="71f3d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="71f3d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f3d-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71f3d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f3d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71f3d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f3d-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71f3d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71f3d-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="71f3d-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="71f3d-124">Bei dieser Klasse ist die Zeichenfolge die GUID des Updates, für das ein Neustart aussteht.</span><span class="sxs-lookup"><span data-stu-id="71f3d-124">For this class, the string is the GUID of the update that is pending reboot.</span></span>

</dd> <dt>

<span data-ttu-id="71f3d-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="71f3d-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71f3d-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71f3d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71f3d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71f3d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71f3d-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71f3d-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71f3d-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="71f3d-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="71f3d-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Update/PendingRebootUpdates".</span><span class="sxs-lookup"><span data-stu-id="71f3d-130">For this class, the string is "./Vendor/MSFT/Update/PendingRebootUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71f3d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71f3d-131">Requirements</span></span>



| <span data-ttu-id="71f3d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71f3d-132">Requirement</span></span> | <span data-ttu-id="71f3d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="71f3d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f3d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71f3d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="71f3d-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71f3d-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="71f3d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71f3d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="71f3d-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="71f3d-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="71f3d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="71f3d-138">Namespace</span></span><br/>                | <span data-ttu-id="71f3d-139">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="71f3d-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="71f3d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="71f3d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71f3d-141"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="71f3d-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="71f3d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="71f3d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71f3d-143"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="71f3d-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

