---
description: Stellt einen Dienst dar, der virtuelle Systeme verwaltet.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9db9e85e158f546a3a8780f1211ecd7a7dfc3c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360493"
---
# <a name="cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="4ad1d-103">CIM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="4ad1d-103">CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4ad1d-104">Stellt einen Dienst dar, der virtuelle Systeme verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-104">Represents a service that manages virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad1d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ad1d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="4ad1d-106">Member</span><span class="sxs-lookup"><span data-stu-id="4ad1d-106">Members</span></span>

<span data-ttu-id="4ad1d-107">Die **CIM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ad1d-107">The **CIM\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="4ad1d-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ad1d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4ad1d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="4ad1d-109">Methods</span></span>

<span data-ttu-id="4ad1d-110">Die **CIM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-110">The **CIM\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="4ad1d-111">Methode</span><span class="sxs-lookup"><span data-stu-id="4ad1d-111">Method</span></span>                                                                                      | <span data-ttu-id="4ad1d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ad1d-112">Description</span></span>                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ad1d-113">**Adresssourcesettings**</span><span class="sxs-lookup"><span data-stu-id="4ad1d-113">**AddResourceSettings**</span></span>](cim-virtualsystemmanagementservice-addresourcesettings.md)       | <span data-ttu-id="4ad1d-114">Fügt der Konfiguration eines virtuellen Systems Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-114">Adds resources to a virtual system configuration.</span></span><br/>                          |
| [<span data-ttu-id="4ad1d-115">**Definesystem**</span><span class="sxs-lookup"><span data-stu-id="4ad1d-115">**DefineSystem**</span></span>](cim-virtualsystemmanagementservice-definesystem.md)                     | <span data-ttu-id="4ad1d-116">Definiert ein virtuelles System.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-116">Defines a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="4ad1d-117">**Destroysystem**</span><span class="sxs-lookup"><span data-stu-id="4ad1d-117">**DestroySystem**</span></span>](cim-virtualsystemmanagementservice-destroysystem.md)                   | <span data-ttu-id="4ad1d-118">Löscht ein virtuelles System.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-118">Deletes a virtual system.</span></span><br/>                                                  |
| [<span data-ttu-id="4ad1d-119">**Modifyresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="4ad1d-119">**ModifyResourceSettings**</span></span>](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | <span data-ttu-id="4ad1d-120">Ändert die Einstellungen der virtuellen Ressource für eine virtuelle Systemkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-120">Modifies the virtual resource settings for a virtual system configuration.</span></span><br/> |
| [<span data-ttu-id="4ad1d-121">**Modifysystemsettings**</span><span class="sxs-lookup"><span data-stu-id="4ad1d-121">**ModifySystemSettings**</span></span>](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | <span data-ttu-id="4ad1d-122">Ändert die Einstellungen des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-122">Modifies virtual system settings.</span></span><br/>                                          |
| [<span data-ttu-id="4ad1d-123">**Removeresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="4ad1d-123">**RemoveResourceSettings**</span></span>](cim-virtualsystemmanagementservice-removeresourcesettings.md) | <span data-ttu-id="4ad1d-124">Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="4ad1d-124">Removes virtual resource settings from a virtual system configuration.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="4ad1d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ad1d-125">Requirements</span></span>



| <span data-ttu-id="4ad1d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ad1d-126">Requirement</span></span> | <span data-ttu-id="4ad1d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4ad1d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad1d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ad1d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad1d-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ad1d-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4ad1d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ad1d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad1d-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ad1d-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4ad1d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ad1d-132">Namespace</span></span><br/>                | <span data-ttu-id="4ad1d-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ad1d-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ad1d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4ad1d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ad1d-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4ad1d-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ad1d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4ad1d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ad1d-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ad1d-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ad1d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ad1d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad1d-139">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="4ad1d-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




