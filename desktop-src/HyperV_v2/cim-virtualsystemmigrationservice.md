---
description: Stellt einen Dienst dar, der die Migration virtueller Systeme zwischen Hostsystemen steuert. Diese Klasse überprüft auch, ob eine ausstehende Migration wahrscheinlich erfolgreich ist.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864572"
---
# <a name="cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="7c43d-104">CIM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7c43d-104">CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="7c43d-105">Stellt einen Dienst dar, der die Migration virtueller Systeme zwischen Hostsystemen steuert.</span><span class="sxs-lookup"><span data-stu-id="7c43d-105">Represents a service that controls the migration of virtual systems between host systems.</span></span> <span data-ttu-id="7c43d-106">Diese Klasse überprüft auch, ob eine ausstehende Migration wahrscheinlich erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="7c43d-106">This class also verifies whether a pending migration is likely to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c43d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c43d-107">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="7c43d-108">Member</span><span class="sxs-lookup"><span data-stu-id="7c43d-108">Members</span></span>

<span data-ttu-id="7c43d-109">Die **CIM- \_ virtualsystemmigrationservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7c43d-109">The **CIM\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="7c43d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7c43d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7c43d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7c43d-111">Methods</span></span>

<span data-ttu-id="7c43d-112">Die **CIM \_ virtualsystemmigrationservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7c43d-112">The **CIM\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="7c43d-113">Methode</span><span class="sxs-lookup"><span data-stu-id="7c43d-113">Method</span></span>                                                                                                                     | <span data-ttu-id="7c43d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c43d-114">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c43d-115">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="7c43d-115">**CheckVirtualSystemIsMigratableToHost**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | <span data-ttu-id="7c43d-116">Überprüft, ob eine ausstehende Migration eines virtuellen Systems zu einem Host wahrscheinlich erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="7c43d-116">Verifies whether a pending virtual system migration to a host is likely to succeed.</span></span><br/>   |
| [<span data-ttu-id="7c43d-117">**CheckVirtualSystemIsMigratableToSystem**</span><span class="sxs-lookup"><span data-stu-id="7c43d-117">**CheckVirtualSystemIsMigratableToSystem**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | <span data-ttu-id="7c43d-118">Überprüft, ob eine ausstehende Migration eines virtuellen Systems zu einem System wahrscheinlich erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="7c43d-118">Verifies whether a pending virtual system migration to a system is likely to succeed.</span></span><br/> |
| [<span data-ttu-id="7c43d-119">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="7c43d-119">**MigrateVirtualSystemToHost**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | <span data-ttu-id="7c43d-120">Migriert ein virtuelles System zu einem Zielhost.</span><span class="sxs-lookup"><span data-stu-id="7c43d-120">Migrates a virtual system to a target host.</span></span><br/>                                           |
| [<span data-ttu-id="7c43d-121">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="7c43d-121">**MigrateVirtualSystemToSystem**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | <span data-ttu-id="7c43d-122">Migriert ein virtuelles System zum Zielsystem.</span><span class="sxs-lookup"><span data-stu-id="7c43d-122">Migrates a virtual system to target system.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="7c43d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c43d-123">Requirements</span></span>



| <span data-ttu-id="7c43d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c43d-124">Requirement</span></span> | <span data-ttu-id="7c43d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7c43d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c43d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c43d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7c43d-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7c43d-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7c43d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c43d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7c43d-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c43d-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7c43d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c43d-130">Namespace</span></span><br/>                | <span data-ttu-id="7c43d-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7c43d-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7c43d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7c43d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c43d-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c43d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7c43d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c43d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c43d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c43d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c43d-137">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="7c43d-137">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




