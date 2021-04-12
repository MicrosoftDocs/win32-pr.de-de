---
description: Volume- und LUN-Bindung
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Volume- und LUN-Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218908"
---
# <a name="volume-and-lun-binding"></a><span data-ttu-id="8100f-103">Volume- und LUN-Bindung</span><span class="sxs-lookup"><span data-stu-id="8100f-103">Volume and LUN Binding</span></span>

<span data-ttu-id="8100f-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="8100f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="8100f-105">Die Bindung ist die Erstellung von Volumes oder LUNs.</span><span class="sxs-lookup"><span data-stu-id="8100f-105">Binding is the creation of volumes or LUNs.</span></span> <span data-ttu-id="8100f-106">Volumes bestehen aus Datenträger Blöcken und LUNs bestehen aus Laufwerks Blöcken.</span><span class="sxs-lookup"><span data-stu-id="8100f-106">Volumes consist of disk extents and LUNs consist of drive extents.</span></span> <span data-ttu-id="8100f-107">Die Bindung wählt für einen Satz von Zuordnungen zu physischen Ressourcen aus und erfolgt innerhalb eines Subsystems, innerhalb eines Pakets oder in beiden.</span><span class="sxs-lookup"><span data-stu-id="8100f-107">Binding selects for a set of mappings to physical resources and occurs within a subsystem, within a pack, or both.</span></span> <span data-ttu-id="8100f-108">Alle Anbieter Programme unterstützen eine teilweise gesteuerte Bindung eines Modells, bei dem der Aufrufer nur die Bindungs Attribute eines bestimmten Interesses angibt und es dem Anbieter ermöglicht, den Rest auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8100f-108">All provider programs support partially directed binding a model in which the caller specifies only those binding attributes of particular interest, and allows the provider to choose the rest.</span></span> <span data-ttu-id="8100f-109">Die Vorgänge in VDS für das Binden von Volumes und LUNs sind ähnlich, aber nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="8100f-109">The operations in VDS for binding volumes and LUNs are similar but not identical.</span></span> <span data-ttu-id="8100f-110">Hardware Anbieter können z. b. zusätzliche Bindungs Optionen anbieten.</span><span class="sxs-lookup"><span data-stu-id="8100f-110">For example, hardware providers can offer additional binding options.</span></span>

<span data-ttu-id="8100f-111">VDS unterstützt die folgenden fünf Volume-und LUN-Bindungs Typen für teilweise gesteuerte Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8100f-111">VDS supports the following five volume and LUN binding types for partially directed configurations.</span></span> <span data-ttu-id="8100f-112">(Hardware Anbieter können viele andere Bindungen unterstützen und unterstützen.)</span><span class="sxs-lookup"><span data-stu-id="8100f-112">(Hardware providers can and do support many other bindings.)</span></span>



| <span data-ttu-id="8100f-113">Begriff</span><span class="sxs-lookup"><span data-stu-id="8100f-113">Term</span></span>                                                                                                                                             | <span data-ttu-id="8100f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8100f-114">Description</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8100f-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Einfache</span><span class="sxs-lookup"><span data-stu-id="8100f-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span></span><br/>                                                     | <span data-ttu-id="8100f-116">Lineare Zuordnung mit nur einem zusammenhängenden Block.</span><span class="sxs-lookup"><span data-stu-id="8100f-116">Linear mapping with one and only one contiguous extent.</span></span><br/>                             |
| <span data-ttu-id="8100f-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Übergreifende</span><span class="sxs-lookup"><span data-stu-id="8100f-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Spanned</span></span><br/>                                                 | <span data-ttu-id="8100f-118">Lineare Zuordnung mit mehreren nicht zusammenhängenden Blöcken auf mehreren Datenträgern oder Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="8100f-118">Linear mapping with multiple noncontiguous extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="8100f-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Tem</span><span class="sxs-lookup"><span data-stu-id="8100f-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Striped</span></span><br/>                                                 | <span data-ttu-id="8100f-120">Eine Zuordnung, die zusammenhängende volumeblöcke auf mehrere Datenträger oder Laufwerke erweitert.</span><span class="sxs-lookup"><span data-stu-id="8100f-120">Mapping that interleaves contiguous volume extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="8100f-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Verkehrt</span><span class="sxs-lookup"><span data-stu-id="8100f-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mirrored</span></span><br/>                                             | <span data-ttu-id="8100f-122">Zuordnung, die zwei oder mehr identische Datenkopien verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8100f-122">Mapping that maintains two or more identical data copies.</span></span><br/>                           |
| <span data-ttu-id="8100f-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Stripeset mit Parität</span><span class="sxs-lookup"><span data-stu-id="8100f-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped with parity</span></span><br/> | <span data-ttu-id="8100f-124">Zuordnung, mit der Paritäts Überprüfung-Informationen auf mehrere Datenträger oder Laufwerke verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="8100f-124">Mapping that distributes parity check information across multiple disks or drives.</span></span><br/>  |



 

<span data-ttu-id="8100f-125">VDS erstellt gespiegelte, Stripesets und Stripesets mit Paritäts Bindungen von mehr als einem Element.</span><span class="sxs-lookup"><span data-stu-id="8100f-125">VDS constructs mirrored, striped, and striped with parity bindings from more than one member.</span></span> <span data-ttu-id="8100f-126">Beispielsweise hat eine zwei-Wege-Spiegelung zwei Member.</span><span class="sxs-lookup"><span data-stu-id="8100f-126">For example, a two-way mirror has two members.</span></span> <span data-ttu-id="8100f-127">Jedes Mitglied kann Blöcke auf mehr als einem Datenträger oder Laufwerk belegen.</span><span class="sxs-lookup"><span data-stu-id="8100f-127">Each member can occupy extents on more than one disk or drive.</span></span> <span data-ttu-id="8100f-128">VDS verkettet die Blöcke, um den Member zu bilden, und bindet dann das Volume oder die LUN an die Elemente.</span><span class="sxs-lookup"><span data-stu-id="8100f-128">VDS concatenates the extents to form the member and then binds the volume or LUN on the members.</span></span> <span data-ttu-id="8100f-129">Ein Anbieter kann alle Bindungs Typen oder eine beliebige Teilmenge unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8100f-129">A provider can support all binding types, or any subset.</span></span> <span data-ttu-id="8100f-130">Im VDS-Objektmodell ist jedes Mitglied einer Spiegelung ein unabhängiges Objekt, das als Plex bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="8100f-130">In the VDS object model, each member of a mirror is an independent object called a plex.</span></span>

<span data-ttu-id="8100f-131">Auch hier sind Volume-und LUN-Typen ähnlich, aber nicht exakt.</span><span class="sxs-lookup"><span data-stu-id="8100f-131">Again, volume and LUN types are similar, but not exact.</span></span> <span data-ttu-id="8100f-132">Eine Beschreibung der Volumetypen finden Sie im [Volume-Objekt](volume-object.md). Informationen zu LUN-Typen finden Sie unter dem [LUN-Objekt](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="8100f-132">For a description of volume types, see the [Volume Object](volume-object.md); for LUN types, see the [LUN Object](lun-object.md).</span></span> <span data-ttu-id="8100f-133">Bindungs Typen sind entweder nicht fehlertolerant oder fehlertolerant.</span><span class="sxs-lookup"><span data-stu-id="8100f-133">Binding types are either non-fault tolerant or fault tolerant.</span></span>

### <a name="non-fault-tolerant-binding"></a><span data-ttu-id="8100f-134">Nicht fehlertolerante Bindung</span><span class="sxs-lookup"><span data-stu-id="8100f-134">Non-Fault Tolerant Binding</span></span>

<span data-ttu-id="8100f-135">Nicht fehlertolerante Volumes und LUNs bieten keine Notfall Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="8100f-135">Non-fault tolerant volumes and LUNs do not offer disaster recovery.</span></span> <span data-ttu-id="8100f-136">Wenn eines der Spindeln, das zu einem nicht fehlertoleranten Volume oder einer LUN beiträgt, fehlschlägt, schlägt das gesamte Volume oder die LUN fehl.</span><span class="sxs-lookup"><span data-stu-id="8100f-136">If one of the spindles that contributes to a non-fault tolerant volume or LUN fails, the entire volume or LUN fails.</span></span> <span data-ttu-id="8100f-137">In Exchange für das Risiko von Daten bieten nicht fehlertolerante Volumes und LUNs eine Eingabe-/Ausgabeleistung, die in der Regel der von fehlertoleranten Volumes und LUNs entspricht.</span><span class="sxs-lookup"><span data-stu-id="8100f-137">In exchange for the risk to data, non-fault tolerant volumes and LUNs offer input/output performance that is generally superior to that of fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="8100f-138">VDS unterstützt die folgenden drei nicht fehlertoleranten Typen: einfache, übergreifende und stripesettypen.</span><span class="sxs-lookup"><span data-stu-id="8100f-138">VDS supports the following three non-fault tolerant types: simple, spanned, and striped.</span></span>

<span data-ttu-id="8100f-139">Einfach</span><span class="sxs-lookup"><span data-stu-id="8100f-139">Simple</span></span>

![Diagramm, das einen einfachen nicht fehlertoleranten Typ mit 2 Paketen und 2 Subsystemen anzeigt.](images/vdssimplelunvol.png)

<span data-ttu-id="8100f-141">Übergreifend</span><span class="sxs-lookup"><span data-stu-id="8100f-141">Spanned</span></span>

![Diagramm, das einen übergreifenden, nicht fehlertoleranten Typ mit 1 Pack und 1 Subsystem anzeigt.](images/vdsspanlunvol.png)

<span data-ttu-id="8100f-143">Tem</span><span class="sxs-lookup"><span data-stu-id="8100f-143">Striped</span></span>

![Diagramm, das einen nicht fehlertoleranten Datenträger mit 1 Pack und 1 Subsystem anzeigt.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a><span data-ttu-id="8100f-145">Fehlertolerante Bindung</span><span class="sxs-lookup"><span data-stu-id="8100f-145">Fault Tolerant Binding</span></span>

<span data-ttu-id="8100f-146">Die folgenden fehlertoleranten Volumes und LUNs bieten eine Notfall Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="8100f-146">The following fault tolerant volumes and LUNs offer disaster recovery.</span></span> <span data-ttu-id="8100f-147">Wenn eines der Spindeln, das zu einem fehlertoleranten Volume oder einer LUN beiträgt, fehlschlägt, können die Daten wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8100f-147">If one of the spindles that contributes to a fault tolerant volume or LUN fails, the data can be recovered.</span></span> <span data-ttu-id="8100f-148">In Exchange für die Datensicherheit ist die Eingabe-/Ausgabeleistung von fehlertoleranten Volumes und LUNs in der Regel geringer als bei nicht fehlertoleranten Volumes und LUNs.</span><span class="sxs-lookup"><span data-stu-id="8100f-148">In exchange for data security, the input/output performance of fault tolerant volumes and LUNs is generally inferior to that of non-fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="8100f-149">VDS unterstützt zwei fehlertolerante Typen: gespiegelt und Stripeset mit Parität.</span><span class="sxs-lookup"><span data-stu-id="8100f-149">VDS supports two fault tolerant types: mirrored and striped with parity.</span></span>

<span data-ttu-id="8100f-150">Gespiegelt (drei-Wege-Spiegelung)</span><span class="sxs-lookup"><span data-stu-id="8100f-150">Mirrored (three-way mirror)</span></span>

![Diagramm, das einen gespiegelten (3-Wege-Spiegel) fehlertoleranten Typ anzeigt.](images/vdsmirrorlunvol.png)

<span data-ttu-id="8100f-152">Stripeset mit Parität</span><span class="sxs-lookup"><span data-stu-id="8100f-152">Striped with parity</span></span>

![Diagramm, das ein Stripeset mit einem Paritäts fehlertoleranten Typ anzeigt](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a><span data-ttu-id="8100f-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8100f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8100f-155">Konfigurations Übersicht</span><span class="sxs-lookup"><span data-stu-id="8100f-155">Configuration Overview</span></span>](configuration.md)
</dt> <dt>

[<span data-ttu-id="8100f-156">Volume-Objekt</span><span class="sxs-lookup"><span data-stu-id="8100f-156">Volume Object</span></span>](volume-object.md)
</dt> <dt>

[<span data-ttu-id="8100f-157">LUN-Objekt</span><span class="sxs-lookup"><span data-stu-id="8100f-157">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

