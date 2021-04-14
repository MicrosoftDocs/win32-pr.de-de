---
description: Diese WMI-Klassen werden in cimwin32. MOF deklariert.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: CIM-WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523107"
---
# <a name="cim-wmi-provider"></a><span data-ttu-id="a2b9c-103">CIM-WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="a2b9c-103">CIM WMI Provider</span></span>

<span data-ttu-id="a2b9c-104">Diese WMI-Klassen werden in cimwin32. MOF deklariert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-104">These WMI classes are declared in CimWin32.mof.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a2b9c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a2b9c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a2b9c-106">**CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-106">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dd>

<span data-ttu-id="a2b9c-107">Eine [**CIM- \_ Aktions**](cim-action.md) Klasse ist ein Vorgang, der Teil eines Prozesses ist, um entweder ein Softwareelement im nächsten Zustand zu erstellen oder das Softwareelement im aktuellen Zustand zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-107">A [**CIM\_Action**](cim-action.md) class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-108">**CIM- \_ Aktions Sequenz**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-108">**CIM\_ActionSequence**</span></span>](cim-actionsequence.md)
</dt> <dd>

<span data-ttu-id="a2b9c-109">Die CIM-Aktion " [**\_ aktionequenz**](cim-actionsequence.md) " definiert eine Reihe von Vorgängen, die das Softwareelement (auf das durch die [**CIM- \_ softwareelementactions**](cim-softwareelementactions.md) -Zuordnung verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-109">The [**CIM\_ActionSequence**](cim-actionsequence.md) association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-110">**CIM- \_ acsiasspare**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-110">**CIM\_ActsAsSpare**</span></span>](cim-actsasspare.md)
</dt> <dd>

<span data-ttu-id="a2b9c-111">Die [**CIM- \_ aczasspare-Zuordnung**](cim-actsasspare.md) gibt an, welche Elemente Spares sein können oder andere aggregierte Elemente ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-111">The [**CIM\_ActsAsSpare**](cim-actsasspare.md) association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="a2b9c-112">Ein Ersatz kann im Modus "Hot-Standby" ausgeführt werden, wie auf Element Weise angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-112">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-113">**CIM- \_ annäheringslots**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-113">**CIM\_AdjacentSlots**</span></span>](cim-adjacentslots.md)
</dt> <dd>

<span data-ttu-id="a2b9c-114">Die [**CIM \_**](cim-adjacentslots.md) -Zuordnungs Slots-Zuordnung beschreibt das Layout von Slots auf einem hostboard oder einer Adapterkarte.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-114">The [**CIM\_AdjacentSlots**](cim-adjacentslots.md) association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="a2b9c-115">Informationen, wie z. b. der Abstand zwischen den Slots und ob Sie "Shared" sind (wenn eine aufgefüllt wird, der andere Slot kann nicht verwendet werden), werden als Zuordnungs Eigenschaften übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-115">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-116">**CIM- \_ aggregatepblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-116">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-117">Die [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) -Klasse bietet zusammenfassende Informationen über adressierbare logische Blöcke, die sich in derselben Speicher Redundanz Gruppe befinden und sich auf demselben physischen Medium befinden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-117">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-118">**CIM \_ aggregatepsextent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-118">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-119">Die [**CIM- \_ aggregatepsextent**](cim-aggregatepsextent.md) -Klasse definiert die Anzahl der adressierbaren logischen Blöcke auf einem einzelnen Speichergerät, ausgenommen logische Blöcke, die als Prüfdaten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-119">The [**CIM\_AggregatePSExtent**](cim-aggregatepsextent.md) class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="a2b9c-120">Wenn Volumesets definiert sind, sind die logischen Blöcke innerhalb eines einzelnen Volumesatzes enthalten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-120">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="a2b9c-121">Dies ist eine alternative Gruppierung für [**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md), wenn nur Zusammenfassungs Informationen benötigt werden oder wenn die automatische Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-121">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-122">**CIM \_ aggregateredundancycomponent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-122">**CIM\_AggregateRedundancyComponent**</span></span>](cim-aggregateredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-123">Die [**CIM- \_ aggregateredundancycomponent**](cim-aggregateredundancycomponent.md) -Klasse beschreibt den aggregierten physischen Block in einer Speicher Redundanz Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-123">The [**CIM\_AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) class describes the aggregate physical extent in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-124">**CIM- \_ alarmdevice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-124">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-125">Die [**CIM \_ alarmdevice**](cim-alarmdevice.md) -Klasse ist ein Alarmgerät, das akustische oder sichtbare Anzeichen für eine Problemsituation ausgibt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-125">The [**CIM\_AlarmDevice**](cim-alarmdevice.md) class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-126">**CIM- \_ Verteilungs Quelle**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-126">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dd>

<span data-ttu-id="a2b9c-127">Die CIM-Klasse " [**\_ Zuweisungs**](cim-allocatedresource.md) Klasse" stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar und zeigt an, dass die Ressource dem Gerät zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-127">The [**CIM\_AllocatedResource**](cim-allocatedresource.md) class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-128">**CIM- \_ applicationsystem**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-128">**CIM\_ApplicationSystem**</span></span>](cim-applicationsystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-129">Die [**CIM \_ applicationsystem**](cim-applicationsystem.md) -Klasse stellt ein Anwendungs-oder Softwaresystem dar, das eine bestimmte Geschäftsfunktion unterstützt, die als unabhängige Einheit verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-129">The [**CIM\_ApplicationSystem**](cim-applicationsystem.md) class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="a2b9c-130">Ein solches System kann mithilfe der [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Klasse in seine funktionalen Komponenten zerlegt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-130">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="a2b9c-131">Die Software Features für eine bestimmte Anwendung oder ein bestimmtes Softwaresystem werden mithilfe der [**CIM \_ applicationsystemsoftwarefeature-Zuordnung**](cim-applicationsystemsoftwarefeature.md) gefunden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-131">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-132">**CIM \_ applicationsystemsoftwarefeature**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-132">**CIM\_ApplicationSystemSoftwareFeature**</span></span>](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="a2b9c-133">Die [**CIM \_ applicationsystemsoftwarefeature**](cim-applicationsystemsoftwarefeature.md) -Klasse stellt eine Zuordnung dar, mit der die Software Features identifiziert werden, die ein bestimmtes Anwendungssystem bilden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-133">The [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="a2b9c-134">Die Software Features können in verschiedene Produkte eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-134">The software features can be included in different products.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-135">**CIM \_ associatedalarm**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-135">**CIM\_AssociatedAlarm**</span></span>](cim-associatedalarm.md)
</dt> <dd>

<span data-ttu-id="a2b9c-136">Die [**CIM \_ associatedalarm**](cim-associatedalarm.md) -Abhängigkeit ordnet einem logischen Gerät einen Alarm zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-136">The [**CIM\_AssociatedAlarm**](cim-associatedalarm.md) dependency associates an alarm with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-137">**CIM \_ associatedakku**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-137">**CIM\_AssociatedBattery**</span></span>](cim-associatedbattery.md)
</dt> <dd>

<span data-ttu-id="a2b9c-138">Die [**CIM \_ associatedakku**](cim-associatedbattery.md) -Abhängigkeit ordnet einen Akku einem logischen Gerät zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-138">The [**CIM\_AssociatedBattery**](cim-associatedbattery.md) dependency associates a battery with a logical device.</span></span> <span data-ttu-id="a2b9c-139">Verwenden Sie diese Zuordnung, um einzelne Batterien zu modellieren, die eine unterbrechungsfreie Stromversorgung (USV) bilden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-139">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-140">**CIM \_ associatedcooling**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-140">**CIM\_AssociatedCooling**</span></span>](cim-associatedcooling.md)
</dt> <dd>

<span data-ttu-id="a2b9c-141">Die [**CIM \_ associatedcooling**](cim-associatedcooling.md) -Zuordnung gibt an, wann die Lüfter oder andere Kühlgeräte für ein Gerät spezifisch sind (im Gegensatz zur Bereitstellung von Gehäuse oder CAB-Kühlung).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-141">The [**CIM\_AssociatedCooling**](cim-associatedcooling.md) association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-142">**CIM \_ associatedmemory**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-142">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> <dd>

<span data-ttu-id="a2b9c-143">Die [**CIM \_ associatememory**](cim-associatedmemory.md) -Klasse ordnet installierten oder zugeordneten Arbeitsspeicher zu, z. b. Cache Speicher mit einem logischen Gerät.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-143">The [**CIM\_AssociateMemory**](cim-associatedmemory.md) class associates installed or associated memory, such as cache memory with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-144">**CIM \_ associatedprocessormemory**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-144">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dd>

<span data-ttu-id="a2b9c-145">Die [**CIM \_ associatedprocessormemory**](cim-associatedprocessormemory.md) -Klasse ordnet den Prozessor-und Systemspeicher oder den Cache eines Prozessors zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-145">The [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md) class associates the processor and system memory, or a processor's cache.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-146">**CIM \_ associatedsensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-146">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-147">Die [**CIM \_ associatedsensor**](cim-associatedsensor.md) -Klasse ordnet einen installierten Sensor einem logischen Gerät zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-147">The [**CIM\_AssociatedSensor**](cim-associatedsensor.md) class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="a2b9c-148">Der Sensor misst wichtige Eingabe-und Ausgabe Eigenschaften und kann im Gerät enthalten oder in der Nähe installiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-148">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-149">**CIM \_ associatedsupplycurrentsensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-149">**CIM\_AssociatedSupplyCurrentSensor**</span></span>](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-150">Die [**CIM \_ associatedsupplycurrentsensor**](cim-associatedsupplycurrentsensor.md) -Klasse ordnet eine Stromversorgung einem aktuellen (AMPERAGE) Sensor zu, der die Eingabe Häufigkeit überwacht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-150">The [**CIM\_AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-151">**CIM \_ associatedsupplyvoltagesensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-151">**CIM\_AssociatedSupplyVoltageSensor**</span></span>](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-152">Verknüpft eine Stromversorgung mit einem Spannungssensor, der die Eingangsspannung überwacht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-152">Associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-153">**CIM- \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-153">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> <dd>

<span data-ttu-id="a2b9c-154">Die [**CIM- \_ BasedOn**](cim-basedon.md) -Klasse stellt eine Zuordnung dar, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-154">The [**CIM\_BasedOn**](cim-basedon.md) class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="a2b9c-155">Physische Blöcke enthalten beispielsweise Blöcke mit geschütztem Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-155">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="a2b9c-156">Volumesätze werden daher aus einem oder mehreren physischen oder geschützten Speicherplatz Blöcken zusammengestellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-156">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="a2b9c-157">Der Cache Speicher kann unabhängig voneinander definiert und in einem physischen Element realisiert werden. er kann aber auch auf flüchtigen oder nicht flüchtigen Speicherblöcken basieren.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-157">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-158">**CIM- \_ Akku**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-158">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dd>

<span data-ttu-id="a2b9c-159">Die [**CIM- \_ Akku**](cim-battery.md) Klasse stellt die Funktionen und die Verwaltung des logischen Akku Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-159">The [**CIM\_Battery**](cim-battery.md) class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="a2b9c-160">Diese Klasse gilt für Akkus in Laptop Systemen und anderen internen und externen Akkus.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-160">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-161">**CIM- \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-161">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-162">Die [**CIM \_ BinarySensor**](cim-binarysensor.md) -Klasse stellt eine boolesche Ausgabe bereit.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-162">The [**CIM\_BinarySensor**](cim-binarysensor.md) class provides a Boolean output.</span></span> <span data-ttu-id="a2b9c-163">Die Eigenschaften " **CurrentState** " und " **possiblestates** " wurden für die sensorung hinzugefügt, sodass die **CIM- \_ BinarySensor** -Unterklasse nicht mehr benötigt wird, obwohl Sie aus Gründen der Abwärtskompatibilität beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-163">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="a2b9c-164">Ein binärer Sensor kann erstellt werden, indem ein Sensor mit zwei möglichen Zuständen instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-164">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-165">**CIM- \_ bioselare**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-165">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dd>

<span data-ttu-id="a2b9c-166">Die [**CIM \_ bioselfigure**](cim-bioselement.md) -Klasse stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-166">The [**CIM\_BIOSElement**](cim-bioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-167">**CIM- \_ biosfeature**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-167">**CIM\_BIOSFeature**</span></span>](cim-biosfeature.md)
</dt> <dd>

<span data-ttu-id="a2b9c-168">stellt die Funktionen der Low-Level-Software dar, die zum Starten und Konfigurieren eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-168">represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-169">**CIM \_ biosfeaturebioselements**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-169">**CIM\_BIOSFeatureBIOSElements**</span></span>](cim-biosfeaturebioselements.md)
</dt> <dd>

<span data-ttu-id="a2b9c-170">Die [**CIM \_ biosfeaturebioselements**](cim-biosfeaturebioselements.md) -Klasse ordnet eine BIOS-Funktion und deren aggregierte BIOS-Elemente zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-170">The [**CIM\_BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) class associates a BIOS feature and its aggregated BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-171">**CIM \_ biosloadedinnv**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-171">**CIM\_BIOSLoadedInNV**</span></span>](cim-biosloadedinnv.md)
</dt> <dd>

<span data-ttu-id="a2b9c-172">Die [**CIM \_ biosloadedinnv**](cim-biosloadedinnv.md) -Klasse ordnet ein BIOS-Element und den nicht flüchtigen Speicher zu, in dem er geladen ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-172">The [**CIM\_BIOSLoadedInNV**](cim-biosloadedinnv.md) class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-173">**CIM \_ bootosfromfs**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-173">**CIM\_BootOSFromFS**</span></span>](cim-bootosfromfs.md)
</dt> <dd>

<span data-ttu-id="a2b9c-174">Die [**CIM \_ bootosfromfs**](cim-bootosfromfs.md) -Klasse ordnet das Betriebssystem und die Dateisysteme zu, von denen das Betriebssystem geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-174">The [**CIM\_BootOSFromFS**](cim-bootosfromfs.md) class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="a2b9c-175">Die Zuordnung ist m:n-. ein verteiltes Betriebssystem kann davon abhängen, dass mehrere Dateisysteme ordnungsgemäß und vollständig geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-175">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-176">**CIM- \_ bootsap**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-176">**CIM\_BootSAP**</span></span>](cim-bootsap.md)
</dt> <dd>

<span data-ttu-id="a2b9c-177">Die [**CIM- \_ bootsap**](cim-bootsap.md) -Klasse stellt die Zugriffspunkte eines Start Dienstanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-177">The [**CIM\_BootSAP**](cim-bootsap.md) class represents the access points of a boot service.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-178">**CIM- \_ Bootservice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-178">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-179">Die [**CIM- \_ Bootservice**](cim-bootservice.md) -Klasse stellt die Funktionalität dar, die von einem Gerät oder einer Software oder von einem Netzwerk bereitgestellt wird, um ein Betriebssystem auf einem einheitlichen Computersystem zu laden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-179">The [**CIM\_BootService**](cim-bootservice.md) class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-180">**CIM \_ bootserviceaccessbysap**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-180">**CIM\_BootServiceAccessBySAP**</span></span>](cim-bootserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="a2b9c-181">Die [**CIM \_ bootserviceaccessbysap**](cim-bootserviceaccessbysap.md) -Klasse ordnet einen Start Dienst und seine Zugriffspunkte zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-181">The [**CIM\_BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) class associates a boot service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-182">**CIM- \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-182">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dd>

<span data-ttu-id="a2b9c-183">Die [**CIM \_ CacheMemory**](cim-cachememory.md) -Klasse definiert die Funktionen und die Verwaltung des Cache Speichers.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-183">The [**CIM\_CacheMemory**](cim-cachememory.md) class defines the capabilities and management of cache memory.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-184">**CIM- \_ Karte**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-184">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dd>

<span data-ttu-id="a2b9c-185">Die [**CIM- \_ Karten**](cim-card.md) Klasse stellt einen Typ von physischem Container dar, der an eine andere Karte oder ein hostingboard angeschlossen werden kann oder selbst ein hostingboard/-Motherboard in einem Chassis ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-185">The [**CIM\_Card**](cim-card.md) class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="a2b9c-186">Diese Klasse enthält alle Pakete, die Signale ausführen können und einen Bereitstellungs Punkt für physische Komponenten bereitstellen, wie z. b. Chips oder andere physische Pakete, wie z. b. andere Karten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-186">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-187">**CIM- \_ cardinslot**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-187">**CIM\_CardInSlot**</span></span>](cim-cardinslot.md)
</dt> <dd>

<span data-ttu-id="a2b9c-188">Die [**CIM \_ cardinslot**](cim-cardinslot.md) -Klasse ordnet eine Adapterkarte dem Container zu, in den Sie eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-188">The [**CIM\_CardInSlot**](cim-cardinslot.md) class associates an adapter card with the container into which it is inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-189">**CIM- \_ kardoncard**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-189">**CIM\_CardOnCard**</span></span>](cim-cardoncard.md)
</dt> <dd>

<span data-ttu-id="a2b9c-190">Die [**CIM \_ cardoncard**](cim-cardoncard.md) -Zuordnung beschreibt die Beziehungen zu Karten, die an den über Ladungen/Baseboards, daughtercards eines Adapters oder Karten mit speziellen Karten ähnlichen Modulen angeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-190">The [**CIM\_CardOnCard**](cim-cardoncard.md) association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-191">**CIM- \_ cdromdrive**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-191">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dd>

<span data-ttu-id="a2b9c-192">Die [**CIM- \_ cdromdrive**](cim-cdromdrive.md) -Klasse stellt ein CD-ROM-Laufwerk auf dem Computer dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-192">The [**CIM\_CDROMDrive**](cim-cdromdrive.md) class represents a CD-ROM drive on the computer.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-193">**CIM- \_ Chassis**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-193">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dd>

<span data-ttu-id="a2b9c-194">Die [**CIM- \_ Chassis**](cim-chassis.md) -Klasse stellt die physischen Elemente dar, die andere Elemente einschließen und definierbare Funktionen bereitstellen, wie z. b. einen Desktop, Verarbeitungs Knoten, UPS, Datenträger-oder Band Speicher oder eine Kombination dieser Elemente.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-194">The [**CIM\_Chassis**](cim-chassis.md) class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-195">**CIM \_ chassisinrack**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-195">**CIM\_ChassisInRack**</span></span>](cim-chassisinrack.md)
</dt> <dd>

<span data-ttu-id="a2b9c-196">Die [**CIM \_ chassisinrack**](cim-chassisinrack.md) -Zuordnung stellt die "enthaltende" Beziehung zwischen einem Gestell und einem darin enthaltenen Chassis dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-196">The [**CIM\_ChassisInRack**](cim-chassisinrack.md) association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-197">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-197">**CIM\_Check**</span></span>](cim-check.md)
</dt> <dd>

<span data-ttu-id="a2b9c-198">Die [**CIM- \_ Check**](cim-check.md) -Klasse stellt eine Bedingung oder ein Merkmal dar, die in einer Umgebung erwartungsgemäß definiert ist, die von einer Instanz einer [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse definiert oder festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-198">The [**CIM\_Check**](cim-check.md) class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="a2b9c-199">Die Überprüfungen, die einem bestimmten Softwareelement zugeordnet sind, werden in einer von zwei Gruppen organisiert, wobei die **Phase** -Eigenschaft der [**CIM- \_ softwareelementchecks**](cim-softwareelementchecks.md) -Zuordnung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-199">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-200">**CIM- \_ Chip**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-200">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> <dd>

<span data-ttu-id="a2b9c-201">Die [**CIM- \_ Chip**](cim-chip.md) Klasse stellt den Typ der integrierten Verbindungs Hardware dar, einschließlich ASICs, Prozessoren, Speicherchips usw.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-201">The [**CIM\_Chip**](cim-chip.md) class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-202">**CIM \_ clusteringsap**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-202">**CIM\_ClusteringSAP**</span></span>](cim-clusteringsap.md)
</dt> <dd>

<span data-ttu-id="a2b9c-203">Die [**CIM \_ clusteringsap**](cim-clusteringsap.md) -Klasse stellt die Zugriffspunkte eines Clustering-Dienstanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-203">The [**CIM\_ClusteringSAP**](cim-clusteringsap.md) class represents the access points of a clustering service.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-204">**CIM- \_ clusteringservice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-204">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-205">Die [**CIM \_ clusteringservice**](cim-clusteringservice.md) -Klasse stellt die Funktionalität dar, die von einem Cluster bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-205">The [**CIM\_ClusteringService**](cim-clusteringservice.md) class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="a2b9c-206">Beispielsweise können Failoverfunktionen als Dienst eines Failoverclusters modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-206">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-207">**CIM \_ clusterserviceaccessbysap**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-207">**CIM\_ClusterServiceAccessBySAP**</span></span>](cim-clusterserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="a2b9c-208">Die [**CIM \_ clusterserviceaccessbysap**](cim-clusterserviceaccessbysap.md) -Klasse stellt die Beziehung zwischen einem Clustering-Dienst und seinen Zugriffs Punkten dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-208">The [**CIM\_ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) class represents the relationship between a clustering service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-209">**CIM \_ collectedcollections**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-209">**CIM\_CollectedCollections**</span></span>](cim-collectedcollections.md)
</dt> <dd>

<span data-ttu-id="a2b9c-210">Die [**CIM \_ collectedcollections**](cim-collectedcollections.md) -Klasse ist eine Aggregations Zuordnung, die eine Auflistung verwalteter System Elemente (MSE) darstellt, die in einer Auflistung von MSES enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-210">The [**CIM\_CollectedCollections**](cim-collectedcollections.md) class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-211">**CIM \_ collectedmses**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-211">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> <dd>

<span data-ttu-id="a2b9c-212">Die [**CIM \_ collectedmses**](cim-collectedmses.md) Association-Klasse stellt die Member des Gruppierungs Objekts dar, eine [**CollectionOfMSEs**](cim-collectionofmses.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-212">The [**CIM\_CollectedMSEs**](cim-collectedmses.md) association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-213">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-213">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> <dd>

<span data-ttu-id="a2b9c-214">Das [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt ermöglicht das Gruppieren von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten zum Zweck der Zuordnung von Einstellungen und Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-214">The [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="a2b9c-215">Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-215">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-216">**CIM \_ collectionofsensors**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-216">**CIM\_CollectionOfSensors**</span></span>](cim-collectionofsensors.md)
</dt> <dd>

<span data-ttu-id="a2b9c-217">Die [**CIM \_ collectionofsensors**](cim-collectionofsensors.md) -Zuordnung stellt die binären Sensoren dar, die den Multistate-Sensor bilden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-217">The [**CIM\_CollectionOfSensors**](cim-collectionofsensors.md) association represents the binary sensors that make up the multistate sensor.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-218">**CIM- \_ CollectionSetting**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-218">**CIM\_CollectionSetting**</span></span>](cim-collectionsetting.md)
</dt> <dd>

<span data-ttu-id="a2b9c-219">Die [**CIM \_ CollectionSetting**](cim-collectionsetting.md) -Klasse stellt die Zuordnung zwischen einem [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) und der Einstellungs Klasse dar, die für Sie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-219">The [**CIM\_CollectionSetting**](cim-collectionsetting.md) class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-220">**CIM- \_ Kompatibilitäts Produkt**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-220">**CIM\_CompatibleProduct**</span></span>](cim-compatibleproduct.md)
</dt> <dd>

<span data-ttu-id="a2b9c-221">Die [**CIM \_ compatibleproduct**](cim-compatibleproduct.md) -Klasse stellt eine Zuordnung zwischen Produkten dar, die angibt, ob zwei referenzierte Produkte interoperabel sind, z. b. ob Sie gemeinsam installiert werden können oder ob es sich um den physischen Container für den anderen handeln kann usw.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-221">The [**CIM\_CompatibleProduct**](cim-compatibleproduct.md) class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-222">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-222">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dd>

<span data-ttu-id="a2b9c-223">Die [**CIM- \_ Komponenten**](cim-component.md) Zuordnung stellt die Bestandteile einer Beziehung zwischen MSES dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-223">The [**CIM\_Component**](cim-component.md) association represents the parts of a relationship between MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-224">**CIM- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-224">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-225">Eine [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse stellt eine spezielle Auflistung von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Instanzen dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-225">A [**CIM\_ComputerSystem**](cim-computersystem.md) class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="a2b9c-226">Diese Sammlung bietet Computerfunktionen und dient als Aggregations Punkt zum Zuordnen eines oder mehrerer der folgenden Elemente: Dateisystem, Betriebssystem, Prozessor und Arbeitsspeicher (flüchtiger und nicht flüchtiger Speicher).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-226">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="a2b9c-227">Diese Klasse wird vom [**CIM- \_ System**](cim-system.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-227">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-228">**CIM \_ computersystemdma**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-228">**CIM\_ComputerSystemDMA**</span></span>](cim-computersystemdma.md)
</dt> <dd>

<span data-ttu-id="a2b9c-229">Die [**CIM \_ computersystemdma**](cim-computersystemdma.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren DMA-Kanälen (Direct Memory Access) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-229">The [**CIM\_ComputerSystemDMA**](cim-computersystemdma.md) class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-230">**CIM \_ computersystemirq**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-230">**CIM\_ComputerSystemIRQ**</span></span>](cim-computersystemirq.md)
</dt> <dd>

<span data-ttu-id="a2b9c-231">Die [**CIM \_ computersystemirq**](cim-computersystemirq.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Interrupt Request Lines (unqs) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-231">The [**CIM\_ComputerSystemIRQ**](cim-computersystemirq.md) class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-232">**CIM \_ computersystemmappedio**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-232">**CIM\_ComputerSystemMappedIO**</span></span>](cim-computersystemmappedio.md)
</dt> <dd>

<span data-ttu-id="a2b9c-233">Die [**CIM \_ computersystemmappedio**](cim-computersystemmappedio.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Speicher Abbild-e/a-Ports dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-233">The [**CIM\_ComputerSystemMappedIO**](cim-computersystemmappedio.md) class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-234">**CIM \_ computersystempackage**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-234">**CIM\_ComputerSystemPackage**</span></span>](cim-computersystempackage.md)
</dt> <dd>

<span data-ttu-id="a2b9c-235">Die [**CIM \_ computersystempackage**](cim-computersystempackage.md) -Klasse stellt eine Zuordnung dar, die explizit die Beziehung zwischen einheitlichen Computersystemen und einem oder mehreren physischen Paketen definiert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-235">The [**CIM\_ComputerSystemPackage**](cim-computersystempackage.md) class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="a2b9c-236">Die Zuordnung ähnelt der Art und Weise, in der logische Geräte durch physische Elemente realisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-236">The association is similar to the way that logical devices are realized by physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-237">**CIM \_ computersystemresource**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-237">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dd>

<span data-ttu-id="a2b9c-238">Die [**CIM \_ computersystemresource**](cim-computersystemresource.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Systemressourcen dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-238">The [**CIM\_ComputerSystemResource**](cim-computersystemresource.md) class represents an association between a computer system and its available system resources.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-239">**CIM- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-239">**CIM\_Configuration**</span></span>](cim-configuration.md)
</dt> <dd>

<span data-ttu-id="a2b9c-240">Das [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt ermöglicht die Gruppierung von Parametersätzen (definiert in [**CIM- \_ Einstellungs**](cim-setting.md) Objekten) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-240">The [**CIM\_Configuration**](cim-configuration.md) object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-241">**CIM \_ connectedto**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-241">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> <dd>

<span data-ttu-id="a2b9c-242">Die [**CIM \_ connectedto**](cim-connectedto.md) -Klasse stellt eine Zuordnung dar, die angibt, dass zwei oder mehr physische Connectors verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-242">The [**CIM\_ConnectedTo**](cim-connectedto.md) class represents an association that indicates that two or more physical connectors are connected.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-243">**CIM \_ connectorionpackage**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-243">**CIM\_ConnectorOnPackage**</span></span>](cim-connectoronpackage.md)
</dt> <dd>

<span data-ttu-id="a2b9c-244">Die [**CIM \_ connectoronpackage**](cim-connectoronpackage.md) -Klasse stellt eine Zuordnung dar, die die Einschluss Beziehung zwischen Connectors und Paketen explizit macht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-244">The [**CIM\_ConnectorOnPackage**](cim-connectoronpackage.md) class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="a2b9c-245">Physische Pakete enthalten Connectors und andere physische Elemente.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-245">Physical packages contain connectors as well as other physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-246">**CIM- \_ Container**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-246">**CIM\_Container**</span></span>](cim-container.md)
</dt> <dd>

<span data-ttu-id="a2b9c-247">Die [**CIM- \_ Container**](cim-container.md) Klasse stellt eine Zuordnung zwischen einem enthaltenen und einem enthaltenden physischen Element dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-247">The [**CIM\_Container**](cim-container.md) class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="a2b9c-248">Ein enthaltende Objekt muss ein physisches Paket sein.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-248">A containing object must be a physical package.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-249">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-249">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dd>

<span data-ttu-id="a2b9c-250">Die [**CIM \_ controlledby**](cim-controlledby.md) -Beziehung gibt an, welche Geräte von dem logischen Controller Gerät befohlen werden bzw. darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-250">The [**CIM\_ControlledBy**](cim-controlledby.md) relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-251">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-251">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-252">Die [**CIM- \_ Controller**](cim-controller.md) Klasse ist eine übergeordnete Klasse zum Gruppieren von verschiedenen Steuerelement bezogenen Geräten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-252">The [**CIM\_Controller**](cim-controller.md) class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="a2b9c-253">Beispiele für Controller sind SCSI-Controller, USB-Controller und serielle Controller.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-253">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-254">**CIM \_ coolingdevice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-254">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-255">Die [**CIM \_ coolingdevice**](cim-coolingdevice.md) -Klasse stellt die Funktionen und die Verwaltung von Kühlgeräten dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-255">The [**CIM\_CoolingDevice**](cim-coolingdevice.md) class represents the capabilities and management of cooling devices.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-256">**CIM- \_ copyfileaction**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-256">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-257">Die [**CIM \_ copyfileaction**](cim-copyfileaction.md) -Klasse stellt das Verschieben oder Kopieren von Dateien von einem Computersystem an einen neuen Speicherort dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-257">The [**CIM\_CopyFileAction**](cim-copyfileaction.md) class represents moving or copying files from a computer system to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-258">**CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-258">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-259">Die CIM-Klasse " [**\_ kreatedirectoryaction**](cim-createdirectoryaction.md) " erstellt leere Verzeichnisse für Software Elemente, die lokal installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-259">The [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class creates empty directories for software elements to be installed locally.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-260">**CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-260">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-261">Die [**CIM \_ CurrentSensor**](cim-currentsensor.md) -Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-261">The [**CIM\_CurrentSensor**](cim-currentsensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-262">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-262">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dd>

<span data-ttu-id="a2b9c-263">Die [**CIM \_ DataFile**](cim-datafile.md) -Klasse stellt eine benannte Auflistung von Daten oder ausführbarem Code dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-263">The [**CIM\_DataFile**](cim-datafile.md) class represents a named collection of data or executable code.</span></span> <span data-ttu-id="a2b9c-264">Es werden nur Instanzen von Dateien auf lokalen Festplatten Datenträgern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-264">Only instances of files on local fixed disks will be returned</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-265">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-265">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dd>

<span data-ttu-id="a2b9c-266">Die [**CIM- \_ Abhängigkeits**](cim-dependency.md) Klasse stellt eine Zuordnung dar, die Abhängigkeitsbeziehungen zwischen Objekten herstellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-266">The [**CIM\_Dependency**](cim-dependency.md) class represents an association that establishes dependency relationships between objects.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-267">**CIM \_ dependencycontext**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-267">**CIM\_DependencyContext**</span></span>](cim-dependencycontext.md)
</dt> <dd>

<span data-ttu-id="a2b9c-268">Die [**CIM \_ dependencycontext**](cim-dependencycontext.md) -Beziehung ordnet eine [**CIM- \_ Abhängigkeits**](cim-dependency.md) Klasse einem oder mehreren [**CIM- \_ Konfigurations**](cim-configuration.md) Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-268">The [**CIM\_DependencyContext**](cim-dependencycontext.md) relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="a2b9c-269">Beispielsweise können die Abhängigkeiten eines Computer Systems je nach Netzwerk, an das das System angefügt ist, geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-269">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-270">**CIM- \_ Desktop Monitor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-270">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-271">Die [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md) -Klasse stellt die Funktionen und die Verwaltung des logischen CRT-Geräts (Desktop Monitor) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-271">The [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-272">**CIM \_ deviceaccessedbyfile**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-272">**CIM\_DeviceAccessedByFile**</span></span>](cim-deviceaccessedbyfile.md)
</dt> <dd>

<span data-ttu-id="a2b9c-273">Die [**CIM \_ deviceaccessedbyfile**](cim-deviceaccessedbyfile.md) -Zuordnungs Klasse gibt das logische Gerät an, auf das über die [**CIM \_ Devicefile**](cim-devicefile.md) -Klasse zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-273">The [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-274">**CIM-Geräte \_ Steuerung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-274">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> <dd>

<span data-ttu-id="a2b9c-275">Die [**CIM- \_ deviceconnetction**](cim-deviceconnection.md) -Zuordnungs Klasse stellt zwei oder mehr verbundene Geräte dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-275">The [**CIM\_DeviceConnection**](cim-deviceconnection.md) association class represents two or more connected devices.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-276">**CIM \_ deviceerrorcounts**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-276">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> <dd>

<span data-ttu-id="a2b9c-277">Die [**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md) -Klasse ist eine statistische Klasse, die Fehler bezogene Leistungsindikatoren für ein logisches Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-277">The [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="a2b9c-278">Die Fehlertypen werden von CCITT (REC X. 733) und ISO (IEC 10164-4) definiert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-278">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-279">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-279">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> <dd>

<span data-ttu-id="a2b9c-280">Die [**CIM \_ Devicefile**](cim-devicefile.md) -Klasse stellt einen logischen Dateityp dar, der ein Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-280">The [**CIM\_DeviceFile**](cim-devicefile.md) class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="a2b9c-281">Diese Konvention eignet sich für Betriebssysteme, die Geräte mit einem Bytestream-e/a-Modell verwalten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-281">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="a2b9c-282">Das logische Gerät, das dieser Datei zugeordnet ist, wird mithilfe der [**CIM \_ deviceaccessedbyfile**](cim-deviceaccessedbyfile.md) -Beziehung angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-282">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-283">**CIM-Geräte \_ Implementierung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-283">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dd>

<span data-ttu-id="a2b9c-284">Die [**CIM-Klasse \_ devicesapimplementation**](cim-devicesapimplementation.md) stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und der Art der Implementierung dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-284">The [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="a2b9c-285">Wenn einem SAP Viele logische Geräte zugeordnet sind, werden die Elemente zusammen mit dem Zugriffspunkt bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-285">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="a2b9c-286">Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des SAP-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-286">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-287">**CIM-Geräte \_ Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-287">**CIM\_DeviceServiceImplementation**</span></span>](cim-deviceserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="a2b9c-288">Die [**CIM- \_ deviceserviceimplementation**](cim-deviceserviceimplementation.md) -Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-288">The [**CIM\_DeviceServiceImplementation**](cim-deviceserviceimplementation.md) class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="a2b9c-289">Wenn mehrere Geräte einem Dienst zugeordnet sind, werden die Elemente zusammen verwendet, um den Dienst bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-289">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="a2b9c-290">Wenn verschiedene Implementierungen eines Dienstanbieter vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des Dienst Objekts.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-290">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-291">**CIM-Geräte \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-291">**CIM\_DeviceSoftware**</span></span>](cim-devicesoftware.md)
</dt> <dd>

<span data-ttu-id="a2b9c-292">Die [**CIM- \_ devicesoftware**](cim-devicesoftware.md) -Beziehung identifiziert Software, die einem Gerät zugeordnet ist, z. b. Treiber, Konfigurations-oder Anwendungssoftware oder Firmware.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-292">The [**CIM\_DeviceSoftware**](cim-devicesoftware.md) relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-293">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-293">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dd>

<span data-ttu-id="a2b9c-294">Die [**CIM- \_ Verzeichnis**](cim-directory.md) Klasse stellt einen Dateityp dar, der die darin enthaltenen Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-294">The [**CIM\_Directory**](cim-directory.md) class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-295">**CIM \_ Director Action**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-296">Die [**abstrakte \_ directoryaction**](cim-directoryaction.md) -Klasse wird Verzeichnisse verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-296">The [**CIM\_DirectoryAction**](cim-directoryaction.md) abstract class manages directories.</span></span> <span data-ttu-id="a2b9c-297">Die Verzeichnis Erstellung wird von der CIM-Klasse " [**\_ kreatedirectoryaction**](cim-createdirectoryaction.md) " verarbeitet, und die Verzeichnis Entfernung erfolgt durch die [**CIM- \_ removedirectoryaction**](cim-removedirectoryaction.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-297">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-298">**CIM \_ directoriykontainsfile**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-298">**CIM\_DirectoryContainsFile**</span></span>](cim-directorycontainsfile.md)
</dt> <dd>

<span data-ttu-id="a2b9c-299">Die [**CIM \_ directorykontainsfile**](cim-directorycontainsfile.md) -Klasse stellt eine Zuordnung zwischen einem Verzeichnis und den Dateien dar, die in diesem Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-299">The [**CIM\_DirectoryContainsFile**](cim-directorycontainsfile.md) class represents an association between a directory and files contained within that directory.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-300">**CIM- \_ directspecification**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-300">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> <dd>

<span data-ttu-id="a2b9c-301">Die [**CIM- \_ directoryspecification**](cim-directoryspecification.md) -Klasse erfasst die Hauptverzeichnis Struktur eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-301">The [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class captures the major directory structure of a software element.</span></span> <span data-ttu-id="a2b9c-302">Diese Klasse wird verwendet, um die Dateien eines Software Elements in verwaltbaren Einheiten zu organisieren, die auf einem Computersystem verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-302">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-303">**CIM \_ directoriyspecificationfile**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-303">**CIM\_DirectorySpecificationFile**</span></span>](cim-directoryspecificationfile.md)
</dt> <dd>

<span data-ttu-id="a2b9c-304">Die [**CIM- \_ directoryspecificationfile-Zuordnung**](cim-directoryspecificationfile.md) stellt das Verzeichnis dar, das die Datei enthält, die durch Verweisen auf die CIM- [**\_ directoryspecification**](cim-directoryspecification.md) -Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-304">The [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-305">**CIM \_ diskretesensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-305">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-306">Die [**CIM \_ diskretesensor**](cim-discretesensor.md) -Klasse verfügt über einen Satz gültiger Zeichen folgen Werte, die Sie melden kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-306">The [**CIM\_DiscreteSensor**](cim-discretesensor.md) class has a set of legal string values that it can report.</span></span> <span data-ttu-id="a2b9c-307">Die Werte werden in der **PossibleValues** -Eigenschaft des Sensors aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-307">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="a2b9c-308">Ein diskreter Sensor verfügt immer über einen aktuellen Lesevorgang, der einem der-Enumerationswerte entspricht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-308">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-309">**CIM- \_ diskdrive**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-309">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dd>

<span data-ttu-id="a2b9c-310">Die [**CIM \_ diskdrive**](cim-diskdrive.md) -Klasse stellt ein physisches Laufwerk dar, das vom Betriebssystem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-310">The [**CIM\_DiskDrive**](cim-diskdrive.md) class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="a2b9c-311">Die Festplattenlaufwerke entsprechen den logischen und Verwaltungs Merkmalen des Laufwerks, und in manchen Fällen werden die physischen Merkmale des Geräts möglicherweise nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-311">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="a2b9c-312">Eine Schnittstelle zu einem physischen Laufwerk ist ein Member dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-312">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="a2b9c-313">Ein Objekt, das auf einem anderen logischen Gerät basiert, ist jedoch kein Member dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-313">However, an object based on another logical device is not a member of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-314">**CIM- \_ Diskettelaufwerk**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-314">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dd>

<span data-ttu-id="a2b9c-315">Die [**CIM \_ diskettedrive**](cim-diskettedrive.md) -Klasse stellt die Funktionen und die Verwaltung eines Disketten Laufwerks dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-315">The [**CIM\_DisketteDrive**](cim-diskettedrive.md) class represents the capabilities and management of a diskette drive.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-316">**CIM \_ Diskpartition**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-316">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dd>

<span data-ttu-id="a2b9c-317">Die [**CIM \_ Diskpartition**](cim-diskpartition.md) -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, der vom Betriebssystem mithilfe der Felder Typ und Untertyp der Partition identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-317">The [**CIM\_DiskPartition**](cim-diskpartition.md) class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="a2b9c-318">Datenträger Partitionen sollten direkt durch physische Medien (angegeben durch die [**CIM- \_**](cim-realizesdiskpartition.md) Neuzuordnung) oder auf Speichervolumes erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-318">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-319">**CIM \_ diskspacecheck**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-319">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> <dd>

<span data-ttu-id="a2b9c-320">Die [**CIM \_ diskspacecheck**](cim-diskspacecheck.md) -Klasse überprüft die Menge an verfügbarem Speicherplatz des Systems und gibt Sie in der **AvailableDiskSpace** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-320">The [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="a2b9c-321">Details werden mit dem Wert in der **AvailableSpace** -Eigenschaft des [**CIM- \_ Dateisystem**](cim-filesystem.md) Objekts verglichen, das dem [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt zugeordnet ist, in dem die Systemumgebung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-321">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="a2b9c-322">Wenn der Wert der **AvailableSpace** -Eigenschaft größer oder gleich dem Wert ist, der in der **AvailableDiskSpace** -Eigenschaft angegeben ist, wird die Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-322">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-323">**CIM- \_ Anzeige**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-323">**CIM\_Display**</span></span>](cim-display.md)
</dt> <dd>

<span data-ttu-id="a2b9c-324">Die [**CIM- \_ Anzeige**](cim-display.md) Klasse ist eine übergeordnete Klasse zum Gruppieren von verschiedenen Anzeigegeräten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-324">The [**CIM\_Display**](cim-display.md) class is a parent class for grouping miscellaneous display devices.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-325">**CIM \_ DMA**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-325">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dd>

<span data-ttu-id="a2b9c-326">Die [**CIM- \_ DMA**](cim-dma.md) -Klasse stellt die Computerarchitektur für den direkten Speicherzugriff (DMA) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-326">The [**CIM\_DMA**](cim-dma.md) class represents computer architecture direct memory access (DMA).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-327">**CIM \_ angedockt**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-327">**CIM\_Docked**</span></span>](cim-docked.md)
</dt> <dd>

<span data-ttu-id="a2b9c-328">Die in [**CIM \_ angedockte**](cim-docked.md) Zuordnung stellt die Beziehung zwischen zwei Chassis dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-328">The [**CIM\_Docked**](cim-docked.md) association represents the relationship between two chassis.</span></span> <span data-ttu-id="a2b9c-329">Beispielsweise kann ein Laptop (ein Typ von Chassis) an einer Docking Station (einem anderen Typ von Chassis) angedockt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-329">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="a2b9c-330">Diese typische Beziehung wird explizit beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-330">This typical relationship is explicitly described.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-331">**CIM- \_ Element Kapazität**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-331">**CIM\_ElementCapacity**</span></span>](cim-elementcapacity.md)
</dt> <dd>

<span data-ttu-id="a2b9c-332">Die [**CIM \_ elementcapacity**](cim-elementcapacity.md) -Klasse ordnet ein [**CIM \_ physicalcapacity**](cim-physicalcapacity.md) -Objekt einem oder mehreren physischen Elementen zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-332">The [**CIM\_ElementCapacity**](cim-elementcapacity.md) class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="a2b9c-333">Es ordnet eine Beschreibung der minimalen und maximalen Hardwareanforderungen (bzw.-Funktionen) den physischen Elementen zu, die beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-333">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-334">**CIM- \_ Element Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-334">**CIM\_ElementConfiguration**</span></span>](cim-elementconfiguration.md)
</dt> <dd>

<span data-ttu-id="a2b9c-335">Die [**CIM- \_ ElementConfiguration**](cim-elementconfiguration.md) -Zuordnung verknüpft ein [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt mit einem oder mehreren verwalteten Systemelementen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-335">The [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="a2b9c-336">Das **CIM- \_ Konfigurations** Objekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für das zugeordnete [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-336">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-337">**CIM- \_ Element Setting**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-337">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="a2b9c-338">Die [**CIM- \_ ElementSetting**](cim-elementsetting.md) -Klasse stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-338">The [**CIM\_ElementSetting**](cim-elementsetting.md) class represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-339">**CIM- \_ elementslinked**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-339">**CIM\_ElementsLinked**</span></span>](cim-elementslinked.md)
</dt> <dd>

<span data-ttu-id="a2b9c-340">Die [**CIM \_ elementslinked**](cim-elementslinked.md) Association stellt physische Elemente dar, die von einem physischen Link miteinander verkabelt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-340">The [**CIM\_ElementsLinked**](cim-elementslinked.md) association represents physical elements that are cabled together by a physical link.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-341">**CIM \_ errorcountersfordevice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-341">**CIM\_ErrorCountersForDevice**</span></span>](cim-errorcountersfordevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-342">Die [**CIM-Klasse \_ errorcountersfordevice**](cim-errorcountersfordevice.md) ordnet dem logischen Gerät, auf das Sie angewendet wird, die [**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md) -Klasse zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-342">The [**CIM\_ErrorCountersForDevice**](cim-errorcountersfordevice.md) class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-343">**CIM \_ executeprogram**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-343">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> <dd>

<span data-ttu-id="a2b9c-344">Die [**CIM \_ executeprogram**](cim-executeprogram.md) -Klasse stellt Dateien dar, die auf dem System ausgeführt werden können, auf dem das Softwareelement installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-344">The [**CIM\_ExecuteProgram**](cim-executeprogram.md) class represents files that can be executed on the system where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-345">**CIM- \_ Export**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-345">**CIM\_Export**</span></span>](cim-export.md)
</dt> <dd>

<span data-ttu-id="a2b9c-346">Die [**CIM- \_ Export**](cim-export.md) Klasse stellt eine Zuordnung zwischen einem lokalen Dateisystem und den zugehörigen Verzeichnissen dar, die angeben, dass die angegebenen Verzeichnisse zum Einbinden verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-346">The [**CIM\_Export**](cim-export.md) class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="a2b9c-347">Beim Exportieren eines vollständigen Dateisystems sollte das Verzeichnis auf das oberste Verzeichnis des Dateisystems verweisen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-347">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-348">**CIM \_ extracapacitygroup**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-348">**CIM\_ExtraCapacityGroup**</span></span>](cim-extracapacitygroup.md)
</dt> <dd>

<span data-ttu-id="a2b9c-349">Die [**CIM \_ extracapacitygroup**](cim-extracapacitygroup.md) -Klasse wird von einer Redundanz Gruppe abgeleitet, die angibt, dass die aggregierten Elemente mehr Kapazität oder mehr Kapazität aufweisen, als erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-349">The [**CIM\_ExtraCapacityGroup**](cim-extracapacitygroup.md) class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="a2b9c-350">Ein Beispiel für diese Art von Redundanz ist die Installation von N + 1 Stromversorgungen oder Lüfter in einem System.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-350">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-351">**CIM- \_ Lüfter**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-351">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dd>

<span data-ttu-id="a2b9c-352">Die [**CIM- \_ Lüfter**](cim-fan.md) -Klasse stellt die Funktionen und die Verwaltung eines Lüfter-kühl Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-352">The [**CIM\_Fan**](cim-fan.md) class represents the capabilities and management of a fan cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-353">**CIM- \_ fileaction**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-353">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-354">Mit der [**CIM \_ fileaction**](cim-fileaction.md) -Klasse kann der Autor Dateien suchen, die bereits auf dem Computer eines Benutzers vorhanden sind, und diese Dateien dann verschieben oder an einen neuen Speicherort kopieren.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-354">The [**CIM\_FileAction**](cim-fileaction.md) class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-355">**CIM- \_ Datei Spezifikation**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-355">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> <dd>

<span data-ttu-id="a2b9c-356">Die [**CIM- \_ filespecification**](cim-filespecification.md) -Klasse stellt eine Datei dar, die sich entweder in einem oder aus dem System befindet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-356">The [**CIM\_FileSpecification**](cim-filespecification.md) class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="a2b9c-357">Die Datei befindet sich in dem Verzeichnis, das durch die [**CIM \_ Director yspecificationfile-Zuordnung**](cim-directoryspecificationfile.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-357">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="a2b9c-358">Die [**Aufruf**](invoke-method-in-class-cim-filespecification.md) Methode verwendet die Informationen, um zu überprüfen, ob die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-358">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="a2b9c-359">Beachten Sie, dass Eigenschaften mit einem **null** -Wert nicht geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-359">Note that properties with a **Null** value are not checked.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-360">**CIM- \_ FileStorage**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-360">**CIM\_FileStorage**</span></span>](cim-filestorage.md)
</dt> <dd>

<span data-ttu-id="a2b9c-361">Die [**CIM- \_ FileStorage**](cim-filestorage.md) -Zuordnung verknüpft das Dateisystem und die logischen Dateien, die über das Dateisystem adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-361">The [**CIM\_FileStorage**](cim-filestorage.md) association links the file system and the logical files addressed through the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-362">**CIM- \_ Dateisystem**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-362">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-363">Die [**CIM- \_ Dateisystem**](cim-filesystem.md) Klasse stellt eine Datei oder ein DataSet dar, die sich lokal auf einem Computersystem befinden oder von einem Dateiserver Remote eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-363">The [**CIM\_FileSystem**](cim-filesystem.md) class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-364">**CIM- \_ Flatpanel**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-364">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> <dd>

<span data-ttu-id="a2b9c-365">Die [**CIM- \_ Flatpanel**](cim-flatpanel.md) -Klasse stellt die Funktionen und die Verwaltung des logischen Flatpanel-Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-365">The [**CIM\_FlatPanel**](cim-flatpanel.md) class represents the capabilities and management of the flat panel logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-366">**CIM \_ fromdirector Action**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-366">**CIM\_FromDirectoryAction**</span></span>](cim-fromdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-367">Die [**CIM \_ fromdirector Action**](cim-fromdirectoryaction.md) -Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-367">The [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="a2b9c-368">Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis durch eine vorherige Aktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-368">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="a2b9c-369">Diese Zuordnung darf nicht mit einer [**CIM \_ fromdirector yspecification**](cim-fromdirectoryspecification.md) -Zuordnung vorhanden sein. eine Datei Aktion kann nur ein einzelnes Quellverzeichnis umfassen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-369">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-370">**CIM \_ fromdirectoriyspecification**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-370">**CIM\_FromDirectorySpecification**</span></span>](cim-fromdirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="a2b9c-371">Die [**CIM \_ fromdirector yspecification**](cim-fromdirectoryspecification.md) -Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-371">The [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="a2b9c-372">Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-372">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="a2b9c-373">Diese Zuordnung darf nicht mit einer [**CIM \_ fromdirector yaction**](cim-fromdirectoryaction.md) -Zuordnung vorhanden sein. eine Datei Aktion kann nur ein einzelnes Quellverzeichnis umfassen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-373">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-374">**CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-374">**CIM\_FRU**</span></span>](cim-fru.md)
</dt> <dd>

<span data-ttu-id="a2b9c-375">Die [**CIM \_ FRU**](cim-fru.md) -Klasse stellt eine Hersteller definierte Auflistung von Produkten und physischen Elementen dar, die einer von einem Feld ersetzbaren Einheit (FRU) zugeordnet sind, um ein Produkt am Standort des Kunden zu unterstützen, zu warten oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-375">The [**CIM\_FRU**](cim-fru.md) class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-376">**CIM- \_ fruincluentsproduct**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-376">**CIM\_FRUIncludesProduct**</span></span>](cim-fruincludesproduct.md)
</dt> <dd>

<span data-ttu-id="a2b9c-377">Die CIM-Klasse " [**\_ fruincludesproduct**](cim-fruincludesproduct.md) " zeigt an, dass eine ersetzbare Feld Einheit (FRU) aus anderen Produkten bestehen kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-377">The [**CIM\_FRUIncludesProduct**](cim-fruincludesproduct.md) class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-378">**CIM \_ fruphysicalelements**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-378">**CIM\_FRUPhysicalElements**</span></span>](cim-fruphysicalelements.md)
</dt> <dd>

<span data-ttu-id="a2b9c-379">Die CIM-Klasse " [**\_ fruphysicalelements**](cim-fruphysicalelements.md) " stellt die physischen Elemente dar, die eine ersetzbare (Feld) Einheit (FRU) bilden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-379">The [**CIM\_FRUPhysicalElements**](cim-fruphysicalelements.md) class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-380">**CIM- \_ Heatpipe**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-380">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dd>

<span data-ttu-id="a2b9c-381">Die [**CIM- \_ Heatpipe**](cim-heatpipe.md) -Klasse stellt die Funktionen und die Verwaltung eines wärmepipe-kühl Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-381">The [**CIM\_HeatPipe**](cim-heatpipe.md) class represents the capabilities and management of a heat pipe cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-382">**CIM- \_ hubspoint**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-382">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> <dd>

<span data-ttu-id="a2b9c-383">Die CIM-Klasse " [**\_ stestedaccesspoint**](cim-hostedaccesspoint.md) " stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, auf dem es bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-383">The [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md) class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="a2b9c-384">Jedes System hostet möglicherweise viele SAPS.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-384">Each system may host many SAPs.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-385">**CIM- \_ boostedbootsap**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-385">**CIM\_HostedBootSAP**</span></span>](cim-hostedbootsap.md)
</dt> <dd>

<span data-ttu-id="a2b9c-386">Die CIM-Klasse " [**\_ shostedbootsap**](cim-hostedbootsap.md) " definiert das Hosting-einheitliche Computersystem für eine [**CIM- \_ bootsap**](cim-bootsap.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-386">The [**CIM\_HostedBootSAP**](cim-hostedbootsap.md) class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="a2b9c-387">Da diese Beziehung von [**CIM \_ hostspoint**](cim-hostedaccesspoint.md)untergeordnet ist, erbt Sie das für [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)definierte Bereichs Schema/Benennungs Schema, bei dem ein Zugriffspunkt dem Hostingsystem entspricht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-387">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="a2b9c-388">In diesem Fall muss **CIM \_ bootsap** auf seine hostende [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md) -Klasse zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-388">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-389">**CIM- \_ Boots Dienst**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-389">**CIM\_HostedBootService**</span></span>](cim-hostedbootservice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-390">Die CIM-Klasse " [**\_ hostbootservice**](cim-hostedbootservice.md) " ordnet ein Hostingsystem und einen Start Dienst zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-390">The [**CIM\_HostedBootService**](cim-hostedbootservice.md) class associates a hosting system and a boot service.</span></span> <span data-ttu-id="a2b9c-391">Da diese Beziehung vom [**CIM- \_ Hostingdienst**](cim-hostedservice.md)untergeordnet ist, erbt Sie das für den Dienst definierte Bereichs Schema/Benennungs Schema, bei dem ein Dienst auf das Hostingsystem beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-391">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-392">**CIM- \_ Dateisystem**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-392">**CIM\_HostedFileSystem**</span></span>](cim-hostedfilesystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-393">Die [**CIM \_ hostedfile**](cim-hostedfilesystem.md) System-Zuordnung stellt eine Verknüpfung zwischen dem Computersystem und dem Dateisystem dar, das auf dem Computersystem gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-393">The [**CIM\_HostedFileSystem**](cim-hostedfilesystem.md) association represents a link between the computer system and the file system hosted on the computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-394">**CIM-Host- \_ jobdestination**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-394">**CIM\_HostedJobDestination**</span></span>](cim-hostedjobdestination.md)
</dt> <dd>

<span data-ttu-id="a2b9c-395">Die CIM-Klasse " [**\_ hostjobdestination**](cim-hostedjobdestination.md) " stellt eine Zuordnung zwischen einem Auftrags Ziel und dem System dar, auf dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-395">The [**CIM\_HostedJobDestination**](cim-hostedjobdestination.md) class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="a2b9c-396">Ein System kann viele Auftrags Warteschlangen hosten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-396">A system may host many job queues.</span></span> <span data-ttu-id="a2b9c-397">Auftrags Ziele werden an das Hostingsystem zurück verschoben.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-397">Job destinations defer to the hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-398">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-398">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-399">Die CIM-Klasse " [**\_ Hostdienst**](cim-hostedservice.md) " stellt eine Zuordnung zwischen einem Dienst und dem System dar, auf dem sich die Funktionalität befindet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-399">The [**CIM\_HostedService**](cim-hostedservice.md) class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="a2b9c-400">Ein System kann viele Dienste hosten, die auf das Hostingsystem zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-400">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="a2b9c-401">Das Modell stellt keine Dienste dar, die auf mehreren Systemen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-401">The model does not represent services hosted across multiple systems.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-402">**CIM- \_ infraredcontroller**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-402">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-403">Die CIM-Klasse " [**\_ infraredcontroller**](cim-infraredcontroller.md) " stellt die Funktionen und die Verwaltung eines Infrarot Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-403">The [**CIM\_InfraredController**](cim-infraredcontroller.md) class represents the capabilities and management of an infrared controller.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-404">**CIM- \_ instanalledos**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-404">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dd>

<span data-ttu-id="a2b9c-405">Die [**CIM \_ installedos**](cim-installedos.md) Association-Klasse stellt eine Verknüpfung zwischen dem Computersystem und dem installierten Betriebssystem dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-405">The [**CIM\_InstalledOS**](cim-installedos.md) association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="a2b9c-406">Ein Betriebssystem wird installiert, wenn es sich im Speicherbereich eines Computer Systems befindet (z. b. auf ein Laufwerk kopiert oder in den Arbeitsspeicher heruntergeladen wird).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-406">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-407">**CIM \_ InstalledSoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-407">**CIM\_InstalledSoftwareElement**</span></span>](cim-installedsoftwareelement.md)
</dt> <dd>

<span data-ttu-id="a2b9c-408">Die [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) -Klasse ordnet ein Computersystem einem installierten Softwareelement zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-408">The [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) class associates a computer system with an installed software element.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-409">**CIM \_ -Antwort**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-409">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dd>

<span data-ttu-id="a2b9c-410">Die CIM-Klasse " [**\_ iriq**](cim-irq.md) " stellt eine Intel Architecture Interrupt Request Line (UNQ) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-410">The [**CIM\_IRQ**](cim-irq.md) class represents an Intel architecture interrupt request line (IRQ).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-411">**CIM- \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-411">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dd>

<span data-ttu-id="a2b9c-412">Die [**CIM- \_ Auftrags**](cim-job.md) Klasse stellt eine Arbeitseinheit für ein System dar, z. b. einen Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-412">The [**CIM\_Job**](cim-job.md) class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="a2b9c-413">Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-413">A job is distinct from a process because a job can be scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-414">**CIM \_ jobdestination**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-414">**CIM\_JobDestination**</span></span>](cim-jobdestination.md)
</dt> <dd>

<span data-ttu-id="a2b9c-415">Die [**CIM \_ jobdestination**](cim-jobdestination.md) -Klasse stellt dar, wo ein Auftrag zur Verarbeitung übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-415">The [**CIM\_JobDestination**](cim-jobdestination.md) class represents where a job is submitted for processing.</span></span> <span data-ttu-id="a2b9c-416">Sie kann auf eine Warteschlange verweisen, die NULL oder mehr Aufträge enthält, z. b. eine Druck Warteschlange, die Druckaufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-416">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="a2b9c-417">Auftrags Ziele werden auf Systemen gehostet, ähnlich der Art, in der Dienste auf Systemen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-417">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-418">**CIM \_ jobdestinationjobs**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-418">**CIM\_JobDestinationJobs**</span></span>](cim-jobdestinationjobs.md)
</dt> <dd>

<span data-ttu-id="a2b9c-419">Die [**CIM \_ jobdestinationjobs-Zuordnung**](cim-jobdestinationjobs.md) beschreibt, wo ein Auftrag zur Verarbeitung übermittelt wird (d. h. an welches Auftrags Ziel).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-419">The [**CIM\_JobDestinationJobs**](cim-jobdestinationjobs.md) association describes where a job is submitted for processing (that is, to which job destination).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-420">**CIM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-420">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dd>

<span data-ttu-id="a2b9c-421">Die [**CIM- \_ Tastatur**](cim-keyboard.md) Klasse stellt die Funktionen und die Verwaltung des logischen Tastatur Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-421">The [**CIM\_Keyboard**](cim-keyboard.md) class represents the capabilities and management of the keyboard logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-422">**CIM \_ linkhasconnector**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-422">**CIM\_LinkHasConnector**</span></span>](cim-linkhasconnector.md)
</dt> <dd>

<span data-ttu-id="a2b9c-423">Die [**CIM \_ linkhasconnector**](cim-linkhasconnector.md) -Klasse ordnet Kabel und Verknüpfungen zu, die als physische Connectors verwendet werden, die die physischen Elemente verbinden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-423">The [**CIM\_LinkHasConnector**](cim-linkhasconnector.md) class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="a2b9c-424">Diese Zuordnung definiert explizit die Beziehung von Connectors für [**CIM \_ physicallink**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-424">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-425">**CIM \_ LocalFile System**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-425">**CIM\_LocalFileSystem**</span></span>](cim-localfilesystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-426">Die [**CIM \_ LocalFile**](cim-localfilesystem.md) System-Klasse stellt den Dateispeicher dar, der von einem Computersystem über lokale Mittel (z. b. direkten Zugriff auf Gerätetreiber) gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-426">The [**CIM\_LocalFileSystem**](cim-localfilesystem.md) class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="a2b9c-427">Der Dateispeicher kann direkt vom Computersystem verwaltet werden, ohne dass ein anderer Computer als Dateiserver fungieren muss.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-427">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="a2b9c-428">Bei einem Cluster Dateisystem ist das Dateisystem jedoch lokal und wird daher auf den Cluster abgehandelt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-428">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-429">**CIM- \_ Speicherort**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-429">**CIM\_Location**</span></span>](cim-location.md)
</dt> <dd>

<span data-ttu-id="a2b9c-430">Die [**CIM- \_ Location**](cim-location.md) -Klasse stellt die Position und die Adresse eines physischen Elements dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-430">The [**CIM\_Location**](cim-location.md) class represents the position and address of a physical element.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-431">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-431">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-432">Die [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse stellt eine Hardware Entität dar, die in physischer Hardware erkannt werden kann oder nicht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-432">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-433">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-433">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dd>

<span data-ttu-id="a2b9c-434">Die [**CIM \_ LogicalDisk**](cim-logicaldisk.md) -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das **DeviceID** (Key)-Feld des Datenträgers identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-434">The [**CIM\_LogicalDisk**](cim-logicaldisk.md) class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="a2b9c-435">Beispielsweise enthält das Feld " **DeviceID** " in einer Windows-Umgebung einen Laufwerk Buchstaben. in einer UNIX-Umgebung enthält Sie den Zugriffs Pfad. und in einer NetWare-Umgebung enthält Sie den Volumenamen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-435">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-436">**CIM \_ LogicalDiskBasedOnPartition**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-436">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

<span data-ttu-id="a2b9c-437">Die [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) -Klasse ordnet der Festplatten Partition, auf der Sie sich befindet, einen logischen Datenträger zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-437">The [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) class associates a logical disk with the disk partition on which it resides.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-438">**CIM \_ logicaldiskbasedonvolumeset**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-438">**CIM\_LogicalDiskBasedOnVolumeSet**</span></span>](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

<span data-ttu-id="a2b9c-439">Die [**CIM \_ logicaldiskbasedonvolumeset**](cim-logicaldiskbasedonvolumeset.md) -Zuordnung bezieht logische Datenträger mit dem Volume, auf dem Sie gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-439">The [**CIM\_LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="a2b9c-440">Logische Datenträger können auf einem einzelnen Volume (z. b. von einem Software Volume-Manager verfügbar gemacht) oder auf einer Datenträger Partition basieren.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-440">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-441">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-441">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="a2b9c-442">Die [**CIM \_ LogicalElement**](cim-logicalelement.md) -Klasse ist die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten, z. b. profile, Prozesse oder Systemfunktionen, in Form logischer Geräte darstellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-442">The [**CIM\_LogicalElement**](cim-logicalelement.md) class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-443">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-443">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dd>

<span data-ttu-id="a2b9c-444">Die [**CIM \_ LogicalFile**](cim-logicalfile.md) -Klasse stellt eine benannte Auflistung von Daten dar, bei der es sich um ausführbaren Code handeln kann, der sich in einem Dateisystem in einem Speicherblock befindet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-444">The [**CIM\_LogicalFile**](cim-logicalfile.md) class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-445">**CIM- \_ logikalidentität**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-445">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dd>

<span data-ttu-id="a2b9c-446">Die [**CIM \_ logicalidentity**](cim-logicalidentity.md) -Klasse ist eine abstrakte und generische Zuordnung, die angibt, dass zwei logische Elemente verschiedene Aspekte der gleichen zugrunde liegenden Entität darstellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-446">The [**CIM\_LogicalIdentity**](cim-logicalidentity.md) class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-447">**CIM- \_ Magnet Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-447">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> <dd>

<span data-ttu-id="a2b9c-448">Die CIM-Klasse " [**\_ magnetyopticaldrive**](cim-magnetoopticaldrive.md) " stellt die Funktionen und die Verwaltung eines "Magneto-Optical"-Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-448">The [**CIM\_MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-449">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-449">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="a2b9c-450">Die [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse ist die Basisklasse für die System Element Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-450">The [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="a2b9c-451">Jede unterscheidbare Systemkomponente ist ein Kandidat für die Einbindung in diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-451">Any distinguishable system component is a candidate for inclusion in this class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-452">**CIM- \_ Managementcontroller**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-452">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-453">Die [**CIM \_ Managementcontroller**](cim-managementcontroller.md) -Klasse bezieht sich auf die Funktionen und die Verwaltung eines Verwaltungs Controllers.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-453">The [**CIM\_ManagementController**](cim-managementcontroller.md) class relates to the capabilities and management of a management controller.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-454">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-454">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-455">Die [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md) -Klasse stellt die Möglichkeit dar, auf ein oder mehrere Medien zuzugreifen und dann die Medien zum Speichern und Abrufen von Daten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-455">The [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-456">**CIM- \_ mediapresent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-456">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-457">Die [**CIM \_ mediapresent**](cim-mediapresent.md) -Zuordnung beschreibt eine Beziehung, bei der über ein Medien Zugriffsgerät auf einen Speicherblock zugegriffen werden muss.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-457">The [**CIM\_MediaPresent**](cim-mediapresent.md) association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-458">**CIM- \_ Speicher**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-458">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dd>

<span data-ttu-id="a2b9c-459">Die [**CIM- \_ Speicher**](cim-memory.md) Klasse stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-459">The [**CIM\_Memory**](cim-memory.md) class represents the capabilities and management of memory-related logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-460">**CIM- \_ memorycapacity**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-460">**CIM\_MemoryCapacity**</span></span>](cim-memorycapacity.md)
</dt> <dd>

<span data-ttu-id="a2b9c-461">Die [**CIM \_ memorycapacity**](cim-memorycapacity.md) -Klasse stellt den Arbeitsspeicher dar, der auf einem physischen Element und dessen minimalen und maximalen Konfigurationen installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-461">The [**CIM\_MemoryCapacity**](cim-memorycapacity.md) class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="a2b9c-462">Informationen zu derzeit installiertem Arbeitsspeicher und den minimalen und maximalen Anforderungen eines Elements befinden sich in Instanzen der [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-462">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-463">**CIM- \_ memorycheck**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-463">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> <dd>

<span data-ttu-id="a2b9c-464">Die [**CIM \_ memorycheck**](cim-memorycheck.md) -Klasse gibt eine Bedingung für die minimale Arbeitsspeicher Menge an, die auf einem System verfügbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-464">The [**CIM\_MemoryCheck**](cim-memorycheck.md) class specifies a condition for the minimum amount of memory that must be available on a system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-465">**CIM \_ memorymappedio**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-465">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dd>

<span data-ttu-id="a2b9c-466">Die [**CIM \_ memorymappedio**](cim-memorymappedio.md) -Klasse stellt die Computerarchitektur-e/a mit Speicher Abbild dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-466">The [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="a2b9c-467">Diese Klasse adressiert Arbeitsspeicher-und Port-e/a-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-467">This class addresses memory and port I/O resources.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-468">**CIM \_ memoryoncard**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-468">**CIM\_MemoryOnCard**</span></span>](cim-memoryoncard.md)
</dt> <dd>

<span data-ttu-id="a2b9c-469">Die [**CIM \_ memoryoncard**](cim-memoryoncard.md) -Klasse ordnet physischen Speicher zu, der sich auf hostingboards, Adapterkarten usw. befindet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-469">The [**CIM\_MemoryOnCard**](cim-memoryoncard.md) class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="a2b9c-470">Diese Zuordnung definiert explizit die Beziehung Zwischenspeicher und Karten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-470">This association explicitly defines the relationship of memory to cards.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-471">**CIM- \_ memorywithmedia**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-471">**CIM\_MemoryWithMedia**</span></span>](cim-memorywithmedia.md)
</dt> <dd>

<span data-ttu-id="a2b9c-472">Die [**CIM- \_ memorywithmedia**](cim-memorywithmedia.md) -Klasse ordnet physischen Speicher einem physischen Medium und der zugehörigen Cartridge zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-472">The [**CIM\_MemoryWithMedia**](cim-memorywithmedia.md) class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="a2b9c-473">Der Arbeitsspeicher bietet Medien Identifikation und speichert benutzerspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-473">The memory provides media identification and stores user-specific data.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-474">**CIM \_ modifysettingaction**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-474">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-475">Die [**CIM \_ modifysettingaction**](cim-modifysettingaction.md) -Klasse stellt die Informationen zum Ändern einer bestimmten Einstellungsdatei für einen bestimmten Eintrag mit einem bestimmten Wert dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-475">The [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-476">**CIM- \_ Monitorauflösung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-476">**CIM\_MonitorResolution**</span></span>](cim-monitorresolution.md)
</dt> <dd>

<span data-ttu-id="a2b9c-477">Die [**CIM- \_ monitorresolution**](cim-monitorresolution.md) -Klasse stellt die Beziehung zwischen horizontaler und vertikaler Auflösung und der Aktualisierungsrate und dem Überprüfungs Modus für einen Desktop Monitor dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-477">The [**CIM\_MonitorResolution**](cim-monitorresolution.md) class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="a2b9c-478">Werte werden im Videocontroller Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-478">Values are specified in the video controller object.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-479">**CIM- \_ monitorsetting**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-479">**CIM\_MonitorSetting**</span></span>](cim-monitorsetting.md)
</dt> <dd>

<span data-ttu-id="a2b9c-480">Die [**CIM- \_ monitorsetting**](cim-monitorsetting.md) -Klasse ordnet die Monitor Auflösung dem Desktop Monitor zu, auf den Sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-480">The [**CIM\_MonitorSetting**](cim-monitorsetting.md) class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-481">**CIM- \_ einbinden**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-481">**CIM\_Mount**</span></span>](cim-mount.md)
</dt> <dd>

<span data-ttu-id="a2b9c-482">Die [**CIM \_**](cim-mount.md) -Bereitstellungs Klasse stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-482">The [**CIM\_Mount**](cim-mount.md) class represents an association between a file system and a directory to which it is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-483">**CIM- \_ multistaatensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-483">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-484">Die [**CIM \_ multistaatensor**](cim-multistatesensor.md) -Klasse stellt eine multimember-Gruppe von binären Sensoren dar, in der jeder binäre Sensor ein boolesches Ergebnis meldet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-484">The [**CIM\_MultiStateSensor**](cim-multistatesensor.md) class represents a multi-member set of binary sensors where each binary sensor reports a Boolean result.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-485">**CIM- \_ Netzwerkadapter**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-485">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dd>

<span data-ttu-id="a2b9c-486">Die [**CIM- \_ netzwerkadapterklasse**](cim-networkadapter.md) ist eine abstrakte Klasse, die allgemeine Konzepte der Netzwerkhardware definiert (z. b. permanente Adresse oder Geschwindigkeit der Operation).</span><span class="sxs-lookup"><span data-stu-id="a2b9c-486">The [**CIM\_NetworkAdapter**](cim-networkadapter.md) class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="a2b9c-487">Die Informationen werden mithilfe der CIM-Zuordnung " [**\_ devicesapimplementation**](cim-devicesapimplementation.md) " übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-487">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-488">**CIM- \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-488">**CIM\_NFS**</span></span>](cim-nfs.md)
</dt> <dd>

<span data-ttu-id="a2b9c-489">Die [**CIM- \_ NFS**](cim-nfs.md) -Klasse stellt ein Remote Dateisystem dar, das mit dem NFS-Protokoll (Network File System) von einem Computersystem bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-489">The [**CIM\_NFS**](cim-nfs.md) class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-490">**CIM- \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-490">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> <dd>

<span data-ttu-id="a2b9c-491">Die [**CIM-Klasse \_ NonVolatileStorage**](cim-nonvolatilestorage.md) stellt die Funktionen und die Verwaltung von nichtflüchtigem Speicher dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-491">The [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="a2b9c-492">Nicht flüchtiger Speicher umfasst nativ Flash-und ROM-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-492">Nonvolatile memory natively includes flash and ROM storage.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-493">**CIM- \_ numericsensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-493">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-494">Die [**CIM- \_ numericsensor**](cim-numericsensor.md) -Klasse stellt einen numerischen Sensor dar, der numerische Messwerte zurückgibt und optional Schwellenwert Einstellungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-494">The [**CIM\_NumericSensor**](cim-numericsensor.md) class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-495">**CIM- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-495">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-496">Die [**CIM \_ OperatingSystem**](cim-operatingsystem.md) -Klasse stellt ein Computerbetriebssystem dar, das aus Software und Firmware besteht, mit denen die Hardware eines Computer Systems verwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-496">The [**CIM\_OperatingSystem**](cim-operatingsystem.md) class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-497">**CIM- \_ operatingsystemsoftwarefeature**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-497">**CIM\_OperatingSystemSoftwareFeature**</span></span>](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="a2b9c-498">Die [**CIM \_ operatingsystemsoftwarefeature**](cim-operatingsystemsoftwarefeature.md) -Klasse stellt die Softwarefunktionen dar, aus denen das Betriebssystem besteht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-498">The [**CIM\_OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) class represents the software features that make up the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-499">**CIM- \_ osprocess**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-499">**CIM\_OSProcess**</span></span>](cim-osprocess.md)
</dt> <dd>

<span data-ttu-id="a2b9c-500">Die [**CIM \_ osprocess**](cim-osprocess.md) -Klasse ordnet das Betriebssystem und einen oder mehrere Prozesse zu, die im Kontext des Betriebssystems ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-500">The [**CIM\_OSProcess**](cim-osprocess.md) class associates the operating system and one or more processes running in the context of the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-501">**CIM- \_ osversioncheck**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-501">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> <dd>

<span data-ttu-id="a2b9c-502">Die [**CIM \_ osversioncheck**](cim-osversioncheck.md) -Klasse gibt die Versionen des Betriebssystems an, die ein Softwareelement unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-502">The [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class specifies the versions of the operating system that can support a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-503">**CIM- \_ packagealarm**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-503">**CIM\_PackageAlarm**</span></span>](cim-packagealarm.md)
</dt> <dd>

<span data-ttu-id="a2b9c-504">Die [**CIM \_ packagealarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) -Zuordnung stellt die Beziehung dar, in der ein Alarmgerät als Teil eines Pakets installiert wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-504">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="a2b9c-505">Die Installation zeigt Probleme mit der Umgebung des Pakets an – den Sicherheitsstatus oder den Gesamtzustand.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-505">The installation indicates issues with the package's environment—its security state or its overall health.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-506">**CIM- \_ packagecooling**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-506">**CIM\_PackageCooling**</span></span>](cim-packagecooling.md)
</dt> <dd>

<span data-ttu-id="a2b9c-507">Die [**CIM \_ packagecooling**](cim-packagecooling.md) -Zuordnung stellt die Beziehung dar, in der ein Kühlgerät in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Kühlung des Pakets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-507">The [**CIM\_PackageCooling**](cim-packagecooling.md) association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-508">**CIM \_ packagedcomponent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-508">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-509">Die [**CIM \_ packagedcomponent**](cim-packagedcomponent.md) -Zuordnung stellt eine explizite Beziehung dar, in der eine Komponente in der Regel in einem physischen Paket (z. b. einem Chassis oder einer Karte) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-509">The [**CIM\_PackagedComponent**](cim-packagedcomponent.md) association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-510">**CIM \_ packageingechassis**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-510">**CIM\_PackageInChassis**</span></span>](cim-packageinchassis.md)
</dt> <dd>

<span data-ttu-id="a2b9c-511">Die [**CIM \_ packageinchassis**](cim-packageinchassis.md) -Zuordnung stellt die Beziehung dar, in der ein Chassis Andere Pakete enthalten kann, z. b. anderes Chassis und Karten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-511">The [**CIM\_PackageInChassis**](cim-packageinchassis.md) association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-512">**CIM- \_ packageinslot**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-512">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> <dd>

<span data-ttu-id="a2b9c-513">Die [**CIM \_ packageinslot**](cim-packageinslot.md) -Zuordnung stellt die Beziehung zwischen den Geräte Karten und dem Gehäuse dar, in dem Sie eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-513">The [**CIM\_PackageInSlot**](cim-packageinslot.md) association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-514">**CIM \_ packagetempsensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-514">**CIM\_PackageTempSensor**</span></span>](cim-packagetempsensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-515">Die [**CIM \_ packagetempsensor**](cim-packagetempsensor.md) -Zuordnung stellt die Beziehung dar, in der ein Temperatursensor häufig in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Umgebung des Pakets zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-515">The [**CIM\_PackageTempSensor**](cim-packagetempsensor.md) association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-516">**CIM- \_ parallelcontroller**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-516">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-517">Die [**CIM \_ parallelcontroller**](cim-parallelcontroller.md) -Zuordnung bezieht sich auf die Funktionen und die Verwaltung des logischen Parallel Port-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-517">The [**CIM\_ParallelController**](cim-parallelcontroller.md) association relates to the capabilities and management of the parallel port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-518">**CIM- \_ participatesinset**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-518">**CIM\_ParticipatesInSet**</span></span>](cim-participatesinset.md)
</dt> <dd>

<span data-ttu-id="a2b9c-519">Die [**CIM \_ participatesinset**](cim-participatesinset.md) -Klasse identifiziert physische Elemente, die zusammen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-519">The [**CIM\_ParticipatesInSet**](cim-participatesinset.md) class identifies physical elements that should be replaced together.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-520">**CIM- \_ PCIController**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-520">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-521">Die [**CIM \_ PCIController**](cim-pcicontroller.md) -Klasse stellt die Eigenschaften und die Verwaltung eines PCI-Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-521">The [**CIM\_PCIController**](cim-pcicontroller.md) class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="a2b9c-522">Die Eigenschaften in dieser Klasse und deren Unterklassen werden in den verschiedenen PCI-Spezifikationen definiert, die von PCI SIG veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-522">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-523">**CIM \_ PCMCIAController**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-523">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-524">Die [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) -Klasse stellt die Funktionen und die Verwaltung eines PCMCIA-Controllers (private Computer Memory Card International Association) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-524">The [**CIM\_PCMCIAController**](cim-pcmciacontroller.md) class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-525">**CIM \_ pcvideocontroller**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-525">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-526">Der [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md) stellt die Funktionen und die Verwaltung eines Video Controllers für persönliche Computer dar, einen Untertyp eines Video Controllers.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-526">The [**CIM\_PCVideoController**](cim-pcvideocontroller.md) represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-527">**CIM \_ pextentredundancycomponent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-527">**CIM\_PExtentRedundancyComponent**</span></span>](cim-pextentredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-528">Die [**CIM \_ pextentredundancycomponent**](cim-pextentredundancycomponent.md) -Klasse stellt die physischen Blöcke dar, die Teil einer Speicher Redundanz Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-528">The [**CIM\_PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) class represents the physical extents that participate in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-529">**CIM- \_ physicalcapacity**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-529">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> <dd>

<span data-ttu-id="a2b9c-530">Die [**CIM \_ physicalcapacity**](cim-physicalcapacity.md) -Klasse ist eine abstrakte Klasse, die die minimalen und maximalen Anforderungen eines physischen Elements und die Fähigkeit zur Unterstützung verschiedener Hardwaretypen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-530">The [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="a2b9c-531">So können z. b. die minimalen und maximalen Arbeitsspeicher Anforderungen als eine Unterklasse von **CIM \_ physicalcapacity** modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-531">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-532">**CIM- \_ physicalcomponent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-532">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-533">Die [**CIM \_ physicalcomponent**](cim-physicalcomponent.md) -Klasse stellt eine Komponente auf niedriger Ebene oder eine grundlegende Komponente innerhalb eines Pakets dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-533">The [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="a2b9c-534">Ein physisches Element, bei dem es sich nicht um einen Link, einen Connector oder ein Paket handelt, ist ein Nachfolger (oder Member) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-534">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-535">**CIM \_ physicalconnector**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-535">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dd>

<span data-ttu-id="a2b9c-536">Die [**CIM \_ physicalconnector**](cim-physicalconnector.md) -Klasse stellt ein beliebiges physisches Element dar, das verwendet wird, um eine Verbindung mit anderen Elementen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-536">The [**CIM\_PhysicalConnector**](cim-physicalconnector.md) class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="a2b9c-537">Jedes Objekt, das eine Verbindung herstellen und Signale oder eine Stromversorgung zwischen mindestens zwei physischen Elementen übertragen kann, ist ein Nachfolger (oder Member) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-537">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-538">**CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-538">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> <dd>

<span data-ttu-id="a2b9c-539">Die [**CIM \_ PhysicalElement**](cim-physicalelement.md) -Unterklassen definieren jede Komponente eines Systems, das über eine eindeutige physische Identität verfügt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-539">The [**CIM\_PhysicalElement**](cim-physicalelement.md) subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="a2b9c-540">Instanzen dieser Klasse können in Bezug auf Bezeichnungen definiert werden, die physisch an das Objekt angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-540">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-541">**CIM \_ physicalelementlocation**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-541">**CIM\_PhysicalElementLocation**</span></span>](cim-physicalelementlocation.md)
</dt> <dd>

<span data-ttu-id="a2b9c-542">Die [**CIM \_ physicalelementlocation**](cim-physicalelementlocation.md) -Klasse ordnet ein physisches Element einem [**CIM- \_ Speicherort**](cim-location.md) Objekt zu Inventur-oder Ersetzungs Zwecken zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-542">The [**CIM\_PhysicalElementLocation**](cim-physicalelementlocation.md) class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-543">**CIM- \_ physicalblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-543">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-544">Die [**CIM- \_ physicalblock**](cim-physicalextent.md) -Klasse stellt eine SCC RAID-Implementierung dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-544">The [**CIM\_PhysicalExtent**](cim-physicalextent.md) class represents an SCC RAID implementation.</span></span> <span data-ttu-id="a2b9c-545">Sie definiert die aufeinander folgenden adressierbaren Block Adressen auf einem einzelnen Speichergerät, die als einzelner Speicherblock in derselben [**CIM \_ storageredundancygroup**](cim-storageredundancygroup.md) -Klasse behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-545">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="a2b9c-546">Eine Alternative, wenn die automatische Konfiguration verwendet wird, besteht darin, die [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) -Klasse zu instanziieren oder zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-546">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-547">**CIM- \_ physicalframe**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-547">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> <dd>

<span data-ttu-id="a2b9c-548">Die [**CIM \_ physicalframe**](cim-physicalframe.md) -Klasse ist eine übergeordnete Klasse von Rack, Chassis und anderen Frame Gehäusen, die in Erweiterungs Klassen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-548">The [**CIM\_PhysicalFrame**](cim-physicalframe.md) class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="a2b9c-549">In dieser übergeordneten Klasse sind Eigenschaften wie **visiblewecker** und **audiblealarm** sowie Daten, die sich auf Sicherheitsverletzungen beziehen, enthalten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-549">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-550">**CIM \_ physicallink**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-550">**CIM\_PhysicalLink**</span></span>](cim-physicallink.md)
</dt> <dd>

<span data-ttu-id="a2b9c-551">Die [**CIM \_ physicallink**](cim-physicallink.md) -Klasse stellt die Verkabelung physischer Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-551">The [**CIM\_PhysicalLink**](cim-physicallink.md) class represents the cabling of physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-552">**CIM- \_ physicalmedia**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-552">**CIM\_PhysicalMedia**</span></span>](cim-physicalmedia.md)
</dt> <dd>

<span data-ttu-id="a2b9c-553">Die [**CIM \_ physicalmedia**](cim-physicalmedia.md) -Klasse stellt Typen von Dokumentation und Speichermedium (z. b. Bänder, CD-ROMs usw.) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-553">The [**CIM\_PhysicalMedia**](cim-physicalmedia.md) class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-554">**CIM- \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-554">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dd>

<span data-ttu-id="a2b9c-555">Die [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) -Klasse stellt Speichergeräte auf niedriger Ebene dar, wie z. b. Simms, DIMMs, Rohdaten Speicher-Chips usw.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-555">The [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-556">**CIM- \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-556">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dd>

<span data-ttu-id="a2b9c-557">Die [**CIM \_ physicalpackage**](cim-physicalpackage.md) -Klasse stellt physische Elemente dar, die andere Komponenten enthalten oder hosten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-557">The [**CIM\_PhysicalPackage**](cim-physicalpackage.md) class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="a2b9c-558">Beispiele hierfür sind ein Regal Gehäuse oder eine Adapterkarte.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-558">Examples are a rack enclosure or an adapter card.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-559">**CIM- \_ pointingdevice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-559">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-560">Die [**CIM \_ pointingdevice**](cim-pointingdevice.md) -Klasse stellt ein Gerät dar, das auf die Bereiche auf der Anzeige zeigt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-560">The [**CIM\_PointingDevice**](cim-pointingdevice.md) class represents a device that points to regions on the display.</span></span> <span data-ttu-id="a2b9c-561">Jedes Gerät, das einen Zeiger bearbeitet oder auf Bereiche in einer visuellen Anzeige zeigt, ist ein Member dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-561">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="a2b9c-562">Beispielsweise eine Maus, einen Tablettstift, ein Touchpad oder ein Tablet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-562">For example, a mouse, stylus, touch pad, or tablet.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-563">**CIM- \_ potsmodem**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-563">**CIM\_POTSModem**</span></span>](cim-potsmodem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-564">Die CIM-Klasse " [**\_ potsmodem**](cim-potsmodem.md) " stellt ein Gerät dar, das binäre Daten in Wellen Modulationen für die Sound basierte Übertragung übersetzt, indem eine Verbindung mit dem reinen Telefon System ("Pots") hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-564">The [**CIM\_POTSModem**](cim-potsmodem.md) class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-565">**CIM- \_ Netzteil**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-565">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> <dd>

<span data-ttu-id="a2b9c-566">Die [**CIM- \_ PowerSupply**](cim-powersupply.md) -Klasse stellt die Funktionen und die Verwaltung des logischen netzwerknetzwerkgeräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-566">The [**CIM\_PowerSupply**](cim-powersupply.md) class represents the capabilities and management of the power supply logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-567">**CIM- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-567">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dd>

<span data-ttu-id="a2b9c-568">Die [**CIM- \_ Drucker**](cim-printer.md) Klasse stellt die Funktionen und die Verwaltung des logischen Drucker Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-568">The [**CIM\_Printer**](cim-printer.md) class represents the capabilities and management of the printer logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-569">**CIM- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-569">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dd>

<span data-ttu-id="a2b9c-570">Die [**CIM- \_ Prozess**](cim-process.md) Klasse stellt eine einzelne Instanz eines laufenden Programms dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-570">The [**CIM\_Process**](cim-process.md) class represents a single instance of a running program.</span></span> <span data-ttu-id="a2b9c-571">Ein Benutzer sieht in der Regel einen Prozess als Anwendung oder Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-571">A user typically sees a process as an application or task.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-572">**CIM- \_ processexecutable**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-572">**CIM\_ProcessExecutable**</span></span>](cim-processexecutable.md)
</dt> <dd>

<span data-ttu-id="a2b9c-573">Die [**CIM \_ processexecutable**](cim-processexecutable.md) -Klasse stellt einen Link zwischen einem Prozess und einer Datendatei dar und gibt an, dass die Datei an der Ausführung des Prozesses beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-573">The [**CIM\_ProcessExecutable**](cim-processexecutable.md) class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-574">**CIM- \_ Prozessor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-574">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-575">Die [**CIM- \_ Prozessor**](cim-processor.md) Klasse stellt die Funktionen und die Verwaltung des logischen Prozessor Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-575">The [**CIM\_Processor**](cim-processor.md) class represents the capabilities and management of the processor logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-576">**CIM- \_ ProcessThread**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-576">**CIM\_ProcessThread**</span></span>](cim-processthread.md)
</dt> <dd>

<span data-ttu-id="a2b9c-577">Die [**CIM- \_ ProcessThread**](cim-processthread.md) -Klasse stellt einen Link zwischen einem Prozess und den Threads dar, die im Kontext des Prozesses ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-577">The [**CIM\_ProcessThread**](cim-processthread.md) class represents a link between a process and the threads running in the context of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-578">**CIM- \_ Produkt**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-578">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dd>

<span data-ttu-id="a2b9c-579">Die [**CIM- \_ Produkt**](cim-product.md) Klasse ist eine konkrete Klasse, die eine Auflistung physischer Elemente, Software Features und anderer Produkte darstellt, die als Einheit erworben wurden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-579">The [**CIM\_Product**](cim-product.md) class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="a2b9c-580">Der Erwerb impliziert eine Vereinbarung zwischen dem Lieferanten und dem Consumer, die Auswirkungen auf die Produkt Lizenzierung, den Support und die Gewährleistung haben kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-580">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-581">**CIM \_ productfru**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-581">**CIM\_ProductFRU**</span></span>](cim-productfru.md)
</dt> <dd>

<span data-ttu-id="a2b9c-582">Die [**CIM \_ productfru**](cim-productfru.md) -Klasse stellt eine Zuordnung zwischen dem Produkt und einer ersetzbaren (Feld) Einheit (FRU) dar, die Informationen zu Produktkomponenten bereitstellt, die bereits waren oder ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-582">The [**CIM\_ProductFRU**](cim-productfru.md) class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-583">**CIM \_ productparser**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-583">**CIM\_ProductParentChild**</span></span>](cim-productparentchild.md)
</dt> <dd>

<span data-ttu-id="a2b9c-584">Die [**CIM \_ productparser**](cim-productparentchild.md) -Zuordnung definiert eine Hierarchie mit über-und untergeordneten Elementen zwischen Produkten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-584">The [**CIM\_ProductParentChild**](cim-productparentchild.md) association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="a2b9c-585">Beispielsweise kann ein Produkt mit anderen Produkten gebündelt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-585">For example, a product can come bundled with other products.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-586">**CIM \_ productphysicalelements**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-586">**CIM\_ProductPhysicalElements**</span></span>](cim-productphysicalelements.md)
</dt> <dd>

<span data-ttu-id="a2b9c-587">Die [**CIM \_ productphysicalelements**](cim-productphysicalelements.md) -Klasse stellt die physischen Elemente dar, die ein Produkt bilden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-587">The [**CIM\_ProductPhysicalElements**](cim-productphysicalelements.md) class represents the physical elements that make up a product.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-588">**CIM \_ productproductabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-588">**CIM\_ProductProductDependency**</span></span>](cim-productproductdependency.md)
</dt> <dd>

<span data-ttu-id="a2b9c-589">Die [**CIM \_ productproductdepen-Klasse**](cim-productproductdependency.md) stellt eine Zuordnung zwischen zwei Produkten dar, die angibt, dass eine für die andere installiert werden muss oder nicht.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-589">The [**CIM\_ProductProductDependency**](cim-productproductdependency.md) class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="a2b9c-590">Dies entspricht konzeptionell der [**CIM \_ serviceserviceabhängigkeiten**](cim-serviceservicedependency.md) -Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-590">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-591">**CIM \_ productsoftwarefeatures**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-591">**CIM\_ProductSoftwareFeatures**</span></span>](cim-productsoftwarefeatures.md)
</dt> <dd>

<span data-ttu-id="a2b9c-592">Die [**CIM \_ productsoftwarefeatures**](cim-productsoftwarefeatures.md) -Zuordnung identifiziert die Software Features für ein bestimmtes Produkt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-592">The [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association identifies the software features for a particular product.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-593">**CIM- \_ productsupport**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-593">**CIM\_ProductSupport**</span></span>](cim-productsupport.md)
</dt> <dd>

<span data-ttu-id="a2b9c-594">Die [**CIM \_ productsupport**](cim-productsupport.md) -Klasse stellt eine Zuordnung Zwischenprodukt und Support Zugriff dar, die die Art der Unterstützung für das Produkt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-594">The [**CIM\_ProductSupport**](cim-productsupport.md) class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="a2b9c-595">Für ein Produkt sind verschiedene Support Typen verfügbar. das gleiche Support Objekt bietet Unterstützung für mehrere Produkte.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-595">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-596">**CIM \_ protectedspaceblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-596">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-597">Die [**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md) -Klasse stellt adressierbare logische Block Adressen dar, die als einzelner Speicherblock behandelt werden, sich jedoch in einem einzelnen physischen Block befinden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-597">The [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) class represents addressable logical-block addresses, which are treated as a single storage extent, but are located on a single physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-598">**CIM \_ psextentbasedonpblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-598">**CIM\_PSExtentBasedOnPExtent**</span></span>](cim-psextentbasedonpextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-599">Die [**CIM \_ psextentbasedonpblock**](cim-psextentbasedonpextent.md) -Klasse ordnet Blöcke mit geschütztem Speicherplatz zu, die auf einem physischen Block basieren.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-599">The [**CIM\_PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) class associates protected space extents that are based on a physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-600">**CIM- \_ Rack**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-600">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> <dd>

<span data-ttu-id="a2b9c-601">Die [**CIM- \_ Rack**](cim-rack.md) -Klasse stellt ein Gestell (ein physischer Frame oder Gehäuse) dar, in dem das Chassis gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-601">The [**CIM\_Rack**](cim-rack.md) class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="a2b9c-602">In der Regel stellt ein Rack das Gehäuse dar. Alle funktionierenden Komponenten werden in das Chassis gepackt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-602">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-603">**CIM \_ erkennt**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-603">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dd>

<span data-ttu-id="a2b9c-604">Die [**CIM \_**](cim-realizes.md) -Klasse stellt die Zuordnung dar, die die Zuordnung zwischen einem logischen Gerät und der physischen Komponente definiert, die das Gerät implementiert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-604">The [**CIM\_Realizes**](cim-realizes.md) class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-605">**CIM \_ realizesaggregatepblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-605">**CIM\_RealizesAggregatePExtent**</span></span>](cim-realizesaggregatepextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-606">Die CIM-Erweiterung " [**\_ realizesaggregatepblock**](cim-realizesaggregatepextent.md) " stellt die Beziehung dar, in der die [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) -Klasse auf einem physischen Medium realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-606">The [**CIM\_RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-607">**CIM- \_ realizesdiskpartition**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-607">**CIM\_RealizesDiskPartition**</span></span>](cim-realizesdiskpartition.md)
</dt> <dd>

<span data-ttu-id="a2b9c-608">Die CIM-Klasse " [**\_ realizesdiskpartition**](cim-realizesdiskpartition.md) " stellt eine Datenträger Partition auf einem physischen Medium dar, die die Erstellung von Partitionen auf einem unformatierten SCSI-oder IDE-Laufwerk modelliert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-608">The [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-609">**CIM- \_ realizespblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-609">**CIM\_RealizesPExtent**</span></span>](cim-realizespextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-610">Die CIM-Erweiterung " [**\_ realizespblock**](cim-realizespextent.md) " stellt die Beziehung dar, in der physische Blöcke auf einem physischen Medium realisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-610">The [**CIM\_RealizesPExtent**](cim-realizespextent.md) association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="a2b9c-611">Außerdem wird die Startadresse des physischen Wertebereichs auf dem physischen Medium angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-611">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-612">**CIM- \_ rebootaction**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-612">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-613">Die [**CIM \_ rebootaction**](cim-rebootaction.md) -Klasse verursacht einen Systemneustart, bei dem das Softwareelement installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-613">The [**CIM\_RebootAction**](cim-rebootaction.md) class causes a system reboot where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-614">**CIM \_ redundant cycomponent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-614">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-615">Die [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) -Klasse ordnet eine Redundanz Gruppe zu, die aus verwalteten Systemelementen besteht, und gibt an, dass die Elemente zusammen Redundanz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-615">The [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="a2b9c-616">Alle Elemente, die in einer Redundanz Gruppe aggregiert werden, sollten Instanziierungen der gleichen Objektklasse sein.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-616">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-617">**CIM- \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-617">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> <dd>

<span data-ttu-id="a2b9c-618">Die [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) -Klasse stellt eine Auflistung verwalteter Systemelemente dar, die angibt, dass die aggregierten Komponenten zusammen Redundanz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-618">The [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="a2b9c-619">Alle Elemente, die in einer Redundanz Gruppe aggregiert werden, sollten Instanziierungen der gleichen Objektklasse sein.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-619">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-620">**CIM- \_ Kühlung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-620">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dd>

<span data-ttu-id="a2b9c-621">Die [**CIM- \_ kühl**](cim-refrigeration.md) Klasse stellt die Funktionen und die Verwaltung eines kühl Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-621">The [**CIM\_Refrigeration**](cim-refrigeration.md) class represents the capabilities and management of a refrigeration cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-622">**CIM \_ relatedstatistics**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-622">**CIM\_RelatedStatistics**</span></span>](cim-relatedstatistics.md)
</dt> <dd>

<span data-ttu-id="a2b9c-623">Die [**CIM \_ relatedstatistics**](cim-relatedstatistics.md) -Zuordnung stellt Hierarchien und Abhängigkeiten verwandter [**CIM \_ statisticalinformation**](cim-statisticalinformation.md) -Klassen dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-623">The [**CIM\_RelatedStatistics**](cim-relatedstatistics.md) association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-624">**CIM- \_ remotefile System**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-624">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-625">Die [**CIM- \_ remotefile**](cim-remotefilesystem.md) System-Klasse stellt ein Remote Dateisystem dar, auf das über einen netzwerkbezogenen Dienst zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-625">The [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md) class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="a2b9c-626">In diesem Fall wird der Dateispeicher von einem Computer gehostet, der als Dateiserver fungiert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-626">In this case, the file store is hosted by a computer, which acts as a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-627">**CIM \_ removedirectoriyaction**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-627">**CIM\_RemoveDirectoryAction**</span></span>](cim-removedirectoryaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-628">Die [**CIM \_ removedirectoryaction**](cim-removedirectoryaction.md) -Klasse entfernt Verzeichnisse für Software Elemente.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-628">The [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class removes directories for software elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-629">**CIM- \_ removefileaction**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-629">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-630">Mit der [**CIM \_ removefileaction**](cim-removefileaction.md) -Klasse werden Dateien deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-630">The [**CIM\_RemoveFileAction**](cim-removefileaction.md) class uninstalls files.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-631">**CIM-Ersatz \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-631">**CIM\_ReplacementSet**</span></span>](cim-replacementset.md)
</dt> <dd>

<span data-ttu-id="a2b9c-632">Die [**CIM \_ replacementset**](cim-replacementset.md) -Klasse aggregiert physische Elemente, die zusammen ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-632">The [**CIM\_ReplacementSet**](cim-replacementset.md) class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="a2b9c-633">Wenn Sie z. b. eine Speicherkarte austauschen, können die Komponenten Speicher-Chips auch entfernt und ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-633">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="a2b9c-634">Oder diese Zuordnung kann verwendet werden, um einen Satz von Speicherchips zu ersetzen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-634">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-635">**CIM \_ resiwisonblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-635">**CIM\_ResidesOnExtent**</span></span>](cim-residesonextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-636">Die [**CIM \_ residesonblock**](cim-residesonextent.md) -Klasse stellt eine Zuordnung zwischen einem Dateisystem und dem Speicherblock dar, in dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-636">The [**CIM\_ResidesOnExtent**](cim-residesonextent.md) class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="a2b9c-637">In der Regel befindet sich ein Dateisystem auf einem logischen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-637">Typically, a file system resides on a logical disk.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-638">**CIM- \_ runningos**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-638">**CIM\_RunningOS**</span></span>](cim-runningos.md)
</dt> <dd>

<span data-ttu-id="a2b9c-639">Die [**CIM \_ runningos**](cim-runningos.md) -Klasse stellt das aktuell ausgeführte Betriebssystem dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-639">The [**CIM\_RunningOS**](cim-runningos.md) class represents the currently executing operating system.</span></span> <span data-ttu-id="a2b9c-640">Höchstens ein Betriebssystem kann zu einem beliebigen Zeitpunkt auf einem Computersystem ausgeführt werden. das Computersystem ist möglicherweise nicht gestartet, oder sein Betriebssystem ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-640">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-641">**CIM \_ sapsapabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-641">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> <dd>

<span data-ttu-id="a2b9c-642">Die [**CIM \_ sapsapabhängigkeits**](cim-sapsapdependency.md) -Klasse ist eine Zuordnung zwischen zwei Dienst Zugriffs Punkten (SAPS), mit der angegeben wird, dass die zweite SAP-Komponente erforderlich ist, damit der erste SAP eine Verbindung mit dem Dienst herstellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-642">The [**CIM\_SAPSAPDependency**](cim-sapsapdependency.md) class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-643">**CIM- \_ Scanner**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-643">**CIM\_Scanner**</span></span>](cim-scanner.md)
</dt> <dd>

<span data-ttu-id="a2b9c-644">Der [**CIM- \_ Scanner**](cim-scanner.md) stellt die Funktionen und die Verwaltung des logischen Scanner-Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-644">The [**CIM\_Scanner**](cim-scanner.md) represents the capabilities and management of the scanner logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-645">**CIM- \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-645">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-646">Die [**CIM \_ SCSIController**](cim-scsicontroller.md) -Klasse stellt die Funktionen und die Verwaltung des logischen SCSI-Controller Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-646">The [**CIM\_SCSIController**](cim-scsicontroller.md) class represents the capabilities and management of the SCSI controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-647">**CIM- \_ scsiinterface**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-647">**CIM\_SCSIInterface**</span></span>](cim-scsiinterface.md)
</dt> <dd>

<span data-ttu-id="a2b9c-648">stellt eine [**CIM \_ controlledby**](cim-controlledby.md) -Beziehung dar, die angibt, auf welche Geräte über einen SCSI-Controller und die Zugriffs Eigenschaften zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-648">represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-649">**CIM- \_ Sensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-649">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-650">Die [**CIM- \_ Sensor**](cim-sensor.md) Klasse stellt ein Hardware Gerät dar, mit dem die Eigenschaften einer physischen Eigenschaft (z. b. die Temperatur-oder Spannungs Merkmale eines einheitlichen Computer Systems) gemessen werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-650">The [**CIM\_Sensor**](cim-sensor.md) class represents a hardware device that is capable of measuring the characteristics of a physical property (for example, the temperature or voltage characteristics of a unitary computer system).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-651">**CIM- \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-651">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-652">Die [**CIM \_ SerialController**](cim-serialcontroller.md) -Klasse stellt die Funktionen und die Verwaltung des logischen Geräts des seriellen Ports dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-652">The [**CIM\_SerialController**](cim-serialcontroller.md) class represents the capabilities and management of the serial port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-653">**CIM- \_ serialschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-653">**CIM\_SerialInterface**</span></span>](cim-serialinterface.md)
</dt> <dd>

<span data-ttu-id="a2b9c-654">Die [**CIM \_ serialinterface**](cim-serialinterface.md) -Klasse stellt eine [**CIM \_ controlledby**](cim-controlledby.md) -Beziehung dar, die angibt, auf welche Geräte über den seriellen Controller und die Eigenschaften des Zugriffs zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-654">The [**CIM\_SerialInterface**](cim-serialinterface.md) class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-655">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-655">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dd>

<span data-ttu-id="a2b9c-656">Die [**CIM- \_ Dienst**](cim-service.md) Klasse stellt ein logisches Element dar, das Informationen zur Darstellung und Verwaltung der von einem Gerät oder einer Software Funktion bereitgestellten Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-656">The [**CIM\_Service**](cim-service.md) class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="a2b9c-657">Bei einem Dienst handelt es sich um ein allgemeines Objekt, um die Implementierung von Funktionen zu konfigurieren und zu verwalten. Es handelt sich nicht um die eigentliche Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-657">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-658">**CIM \_ serviceaccessbysap**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-658">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="a2b9c-659">Die [**CIM \_ serviceaccessbysap**](cim-serviceaccessbysap.md) Association-Klasse stellt die Zugriffspunkte für einen Dienst dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-659">The [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md) association class represents the access points for a service.</span></span> <span data-ttu-id="a2b9c-660">Beispielsweise kann auf einen Drucker über NetWare, Macintosh oder Windows-Dienst Zugriffspunkte (SAPS) zugegriffen werden, die potenziell auf unterschiedlichen Systemen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-660">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-661">**CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-661">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dd>

<span data-ttu-id="a2b9c-662">Die [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) -Klasse stellt die Möglichkeit dar, einen Dienst zu verwenden oder aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-662">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="a2b9c-663">Zugriffspunkte stellen Dienste dar, die von anderen Entitäten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-663">Access points represent services that are available for use by other entities.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-664">**CIM \_ servicesapabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-664">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> <dd>

<span data-ttu-id="a2b9c-665">Die [**CIM \_ servicesapdepen-Klasse**](cim-servicesapdependency.md) stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der angibt, dass der referenzierte SAP vom Dienst verwendet wird, um seine Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-665">The [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-666">**CIM \_ serviceserviceabhängigkeiten**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-666">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dd>

<span data-ttu-id="a2b9c-667">Die [**CIM \_ serviceservicedepen-Klasse**](cim-serviceservicedependency.md) stellt eine Zuordnung zwischen zwei Diensten dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-667">The [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) class represents an association between two services.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-668">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-668">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="a2b9c-669">Die [**CIM- \_ Einstellungs**](cim-setting.md) Klasse stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-669">The [**CIM\_Setting**](cim-setting.md) class represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-670">**CIM- \_ settingcheck**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-670">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> <dd>

<span data-ttu-id="a2b9c-671">Die [**CIM \_ settingcheck**](cim-settingcheck.md) -Klasse gibt Informationen an, die erforderlich sind, um eine bestimmte Einstellungsdatei für einen bestimmten Eintrag zu überprüfen, der einen Wert gleich dem angegebenen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-671">The [**CIM\_SettingCheck**](cim-settingcheck.md) class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="a2b9c-672">Bei allen vergleichen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-672">All comparisons are assumed to be case insensitive.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-673">**CIM- \_ settingcontext**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-673">**CIM\_SettingContext**</span></span>](cim-settingcontext.md)
</dt> <dd>

<span data-ttu-id="a2b9c-674">Die [**CIM \_ settingcontext**](cim-settingcontext.md) -Klasse ordnet Konfigurationsobjekte Einstellungs Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-674">The [**CIM\_SettingContext**](cim-settingcontext.md) class associates configuration objects with setting objects.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-675">**CIM- \_ Slot**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-675">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dd>

<span data-ttu-id="a2b9c-676">Die [**CIM- \_ Slot**](cim-slot.md) -Klasse stellt Connectors dar, in die Pakete eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-676">The [**CIM\_Slot**](cim-slot.md) class represents connectors into which packages are inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-677">**CIM \_ slotinslot**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-677">**CIM\_SlotInSlot**</span></span>](cim-slotinslot.md)
</dt> <dd>

<span data-ttu-id="a2b9c-678">Die [**CIM \_ slotinslot**](cim-slotinslot.md) -Beziehung stellt die Fähigkeit eines speziellen Adapters dar, die vorhandene slotstruktur zu erweitern, um ansonsten inkompatible Karten zu ermöglichen, die an einem Frame oder einem hostingboard angeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-678">The [**CIM\_SlotInSlot**](cim-slotinslot.md) relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-679">**CIM- \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-679">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> <dd>

<span data-ttu-id="a2b9c-680">Die [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Klasse zerlegt ein [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Objekt in einen Satz individuell verwaltbarer oder bereitstell barer Teile für eine bestimmte Plattform.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-680">The [**CIM\_SoftwareElement**](cim-softwareelement.md) class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="a2b9c-681">Die Plattform eines Software Elements wird durch die zugrunde liegende Hardwarearchitektur und das Betriebssystem eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-681">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-682">**CIM- \_ softwareelementactions**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-682">**CIM\_SoftwareElementActions**</span></span>](cim-softwareelementactions.md)
</dt> <dd>

<span data-ttu-id="a2b9c-683">Die [**CIM- \_ softwareelementactions**](cim-softwareelementactions.md) -Zuordnung identifiziert die Aktionen für ein Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-683">The [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association identifies the actions for a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-684">**CIM- \_ softwareelementchecks**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-684">**CIM\_SoftwareElementChecks**</span></span>](cim-softwareelementchecks.md)
</dt> <dd>

<span data-ttu-id="a2b9c-685">Die [**CIM- \_ softwareelementchecks**](cim-softwareelementchecks.md) -Zuordnungs Klasse verknüpft ein Softwareelement mit Bedingungs-oder Standortinformationen, die für eine Funktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-685">The [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association class relates a software element with condition or location information that a feature may require.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-686">**CIM- \_ softwareelementversioncheck**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-686">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> <dd>

<span data-ttu-id="a2b9c-687">Die [**CIM \_ softwareelementversioncheck**](cim-softwareelementversioncheck.md) -Klasse stellt einen Typ von Softwareelement dar, der in der Umgebung vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-687">The [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class represents a type of software element that must exist in the environment.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-688">**CIM- \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-688">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> <dd>

<span data-ttu-id="a2b9c-689">Die [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Klasse stellt eine bestimmte Funktion oder Funktion eines Produkts oder Anwendungs Systems dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-689">The [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class represents a particular function or capability of a product or application system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-690">**CIM- \_ softwarefeaturesapimplementation**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-690">**CIM\_SoftwareFeatureSAPImplementation**</span></span>](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

<span data-ttu-id="a2b9c-691">Die [**CIM- \_ softwarefeaturesapimplementation**](cim-softwarefeaturesapimplementation.md) -Klasse stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und der Art der Implementierung in Software dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-691">The [**CIM\_SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-692">**CIM \_ softwarefeatureserviceimplementation**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-692">**CIM\_SoftwareFeatureServiceImplementation**</span></span>](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="a2b9c-693">Die [**CIM \_ softwarefeatureserviceimplementation**](cim-softwarefeatureserviceimplementation.md) -Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung in Software dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-693">The [**CIM\_SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) class represents an association between a service and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-694">**CIM- \_ softwarefeaturesoftwareelements**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-694">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

<span data-ttu-id="a2b9c-695">Die [**CIM- \_ softwarefeaturesoftwareelements**](cim-softwarefeaturesoftwareelements.md) -Zuordnung identifiziert die Software Elemente, die ein bestimmtes Software Feature bilden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-695">The [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) association identifies the software elements that make up a specific software feature.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-696">**CIM- \_ SpareGroup**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-696">**CIM\_SpareGroup**</span></span>](cim-sparegroup.md)
</dt> <dd>

<span data-ttu-id="a2b9c-697">Die [**CIM \_ SpareGroup**](cim-sparegroup.md) -Klasse wird von der [**CIM \_ redundant cygroup**](cim-redundancygroup.md) -Klasse abgeleitet und gibt an, dass mindestens eines der aggregierten Elemente geschont werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-697">The [**CIM\_SpareGroup**](cim-sparegroup.md) class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-698">**CIM- \_ statisticalinformation**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-698">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dd>

<span data-ttu-id="a2b9c-699">Die [**CIM \_ statisticalinformation**](cim-statisticalinformation.md) -Klasse ist eine Stamm Klasse für die beliebige Auflistung von statistischen Daten oder Metriken, die für ein oder mehrere verwaltete Systemelemente anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-699">The [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-700">**CIM- \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-700">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> <dd>

<span data-ttu-id="a2b9c-701">Die [**CIM \_ Statistics**](cim-statistics.md) -Klasse stellt eine Zuordnung dar, die verwaltete Systemelemente mit den statistischen Gruppen verknüpft, die für Sie gelten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-701">The [**CIM\_Statistics**](cim-statistics.md) class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-702">**CIM- \_ storagemängel**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-702">**CIM\_StorageDefect**</span></span>](cim-storagedefect.md)
</dt> <dd>

<span data-ttu-id="a2b9c-703">Die [**CIM \_ storagemängel**](cim-storagedefect.md) -Aggregation sammelt die Speicherfehler für einen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-703">The [**CIM\_StorageDefect**](cim-storagedefect.md) aggregation collects the storage errors for a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-704">**CIM- \_ storageerror**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-704">**CIM\_StorageError**</span></span>](cim-storageerror.md)
</dt> <dd>

<span data-ttu-id="a2b9c-705">Die [**CIM \_ storageerror**](cim-storageerror.md) -Klasse stellt Blöcke von Medien oder Speicherplatz dar, die aufgrund von Fehlern nicht verwendeter Speicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-705">The [**CIM\_StorageError**](cim-storageerror.md) class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="a2b9c-706">Der Schlüssel der-Klasse ist die **StartingAddress** -Eigenschaft der Bytes, die fehlerhaft sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-706">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-707">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-707">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-708">Die [**CIM \_ storageblock**](cim-storageextent.md) -Klasse stellt die Funktionen und die Verwaltung der verschiedenen Medien dar, die zum Speichern von Daten und zum Abrufen des Datenabrufs vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-708">The [**CIM\_StorageExtent**](cim-storageextent.md) class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="a2b9c-709">Diese übergeordnete Klasse kann die verschiedenen Komponenten von RAID (Hardware oder Software) oder einen logischen Bereich auf physischen Medien darstellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-709">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-710">**CIM \_ storageredundancygroup**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-710">**CIM\_StorageRedundancyGroup**</span></span>](cim-storageredundancygroup.md)
</dt> <dd>

<span data-ttu-id="a2b9c-711">Die [**CIM \_ storageredundancygroup**](cim-storageredundancygroup.md) -Klasse stellt Massenspeicher bezogene Redundanz Informationen dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-711">The [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class represents mass storage-related redundancy information.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-712">**CIM- \_ supportaccess**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-712">**CIM\_SupportAccess**</span></span>](cim-supportaccess.md)
</dt> <dd>

<span data-ttu-id="a2b9c-713">Die [**CIM \_ supportaccess**](cim-supportaccess.md) -Klasse definiert, wie Sie Unterstützung für ein Produkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-713">The [**CIM\_SupportAccess**](cim-supportaccess.md) class defines how to obtain assistance for a product.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-714">**CIM- \_ Swap-Papier**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-714">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> <dd>

<span data-ttu-id="a2b9c-715">Die [**CIM \_ swapspacecheck**](cim-swapspacecheck.md) -Klasse gibt die Menge an Auslagerungs Bereich an, die auf dem System verfügbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-715">The [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class specifies the amount of swap space that must be available on the system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-716">**CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-716">**CIM\_System**</span></span>](cim-system.md)
</dt> <dd>

<span data-ttu-id="a2b9c-717">Die [**CIM- \_ System**](cim-system.md) Klasse aggregiert einen Aufzähl baren Satz verwalteter System Elemente.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-717">The [**CIM\_System**](cim-system.md) class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="a2b9c-718">Die Aggregation funktioniert als Ganzes funktionstüchtig.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-718">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="a2b9c-719">Innerhalb einer bestimmten Unterklasse des Systems gibt es eine klar definierte Liste der verwalteten System Element Klassen, deren Instanzen aggregiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-719">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-720">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-720">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dd>

<span data-ttu-id="a2b9c-721">eine Common Information Model (CIM)-Zuordnungs Klasse, mit der Beziehungen zwischen einem System und den verwalteten Systemelementen hergestellt werden, von denen es zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-721">a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-722">**CIM- \_ System Gerät**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-722">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-723">Die [**CIM- \_ SystemDevice**](cim-systemdevice.md) -Zuordnung stellt eine explizite Beziehung dar, in der logische Geräte von einem System aggregiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-723">The [**CIM\_SystemDevice**](cim-systemdevice.md) association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-724">**CIM- \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-724">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dd>

<span data-ttu-id="a2b9c-725">Die [**CIM- \_ systemressourcenklasse**](cim-systemresource.md) stellt eine Entität dar, die von BIOS verwaltet wird, oder ein Betriebssystem, das für die Verwendung durch Software und logische Geräte verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-725">The [**CIM\_SystemResource**](cim-systemresource.md) class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-726">**CIM- \_ Tachometer**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-726">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> <dd>

<span data-ttu-id="a2b9c-727">Die CIM-Klasse " [**\_ Tachometer**](cim-tachometer.md) " ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-727">The [**CIM\_Tachometer**](cim-tachometer.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-728">**CIM- \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-728">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dd>

<span data-ttu-id="a2b9c-729">Die [**CIM \_ TapeDrive**](cim-tapedrive.md) -Klasse stellt ein Bandlaufwerk auf dem System dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-729">The [**CIM\_TapeDrive**](cim-tapedrive.md) class represents a tape drive on the system.</span></span> <span data-ttu-id="a2b9c-730">Bandlaufwerke unterscheiden sich hauptsächlich darin, dass nur sequenziell auf Sie zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-730">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-731">**CIM- \_ Temperatursensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-731">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-732">Die [**CIM- \_ Temperatursensor**](cim-temperaturesensor.md) Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-732">The [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-733">**CIM- \_ Thread**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-733">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dd>

<span data-ttu-id="a2b9c-734">Die [**CIM- \_ Thread**](cim-thread.md) Klasse stellt die Möglichkeit dar, gleichzeitig Einheiten eines Prozesses oder einer Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-734">The [**CIM\_Thread**](cim-thread.md) class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="a2b9c-735">Ein Prozess kann über viele Threads verfügen, von denen jede für den Prozess schwach ist.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-735">A process can have many threads, each of which is weak to the process.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-736">**CIM- \_ Verzeichnis Aktion**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-736">**CIM\_ToDirectoryAction**</span></span>](cim-todirectoryaction.md)
</dt> <dd>

<span data-ttu-id="a2b9c-737">Die [**CIM \_**](cim-todirectoryaction.md) -Verzeichnis Verbindungs Zuordnung identifiziert das Zielverzeichnis für die Datei Aktion.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-737">The [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-738">**CIM- \_ Verzeichnis Spezifikation**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-738">**CIM\_ToDirectorySpecification**</span></span>](cim-todirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="a2b9c-739">Die [**CIM \_**](cim-todirectoryspecification.md) -Verzeichnisdienst Spezifikation identifiziert das Zielverzeichnis für die Datei Aktion.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-739">The [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-740">**CIM- \_ uninterruptiblepowersupply**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-740">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> <dd>

<span data-ttu-id="a2b9c-741">Die [**CIM-Klasse \_ uninterruptiblepowersupply**](cim-uninterruptiblepowersupply.md) stellt die Funktionen und die Verwaltung einer unterbrechungsfreien Stromversorgung (UPS) dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-741">The [**CIM\_UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-742">**CIM \_ unitarycomputersystem**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-742">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dd>

<span data-ttu-id="a2b9c-743">Die [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md) -Klasse stellt einen Desktop-, Mobil-, Netzwerk Computer-, Server-oder anderen Typ eines Computer Systems mit einem einzelnen Knoten dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-743">The [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-744">**CIM-Start \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-744">**CIM\_USBController**</span></span>](cim-usbcontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-745">Die [**CIM \_**](cim-usbcontroller.md) -Klasse "Start Controller" stellt die Funktionen und die Verwaltung eines USB-Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-745">The [**CIM\_USBController**](cim-usbcontroller.md) class represents the capabilities and management of a USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-746">**CIM-Start \_ Controller-controllerhashub**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-746">**CIM\_USBControllerHasHub**</span></span>](cim-usbcontrollerhashub.md)
</dt> <dd>

<span data-ttu-id="a2b9c-747">Die [**CIM \_**](cim-usbcontrollerhashub.md) -Klasse "-Klasse" definiert die Hubs, die dem USB-Controller nachgelagert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-747">The [**CIM\_USBControllerHasHub**](cim-usbcontrollerhashub.md) class defines the hubs that are downstream of the USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-748">**CIM-Start \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-748">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-749">Die [**CIM \_**](cim-usbdevice.md) -Klasse "-Klasse" stellt die Verwaltungsmerkmale eines USB-Geräts dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-749">The [**CIM\_USBDevice**](cim-usbdevice.md) class represents the management characteristics of a USB device.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-750">**CIM-Startseite \_**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-750">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> <dd>

<span data-ttu-id="a2b9c-751">Die [**CIM \_**](cim-usbhub.md) -Klasse "-Klasse" stellt die Funktionen und die Verwaltung eines USB-Hubs dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-751">The [**CIM\_USBHub**](cim-usbhub.md) class represents the capabilities and management of a USB hub.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-752">**CIM- \_ userdevice**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-752">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dd>

<span data-ttu-id="a2b9c-753">Die [**CIM- \_ userdevice**](cim-userdevice.md) -Klasse ist eine übergeordnete Klasse, von der andere Klassen, z. b. [**CIM- \_ Tastatur**](cim-keyboard.md) oder [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md), abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-753">The [**CIM\_UserDevice**](cim-userdevice.md) class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="a2b9c-754">Benutzer Geräte sind logische Geräte, die es einem Computersystem ermöglichen, Daten einzugeben, anzuzeigen oder zu hören.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-754">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-755">**CIM \_ versioncompatibilitycheck**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-755">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> <dd>

<span data-ttu-id="a2b9c-756">Die [**CIM \_ versioncompatibilitycheck**](cim-versioncompatibilitycheck.md) -Klasse gibt an, ob es zulässig ist, den nächsten Zustand eines Software Elements zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-756">The [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class specifies whether it is permissible to create the next state of a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-757">**CIM- \_ videobioselements**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-757">**CIM\_VideoBIOSElement**</span></span>](cim-videobioselement.md)
</dt> <dd>

<span data-ttu-id="a2b9c-758">Die [**CIM \_ videobioselfigure**](cim-videobioselement.md) -Klasse stellt die Software auf niedriger Ebene dar, die in nicht flüchtigen Speicher geladen wird und zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-758">The [**CIM\_VideoBIOSElement**](cim-videobioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-759">**CIM \_ videobiosfeature**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-759">**CIM\_VideoBIOSFeature**</span></span>](cim-videobiosfeature.md)
</dt> <dd>

<span data-ttu-id="a2b9c-760">Die [**CIM \_ videobiosfeature**](cim-videobiosfeature.md) -Klasse stellt die Funktionen der Low-Level-Software dar, die zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-760">The [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-761">**CIM \_ videobiosfeaturevideobioselements**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-761">**CIM\_VideoBIOSFeatureVideoBIOSElements**</span></span>](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

<span data-ttu-id="a2b9c-762">Die [**CIM \_ videobiosfeaturevideobioselements**](cim-videobiosfeaturevideobioselements.md) -Klasse ordnet eine Video-BIOS-Funktion und ihre aggregierten Video-BIOS-Elemente zu.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-762">The [**CIM\_VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-763">**CIM- \_ Videocontroller**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-763">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> <dd>

<span data-ttu-id="a2b9c-764">Die [**CIM \_ Videocontroller**](cim-videocontroller.md) -Klasse stellt die Funktionen und die Verwaltung des Video Controllers dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-764">The [**CIM\_VideoController**](cim-videocontroller.md) class represents the capabilities and management of the video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-765">**CIM- \_ videocontrollerresolution**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-765">**CIM\_VideoControllerResolution**</span></span>](cim-videocontrollerresolution.md)
</dt> <dd>

<span data-ttu-id="a2b9c-766">Die [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klasse stellt die verschiedenen Video Modi dar, die von einem Videocontroller unterstützt werden können.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-766">The [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class represents the various video modes that a video controller can support.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-767">**CIM- \_ videosetting**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-767">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dd>

<span data-ttu-id="a2b9c-768">Die [**CIM- \_ videosetting**](cim-videosetting.md) -Klasse ordnet das [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Einstellungs Objekt dem Controller zu, auf den es angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-768">The [**CIM\_VideoSetting**](cim-videosetting.md) class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-769">**CIM- \_ VolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-769">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> <dd>

<span data-ttu-id="a2b9c-770">Die [**CIM \_ VolatileStorage**](cim-volatilestorage.md) -Klasse stellt die Funktionen und die Verwaltung von flüchtigem Speicher dar.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-770">The [**CIM\_VolatileStorage**](cim-volatilestorage.md) class represents the capabilities and management of volatile storage.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-771">**CIM- \_ Temperatursensor**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-771">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dd>

<span data-ttu-id="a2b9c-772">Die CIM-Klasse " [**\_ VoltageSensor**](cim-voltagesensor.md) " ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-772">The [**CIM\_VoltageSensor**](cim-voltagesensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="a2b9c-773">Mit Ergänzungen der [**CIM- \_ Sensor**](cim-sensor.md) -und [**CIM- \_ numericsensor**](cim-numericsensor.md) -Klassen in Version 2,2 ist es nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-773">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-774">**CIM- \_ volumeset**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-774">**CIM\_VolumeSet**</span></span>](cim-volumeset.md)
</dt> <dd>

<span data-ttu-id="a2b9c-775">Die [**CIM \_ volumeset**](cim-volumeset.md) -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die der Betriebsumgebung zum Lesen und Schreiben von Benutzerdaten präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-775">The [**CIM\_VolumeSet**](cim-volumeset.md) class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span>

</dd> <dt>

[<span data-ttu-id="a2b9c-776">**CIM- \_ Wurm Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="a2b9c-776">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> <dd>

<span data-ttu-id="a2b9c-777">Die CIM-Klasse " [**\_ Wormdrive**](cim-wormdrive.md) " stellt die Funktionen und die Verwaltung eines Wurm Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="a2b9c-777">The [**CIM\_WORMDrive**](cim-wormdrive.md) class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

</dd> </dl>

 

 
