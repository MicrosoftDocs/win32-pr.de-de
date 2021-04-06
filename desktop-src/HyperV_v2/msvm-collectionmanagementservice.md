---
description: Verwaltet die Sammlungen auf dem Hyper-V-Host.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Msvm_CollectionManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760495"
---
# <a name="msvm_collectionmanagementservice-class"></a><span data-ttu-id="70419-103">MSVM \_ collectionmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="70419-103">Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="70419-104">Verwaltet die Sammlungen auf dem Hyper-V-Host.</span><span class="sxs-lookup"><span data-stu-id="70419-104">Manages the collections on the Hyper-V host.</span></span>

<span data-ttu-id="70419-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="70419-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70419-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="70419-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="70419-107">Member</span><span class="sxs-lookup"><span data-stu-id="70419-107">Members</span></span>

<span data-ttu-id="70419-108">Die **MSVM \_ collectionmanagementservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="70419-108">The **Msvm\_CollectionManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="70419-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="70419-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70419-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="70419-110">Methods</span></span>

<span data-ttu-id="70419-111">Die **MSVM \_ collectionmanagementservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="70419-111">The **Msvm\_CollectionManagementService** class has these methods.</span></span>



| <span data-ttu-id="70419-112">Methode</span><span class="sxs-lookup"><span data-stu-id="70419-112">Method</span></span>                                                                          | <span data-ttu-id="70419-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70419-113">Description</span></span>                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70419-114">**AddMember**</span><span class="sxs-lookup"><span data-stu-id="70419-114">**AddMember**</span></span>](msvm-collectionmanagementservice-addmember.md)                 | <span data-ttu-id="70419-115">Fügt das angegebene managedelta-Element als Member des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="70419-115">Adds the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                           |
| [<span data-ttu-id="70419-116">**Definecollection**</span><span class="sxs-lookup"><span data-stu-id="70419-116">**DefineCollection**</span></span>](msvm-collectionmanagementservice-definecollection.md)   | <span data-ttu-id="70419-117">Erstellt ein neues [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="70419-117">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="70419-118">**Destroycollection**</span><span class="sxs-lookup"><span data-stu-id="70419-118">**DestroyCollection**</span></span>](msvm-collectionmanagementservice-destroycollection.md) | <span data-ttu-id="70419-119">Löscht das angegebene [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="70419-119">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="70419-120">**RemoveMember**</span><span class="sxs-lookup"><span data-stu-id="70419-120">**RemoveMember**</span></span>](msvm-collectionmanagementservice-removemember.md)           | <span data-ttu-id="70419-121">Entfernt das angegebene managedelta-Element als Member des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="70419-121">Removes the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="70419-122">**Removemitgliedbyid**</span><span class="sxs-lookup"><span data-stu-id="70419-122">**RemoveMemberById**</span></span>](msvm-collectionmanagementservice-removememberbyid.md)   | <span data-ttu-id="70419-123">Entfernt das angegebene managedelta-Element als Member der [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) mit dem angegebenen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="70419-123">Removes the specified ManagedElement as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="70419-124">Dies ist auch dann erfolgreich, wenn das Objekt mit diesem Bezeichner nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="70419-124">This will succeed even if the object with that identifier is not present.</span></span><br/> |
| [<span data-ttu-id="70419-125">**Renamecollection**</span><span class="sxs-lookup"><span data-stu-id="70419-125">**RenameCollection**</span></span>](msvm-collectionmanagementservice-renamecollection.md)   | <span data-ttu-id="70419-126">Aktualisiert den Elementname des angegebenen [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="70419-126">Updates the ElementName the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="70419-127">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="70419-127">**StartService**</span></span>](msvm-collectionmanagementservice-startservice.md)           | <span data-ttu-id="70419-128">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="70419-128">Starts the service.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="70419-129">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="70419-129">**StopService**</span></span>](msvm-collectionmanagementservice-stopservice.md)             | <span data-ttu-id="70419-130">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="70419-130">Stops the service.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="70419-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70419-131">Requirements</span></span>



| <span data-ttu-id="70419-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70419-132">Requirement</span></span> | <span data-ttu-id="70419-133">Wert</span><span class="sxs-lookup"><span data-stu-id="70419-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70419-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70419-134">Minimum supported client</span></span><br/> | <span data-ttu-id="70419-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70419-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="70419-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70419-136">Minimum supported server</span></span><br/> | <span data-ttu-id="70419-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="70419-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="70419-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="70419-138">Namespace</span></span><br/>                | <span data-ttu-id="70419-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="70419-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="70419-140">MOF</span><span class="sxs-lookup"><span data-stu-id="70419-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70419-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="70419-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70419-142">DLL</span><span class="sxs-lookup"><span data-stu-id="70419-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70419-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70419-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70419-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70419-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70419-145">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="70419-145">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




