---
description: Dienst zum Erstellen, zerstören und Exportieren von Bezugspunkten.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347004"
---
# <a name="msvm_collectionreferencepointservice-class"></a><span data-ttu-id="79ed3-103">MSVM \_ collectionreferencepointservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="79ed3-103">Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="79ed3-104">Dienst zum Erstellen, zerstören und Exportieren von Bezugspunkten</span><span class="sxs-lookup"><span data-stu-id="79ed3-104">Service to create, destroy and export reference points</span></span>

<span data-ttu-id="79ed3-105">von virtuellen System Sammlungen.</span><span class="sxs-lookup"><span data-stu-id="79ed3-105">of virtual system collections.</span></span>

<span data-ttu-id="79ed3-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="79ed3-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79ed3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79ed3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="79ed3-108">Member</span><span class="sxs-lookup"><span data-stu-id="79ed3-108">Members</span></span>

<span data-ttu-id="79ed3-109">Die **MSVM \_ collectionreferencepointservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="79ed3-109">The **Msvm\_CollectionReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="79ed3-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="79ed3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="79ed3-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="79ed3-111">Methods</span></span>

<span data-ttu-id="79ed3-112">Die **MSVM \_ collectionreferencepointservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="79ed3-112">The **Msvm\_CollectionReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="79ed3-113">Methode</span><span class="sxs-lookup"><span data-stu-id="79ed3-113">Method</span></span>                                                                                      | <span data-ttu-id="79ed3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79ed3-114">Description</span></span>                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79ed3-115">**"Kreatereferencepoint"**</span><span class="sxs-lookup"><span data-stu-id="79ed3-115">**CreateReferencePoint**</span></span>](msvm-collectionreferencepointservice-createreferencepoint.md)   | <span data-ttu-id="79ed3-116">Erstellt einen Referenzpunkt einer Sammlung virtueller Systeme.</span><span class="sxs-lookup"><span data-stu-id="79ed3-116">Creates a reference point of a virtual system collection.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="79ed3-117">**Destroyreferencepoint**</span><span class="sxs-lookup"><span data-stu-id="79ed3-117">**DestroyReferencePoint**</span></span>](msvm-collectionreferencepointservice-destroyreferencepoint.md) | <span data-ttu-id="79ed3-118">Zerstört eine vorhandene Verweis Punkt Auflistung.</span><span class="sxs-lookup"><span data-stu-id="79ed3-118">Destroys an existing reference point collection.</span></span> <span data-ttu-id="79ed3-119">Diese Methode kann als Nebeneffekt andere Verweis Punkte zerstören, die von der betroffenen Verweis Punkt Auflistung abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="79ed3-119">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span><br/>                      |
| [<span data-ttu-id="79ed3-120">**Exportreferencepoint**</span><span class="sxs-lookup"><span data-stu-id="79ed3-120">**ExportReferencePoint**</span></span>](msvm-collectionreferencepointservice-exportreferencepoint.md)   | <span data-ttu-id="79ed3-121">Exportiert eine Verweis Punkt Auflistung in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="79ed3-121">Exports a reference point collection to a file.</span></span> <span data-ttu-id="79ed3-122">In der resultierenden Datei werden die Verweis Punkt Auflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="79ed3-122">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |
| [<span data-ttu-id="79ed3-123">**Removeassociateddata**</span><span class="sxs-lookup"><span data-stu-id="79ed3-123">**RemoveAssociatedData**</span></span>](msvm-collectionreferencepointservice-removeassociateddata.md)   | <span data-ttu-id="79ed3-124">Entfernt das dem Bezugspunkt zugeordnete Datenprotokoll.</span><span class="sxs-lookup"><span data-stu-id="79ed3-124">Removes the data log associated with the reference point.</span></span><br/>                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="79ed3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79ed3-125">Requirements</span></span>



| <span data-ttu-id="79ed3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79ed3-126">Requirement</span></span> | <span data-ttu-id="79ed3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="79ed3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79ed3-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79ed3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="79ed3-129">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79ed3-129">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="79ed3-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79ed3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="79ed3-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="79ed3-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="79ed3-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="79ed3-132">Namespace</span></span><br/>                | <span data-ttu-id="79ed3-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="79ed3-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79ed3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="79ed3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79ed3-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="79ed3-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79ed3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="79ed3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79ed3-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79ed3-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79ed3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79ed3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ed3-139">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="79ed3-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




