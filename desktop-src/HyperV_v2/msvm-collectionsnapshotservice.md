---
description: Dienst zum Erstellen, zerstören und Exportieren von Snapshot Collection von virtuellen Systemen.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348532"
---
# <a name="msvm_collectionsnapshotservice-class"></a><span data-ttu-id="16e78-103">MSVM \_ collectionsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="16e78-103">Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="16e78-104">Dienst zum Erstellen, zerstören und Exportieren von Snapshot Collection von virtuellen Systemen.</span><span class="sxs-lookup"><span data-stu-id="16e78-104">Service to create, destroy and export snapshot collection of virtual systems.</span></span>

<span data-ttu-id="16e78-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16e78-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e78-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16e78-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="16e78-107">Member</span><span class="sxs-lookup"><span data-stu-id="16e78-107">Members</span></span>

<span data-ttu-id="16e78-108">Die **MSVM \_ collectionsnapshotservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="16e78-108">The **Msvm\_CollectionSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="16e78-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="16e78-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16e78-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="16e78-110">Methods</span></span>

<span data-ttu-id="16e78-111">Die **MSVM \_ collectionsnapshotservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="16e78-111">The **Msvm\_CollectionSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="16e78-112">Methode</span><span class="sxs-lookup"><span data-stu-id="16e78-112">Method</span></span>                                                                                    | <span data-ttu-id="16e78-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16e78-113">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e78-114">**Applysnapshot**</span><span class="sxs-lookup"><span data-stu-id="16e78-114">**ApplySnapshot**</span></span>](msvm-collectionsnapshotservice-applysnapshot.md)                     | <span data-ttu-id="16e78-115">Wendet eine Momentaufnahme Sammlung auf die Sammlung des virtuellen Computer Systems an.</span><span class="sxs-lookup"><span data-stu-id="16e78-115">Applies a snapshot collection to the collection of virtual computer system.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="16e78-116">**Converttoreferencepoint**</span><span class="sxs-lookup"><span data-stu-id="16e78-116">**ConvertToReferencePoint**</span></span>](msvm-collectionsnapshotservice-converttoreferencepoint.md) | <span data-ttu-id="16e78-117">Konvertiert eine vorhandene Auflistungs Momentaufnahme in eine Verweis Punkt Auflistung.</span><span class="sxs-lookup"><span data-stu-id="16e78-117">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="16e78-118">Die Momentaufnahme Auflistung wird als Nebeneffekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="16e78-118">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="16e78-119">Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="16e78-119">Only recovery snapshots can be converted to reference points.</span></span><br/>                      |
| [<span data-ttu-id="16e78-120">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="16e78-120">**CreateSnapshot**</span></span>](msvm-collectionsnapshotservice-createsnapshot.md)                   | <span data-ttu-id="16e78-121">Erstellt eine Momentaufnahme einer virtuellen System Sammlung.</span><span class="sxs-lookup"><span data-stu-id="16e78-121">Creates a snapshot of a virtual system collection.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="16e78-122">**Destroysnapshot**</span><span class="sxs-lookup"><span data-stu-id="16e78-122">**DestroySnapshot**</span></span>](msvm-collectionsnapshotservice-destroysnapshot.md)                 | <span data-ttu-id="16e78-123">Zerstört eine vorhandene Momentaufnahme der virtuellen System Sammlung.</span><span class="sxs-lookup"><span data-stu-id="16e78-123">Destroy an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="16e78-124">Diese Methode kann als Nebeneffekt andere Momentaufnahmen zerstören, die von der betroffenen Momentaufnahme abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="16e78-124">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span><br/>                                                   |
| [<span data-ttu-id="16e78-125">**Export Momentaufnahme**</span><span class="sxs-lookup"><span data-stu-id="16e78-125">**ExportSnapshot**</span></span>](msvm-collectionsnapshotservice-exportsnapshot.md)                   | <span data-ttu-id="16e78-126">Exportiert eine Momentaufnahme Sammlung virtueller Computersysteme in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="16e78-126">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="16e78-127">Die Momentaufnahme Sammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.</span><span class="sxs-lookup"><span data-stu-id="16e78-127">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16e78-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16e78-128">Requirements</span></span>



| <span data-ttu-id="16e78-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16e78-129">Requirement</span></span> | <span data-ttu-id="16e78-130">Wert</span><span class="sxs-lookup"><span data-stu-id="16e78-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e78-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16e78-131">Minimum supported client</span></span><br/> | <span data-ttu-id="16e78-132">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16e78-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="16e78-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16e78-133">Minimum supported server</span></span><br/> | <span data-ttu-id="16e78-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="16e78-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="16e78-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="16e78-135">Namespace</span></span><br/>                | <span data-ttu-id="16e78-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="16e78-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16e78-137">MOF</span><span class="sxs-lookup"><span data-stu-id="16e78-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16e78-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="16e78-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16e78-139">DLL</span><span class="sxs-lookup"><span data-stu-id="16e78-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16e78-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16e78-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16e78-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16e78-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e78-142">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="16e78-142">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




