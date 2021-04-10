---
description: Stellt einen Dienst dar, mit dem Momentaufnahmen virtueller Systeme erstellt, angewendet und gelöscht werden können.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: CIM_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869283"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="0532a-103">CIM \_ virtualsystemsnapshotservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0532a-103">CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="0532a-104">Stellt einen Dienst dar, mit dem Momentaufnahmen virtueller Systeme erstellt, angewendet und gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="0532a-104">Represents a service that can create, apply, and delete snapshots of virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="0532a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0532a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="0532a-106">Member</span><span class="sxs-lookup"><span data-stu-id="0532a-106">Members</span></span>

<span data-ttu-id="0532a-107">Die **CIM \_ virtualsystemsnapshotservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0532a-107">The **CIM\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="0532a-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="0532a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0532a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="0532a-109">Methods</span></span>

<span data-ttu-id="0532a-110">Die **CIM \_ virtualsystemsnapshotservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0532a-110">The **CIM\_VirtualSystemSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="0532a-111">Methode</span><span class="sxs-lookup"><span data-stu-id="0532a-111">Method</span></span>                                                                      | <span data-ttu-id="0532a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0532a-112">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0532a-113">**Applysnapshot**</span><span class="sxs-lookup"><span data-stu-id="0532a-113">**ApplySnapshot**</span></span>](cim-virtualsystemsnapshotservice-applysnapshot.md)     | <span data-ttu-id="0532a-114">Wendet dem virtuellen System eine Momentaufnahme des virtuellen Systems auf das virtuelle Quellsystem an.</span><span class="sxs-lookup"><span data-stu-id="0532a-114">Applies a virtual system snapshot to the virtual system to the source virtual system.</span></span><br/> |
| [<span data-ttu-id="0532a-115">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="0532a-115">**CreateSnapshot**</span></span>](cim-virtualsystemsnapshotservice-createsnapshot.md)   | <span data-ttu-id="0532a-116">Erstellt eine Momentaufnahme eines virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="0532a-116">Creates a snapshot of a virtual system.</span></span><br/>                                               |
| [<span data-ttu-id="0532a-117">**Destroysnapshot**</span><span class="sxs-lookup"><span data-stu-id="0532a-117">**DestroySnapshot**</span></span>](cim-virtualsystemsnapshotservice-destroysnapshot.md) | <span data-ttu-id="0532a-118">Löscht eine Momentaufnahme eines virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="0532a-118">Deletes a virtual system snapshot.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0532a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0532a-119">Requirements</span></span>



| <span data-ttu-id="0532a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0532a-120">Requirement</span></span> | <span data-ttu-id="0532a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0532a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0532a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0532a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0532a-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0532a-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0532a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0532a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0532a-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0532a-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0532a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="0532a-126">Namespace</span></span><br/>                | <span data-ttu-id="0532a-127">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0532a-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0532a-128">MOF</span><span class="sxs-lookup"><span data-stu-id="0532a-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0532a-129"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0532a-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0532a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0532a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0532a-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0532a-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0532a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0532a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0532a-133">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="0532a-133">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




