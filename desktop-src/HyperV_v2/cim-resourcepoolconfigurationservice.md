---
description: Verwaltet die Konfiguration von Ressourcenpools mithilfe von Aufträgen.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862864"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="48dff-103">CIM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="48dff-103">CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="48dff-104">Verwaltet die Konfiguration von Ressourcenpools mithilfe von Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="48dff-104">Manages the configuration of resource pools by using jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="48dff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48dff-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="48dff-106">Member</span><span class="sxs-lookup"><span data-stu-id="48dff-106">Members</span></span>

<span data-ttu-id="48dff-107">Die **CIM \_ resourcepoolconfigurationservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="48dff-107">The **CIM\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="48dff-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="48dff-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="48dff-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="48dff-109">Methods</span></span>

<span data-ttu-id="48dff-110">Die **CIM \_ resourcepoolconfigurationservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="48dff-110">The **CIM\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="48dff-111">Methode</span><span class="sxs-lookup"><span data-stu-id="48dff-111">Method</span></span>                                                                                                          | <span data-ttu-id="48dff-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48dff-112">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="48dff-113">**Adresssourcestoresourcepool**</span><span class="sxs-lookup"><span data-stu-id="48dff-113">**AddResourcesToResourcePool**</span></span>](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | <span data-ttu-id="48dff-114">Startet einen Auftrag zum Hinzufügen von Ressourcen zu einem Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="48dff-114">Starts a job to add resources to a resource pool.</span></span><br/>                  |
| [<span data-ttu-id="48dff-115">**Changeparser-sourcepool**</span><span class="sxs-lookup"><span data-stu-id="48dff-115">**ChangeParentResourcePool**</span></span>](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | <span data-ttu-id="48dff-116">Starten Sie einen Auftrag, um den übergeordneten Ressourcenpool eines Ressourcenpools zu ändern.</span><span class="sxs-lookup"><span data-stu-id="48dff-116">Start a job to change the parent resource pool of a resource pool.</span></span><br/> |
| [<span data-ttu-id="48dff-117">**"Kreatechildresourcepool"**</span><span class="sxs-lookup"><span data-stu-id="48dff-117">**CreateChildResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | <span data-ttu-id="48dff-118">Starten Sie einen Auftrag, um einen Ressourcenpool aus einem übergeordneten Ressourcenpool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48dff-118">Start a job to create a resource pool from a parent resource pool.</span></span><br/> |
| [<span data-ttu-id="48dff-119">**CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="48dff-119">**CreateResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | <span data-ttu-id="48dff-120">Startet einen Auftrag, um einen Stamm Ressourcenpool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48dff-120">Starts a job to create a root resource pool.</span></span><br/>                       |
| [<span data-ttu-id="48dff-121">**Deleteresourcepool**</span><span class="sxs-lookup"><span data-stu-id="48dff-121">**DeleteResourcePool**</span></span>](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | <span data-ttu-id="48dff-122">Starten Sie einen Auftrag, um einen Ressourcenpool zu löschen.</span><span class="sxs-lookup"><span data-stu-id="48dff-122">Start a job to delete a resource pool.</span></span><br/>                             |
| [<span data-ttu-id="48dff-123">**Removeresourcesfromresourcepool**</span><span class="sxs-lookup"><span data-stu-id="48dff-123">**RemoveResourcesFromResourcePool**</span></span>](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | <span data-ttu-id="48dff-124">Startet einen Auftrag, um Ressourcen aus einem Ressourcenpool zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="48dff-124">Starts a job to remove resources from a resource pool.</span></span><br/>             |



 

## <a name="requirements"></a><span data-ttu-id="48dff-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48dff-125">Requirements</span></span>



| <span data-ttu-id="48dff-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48dff-126">Requirement</span></span> | <span data-ttu-id="48dff-127">Wert</span><span class="sxs-lookup"><span data-stu-id="48dff-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48dff-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48dff-128">Minimum supported client</span></span><br/> | <span data-ttu-id="48dff-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="48dff-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="48dff-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48dff-130">Minimum supported server</span></span><br/> | <span data-ttu-id="48dff-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="48dff-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="48dff-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="48dff-132">Namespace</span></span><br/>                | <span data-ttu-id="48dff-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="48dff-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="48dff-134">MOF</span><span class="sxs-lookup"><span data-stu-id="48dff-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48dff-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48dff-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48dff-136">DLL</span><span class="sxs-lookup"><span data-stu-id="48dff-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48dff-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48dff-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48dff-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48dff-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48dff-139">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="48dff-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




