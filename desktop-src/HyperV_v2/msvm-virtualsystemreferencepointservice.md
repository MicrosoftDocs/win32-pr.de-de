---
description: Beschreibt einen Referenzpunkt Dienst für virtuelle Systeme.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357149"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="c19f9-103">MSVM \_ virtualsystemreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="c19f9-103">Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="c19f9-104">Beschreibt einen Referenzpunkt Dienst für virtuelle Systeme.</span><span class="sxs-lookup"><span data-stu-id="c19f9-104">Describes a virtual system reference point service.</span></span>

<span data-ttu-id="c19f9-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c19f9-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c19f9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c19f9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="c19f9-107">Member</span><span class="sxs-lookup"><span data-stu-id="c19f9-107">Members</span></span>

<span data-ttu-id="c19f9-108">Die **MSVM \_ virtualsystemreferencepointservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c19f9-108">The **Msvm\_VirtualSystemReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="c19f9-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="c19f9-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c19f9-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="c19f9-110">Methods</span></span>

<span data-ttu-id="c19f9-111">Die **MSVM \_ virtualsystemreferencepointservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c19f9-111">The **Msvm\_VirtualSystemReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="c19f9-112">Methode</span><span class="sxs-lookup"><span data-stu-id="c19f9-112">Method</span></span>                                                                                                       | <span data-ttu-id="c19f9-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c19f9-113">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="c19f9-114">**"Kreatereferencepoint"**</span><span class="sxs-lookup"><span data-stu-id="c19f9-114">**CreateReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | <span data-ttu-id="c19f9-115">Erstellt einen Referenzpunkt eines virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="c19f9-115">Creates a reference point of a virtual system.</span></span><br/>            |
| [<span data-ttu-id="c19f9-116">**Destroyreferencepoint**</span><span class="sxs-lookup"><span data-stu-id="c19f9-116">**DestroyReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | <span data-ttu-id="c19f9-117">Löscht den angegebenen Verweis Punkt.</span><span class="sxs-lookup"><span data-stu-id="c19f9-117">Deletes the specified reference point.</span></span><br/>                    |
| [<span data-ttu-id="c19f9-118">**Exportreferencepoint**</span><span class="sxs-lookup"><span data-stu-id="c19f9-118">**ExportReferencePoint**</span></span>](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | <span data-ttu-id="c19f9-119">Exportiert den Verweis Punkt des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="c19f9-119">Exports the reference point of the virtual system.</span></span><br/>        |
| [<span data-ttu-id="c19f9-120">**Importreferencepointmetadata**</span><span class="sxs-lookup"><span data-stu-id="c19f9-120">**ImportReferencePointMetadata**</span></span>](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | <span data-ttu-id="c19f9-121">Importiert Verweis Punkt Metadaten des virtuellen Systems.</span><span class="sxs-lookup"><span data-stu-id="c19f9-121">Imports reference point metadata of the virtual system.</span></span><br/>   |
| [<span data-ttu-id="c19f9-122">**Removeassociateddata**</span><span class="sxs-lookup"><span data-stu-id="c19f9-122">**RemoveAssociatedData**</span></span>](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | <span data-ttu-id="c19f9-123">Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.</span><span class="sxs-lookup"><span data-stu-id="c19f9-123">Removes the data log associated with the reference point.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c19f9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c19f9-124">Requirements</span></span>



| <span data-ttu-id="c19f9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c19f9-125">Requirement</span></span> | <span data-ttu-id="c19f9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c19f9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c19f9-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c19f9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c19f9-128">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c19f9-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c19f9-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c19f9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c19f9-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c19f9-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c19f9-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c19f9-131">Namespace</span></span><br/>                | <span data-ttu-id="c19f9-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c19f9-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c19f9-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c19f9-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c19f9-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c19f9-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c19f9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c19f9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c19f9-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c19f9-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c19f9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c19f9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c19f9-138">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="c19f9-138">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




