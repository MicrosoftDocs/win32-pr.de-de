---
description: Diese WMI-Klassen werden in CimWin32.mof deklariert.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: CIM-WMI-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9a01e0771645cf6101171ce870be593181cb61d6118e627b9bf96b61994be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420334"
---
# <a name="cim-wmi-provider"></a>CIM-WMI-Anbieter

Diese WMI-Klassen werden in CimWin32.mof deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**\_CIM-Aktion**](cim-action.md)
</dt> <dd>

Eine [**CIM \_ Action-Klasse**](cim-action.md) ist ein Vorgang, der Teil eines Prozesses ist, um entweder ein Softwareelement im nächsten Zustand zu erstellen oder das Softwareelement im aktuellen Zustand zu beseitigen.

</dd> <dt>

[**CIM \_ ActionSequence**](cim-actionsequence.md)
</dt> <dd>

Die [**CIM \_ ActionSequence-Zuordnung**](cim-actionsequence.md) definiert eine Reihe von Vorgängen, die das Softwareelement (auf das durch die [**CIM \_ SoftwareElementActions-Zuordnung**](cim-softwareelementactions.md) verwiesen wird) in den nächsten Zustand überarbeiten oder das Softwareelement aus seinem aktuellen Zustand entfernen.

</dd> <dt>

[**\_CIM-AktionenAsSpare**](cim-actsasspare.md)
</dt> <dd>

Die [**\_ CIM-Zuordnung "ActsAsSpare"**](cim-actsasspare.md) gibt an, welche Elemente ersatz- oder andere aggregierte Elemente ersetzen können. Ein Ersatz kann im Modus "Heißer Standbymodus" ausgeführt werden, wie auf Element-für-Element-Basis angegeben.

</dd> <dt>

[**CIM \_ AdjacentSlots**](cim-adjacentslots.md)
</dt> <dd>

Die [**Zuordnung CIM \_ AdjacentSlots**](cim-adjacentslots.md) beschreibt das Layout von Slots auf einem Hostboard oder einer Adapterkarte. Informationen, z. B. der Abstand zwischen den Slots und ob sie "freigegeben" sind (wenn einer aufgefüllt wird, kann der andere Slot nicht verwendet werden), werden als Zuordnungseigenschaften übermittelt.

</dd> <dt>

[**\_CIM-AggregatPExtent**](cim-aggregatepextent.md)
</dt> <dd>

Die [**CIM \_ AggregatePExtent-Klasse**](cim-aggregatepextent.md) stellt zusammenfassende Informationen zu adressierbaren logischen Blöcken zur Verfügung, die sich in derselben Speicherredundanzgruppe befinden und sich auf demselben physischen Medium befinden.

</dd> <dt>

[**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md)
</dt> <dd>

Die [**CIM \_ AggregatePSExtent-Klasse**](cim-aggregatepsextent.md) definiert die Anzahl der adressierbaren logischen Blöcke auf einem einzelnen Speichergerät, mit Ausnahme logischer Blöcke, die als Prüfdaten zugeordnet sind. Wenn Volumesätze definiert sind, sind die logischen Blöcke in einem einzelnen Volumesatz enthalten. Dies ist eine alternative Gruppierung für [**CIM \_ ProtectedSpaceExtent,**](cim-protectedspaceextent.md)wenn nur Zusammenfassungsinformationen benötigt werden oder wenn die automatische Konfiguration verwendet wird.

</dd> <dt>

[**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md)
</dt> <dd>

Die [**CIM \_ AggregateRedundancyComponent-Klasse**](cim-aggregateredundancycomponent.md) beschreibt den aggregierten physischen Umfang in einer Speicherredundanzgruppe.

</dd> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> <dd>

Die [**CIM \_ AlarmDevice-Klasse**](cim-alarmdevice.md) ist ein Alarmgerät, das akustische oder sichtbare Hinweise im Zusammenhang mit einer Problemsituation aus gibt.

</dd> <dt>

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dd>

Die [**CIM \_ AllocatedResource-Klasse**](cim-allocatedresource.md) stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar und gibt an, dass die Ressource dem Gerät zugewiesen ist.

</dd> <dt>

[**CIM \_ ApplicationSystem**](cim-applicationsystem.md)
</dt> <dd>

Die [**CIM \_ ApplicationSystem-Klasse**](cim-applicationsystem.md) stellt eine Anwendung oder ein Softwaresystem dar, die eine bestimmte Geschäftsfunktion unterstützt, die als unabhängige Einheit verwaltet werden kann. Ein solches System kann mithilfe der [**CIM \_ SoftwareFeature-Klasse**](cim-softwarefeature.md) in seine funktionalen Komponenten zersetzt werden. Die Softwarefeatures für eine bestimmte Anwendung oder ein bestimmtes Softwaresystem werden mithilfe der [**CIM \_ ApplicationSystemSoftwareFeature-Zuordnung**](cim-applicationsystemsoftwarefeature.md) gespeichert.

</dd> <dt>

[**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

Die [**CIM \_ ApplicationSystemSoftwareFeature-Klasse**](cim-applicationsystemsoftwarefeature.md) stellt eine Zuordnung dar, die die Softwarefeatures identifiziert, aus denen ein bestimmtes Anwendungssystem bestehende ist. Die Softwarefeatures können in verschiedenen Produkten enthalten sein.

</dd> <dt>

[**CIM \_ AssociatedAlarm**](cim-associatedalarm.md)
</dt> <dd>

Die [**CIM \_ AssociatedAlarm-Abhängigkeit**](cim-associatedalarm.md) ordnet einem logischen Gerät einen Alarm zu.

</dd> <dt>

[**CIM \_ AssociatedBattery**](cim-associatedbattery.md)
</dt> <dd>

Die [**CIM \_ AssociatedBattery-Abhängigkeit**](cim-associatedbattery.md) ordnet einem logischen Gerät einen Akku zu. Verwenden Sie diese Zuordnung, um einzelne Akkus zu modellieren, die eine unterbrechungsfreie Stromversorgung (USV) machen.

</dd> <dt>

[**CIM \_ Associated CimIng**](cim-associatedcooling.md)
</dt> <dd>

Die [**Zuordnung CIM Associated Cooling \_ gibt**](cim-associatedcooling.md) an, wann Lüfter oder andere Kühlgeräte für ein Gerät spezifisch sind (im Gegensatz zur Bereitstellung von Gehäuse- oder Kühlschränken).

</dd> <dt>

[**CIM \_ AssociatedMemory**](cim-associatedmemory.md)
</dt> <dd>

Die [**CIM \_ AssociateMemory-Klasse**](cim-associatedmemory.md) ordnet installierten oder zugeordneten Arbeitsspeicher, z. B. Cachespeicher, einem logischen Gerät zu.

</dd> <dt>

[**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)
</dt> <dd>

Die [**CIM \_ AssociatedProcessorMemory-Klasse**](cim-associatedprocessormemory.md) ordnet den Prozessor- und Systemspeicher oder den Cache eines Prozessors zu.

</dd> <dt>

[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)
</dt> <dd>

Die [**CIM \_ AssociatedSensor-Klasse**](cim-associatedsensor.md) ordnet einem logischen Gerät einen installierten Sensor zu. Der Sensor misst kritische Eingabe- und Ausgabeeigenschaften und kann in das Gerät aufgenommen oder in der Nähe installiert werden.

</dd> <dt>

[**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

Die [**CIM \_ AssociatedSupplyCurrentSensor-Klasse**](cim-associatedsupplycurrentsensor.md) ordnet eine Stromversorgung einem aktuellen Sensor (Amperage) zu, der die Eingangsfrequenz überwacht.

</dd> <dt>

[**CIM \_ AssociatedSupplyVoltageSensor**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Ordnet einem Spannungssensor, der die Eingangsspannung überwacht, eine Stromversorgung zu.

</dd> <dt>

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> <dd>

Die [**CIM \_ BasedOn-Klasse**](cim-basedon.md) stellt eine Zuordnung dar, die beschreibt, wie Speicher extents aus Unterebenen-Extents zusammengestellt werden können. Physische Extents enthalten z. B. Geschützte Speicherplatz-Extents. Daher werden Volumesätze aus einem oder mehr physischen oder geschützten Speicherplatzbereich zusammengestellt. Cachespeicher kann unabhängig voneinander definiert und in einem physischen Element realisiert werden, oder er kann auf flüchtigen oder nicht flüchtigen Speichermodulen basieren.

</dd> <dt>

[**\_CIM-Akku**](cim-battery.md)
</dt> <dd>

Die [**CIM \_ Battery-Klasse**](cim-battery.md) stellt die Funktionen und die Verwaltung des logischen Akkugeräts dar. Diese Klasse gilt für Akkus in Laptopsystemen und anderen internen und externen Akkus.

</dd> <dt>

[**CIM \_ BinarySensor**](cim-binarysensor.md)
</dt> <dd>

Die [**CIM \_ BinarySensor-Klasse**](cim-binarysensor.md) bietet eine boolesche Ausgabe. Die **Eigenschaften CurrentState** und **PossibleStates** wurden für die Sensoring hinzugefügt, wodurch die **CIM \_ BinarySensor-Unterklasse** nicht mehr benötigt wird, obwohl sie aus Gründen der Abwärtskompatibilität beibehalten wird. Ein binärer Sensor kann erstellt werden, indem ein Sensor mit zwei möglichen Zuzuständen instanziiert wird.

</dd> <dt>

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dd>

Die [**CIM \_ BIOSElement-Klasse**](cim-bioselement.md) stellt die Low-Level-Software dar, die in nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computersystems verwendet wird.

</dd> <dt>

[**CIM \_ BIOSFeature**](cim-biosfeature.md)
</dt> <dd>

stellt die Funktionen der Low-Level-Software dar, die zum Starten und Konfigurieren eines Computersystems verwendet wird.

</dd> <dt>

[**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md)
</dt> <dd>

Die [**CIM \_ BIOSFeatureBIOSElements-Klasse**](cim-biosfeaturebioselements.md) ordnet ein BIOS-Feature und seine aggregierten BIOS-Elemente zu.

</dd> <dt>

[**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md)
</dt> <dd>

Die [**CIM \_ BIOSLoadedInNV-Klasse**](cim-biosloadedinnv.md) ordnet ein BIOS-Element und den nicht flüchtigen Speicher zu, in den es geladen wird.

</dd> <dt>

[**CIM \_ BootOSFromFS**](cim-bootosfromfs.md)
</dt> <dd>

Die [**CIM \_ BootOSFromFS-Klasse**](cim-bootosfromfs.md) ordnet das Betriebssystem und die Dateisysteme zu, aus denen das Betriebssystem geladen wird. Die Zuordnung ist n:n. Ein verteiltes Betriebssystem kann davon abhängen, dass mehrere Dateisysteme ordnungsgemäß und vollständig geladen werden.

</dd> <dt>

[**CIM \_ BootSAP**](cim-bootsap.md)
</dt> <dd>

Die [**CIM \_ BootSAP-Klasse**](cim-bootsap.md) stellt die Zugriffspunkte eines Startdiensts dar.

</dd> <dt>

[**CIM \_ BootService**](cim-bootservice.md)
</dt> <dd>

Die [**CIM \_ BootService-Klasse**](cim-bootservice.md) stellt die Funktionalität dar, die von einem Gerät, einer Software oder einem Netzwerk zum Laden eines Betriebssystems auf einem unitären Computersystem bereitgestellt wird.

</dd> <dt>

[**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md)
</dt> <dd>

Die [**CIM \_ BootServiceAccessBySAP-Klasse**](cim-bootserviceaccessbysap.md) ordnet einen Startdienst und seine Zugriffspunkte zu.

</dd> <dt>

[**CIM \_ CacheMemory**](cim-cachememory.md)
</dt> <dd>

Die [**CIM \_ CacheMemory-Klasse**](cim-cachememory.md) definiert die Funktionen und die Verwaltung des Cachespeichers.

</dd> <dt>

[**\_CIM-Karte**](cim-card.md)
</dt> <dd>

Die [**CIM \_ Card-Klasse**](cim-card.md) stellt einen physischen Containertyp dar, der an eine andere Karte oder ein Hostingboard angeschlossen werden kann oder selbst ein Hostingboard/eine Hauptplatine in einem Gehäuse ist. Diese Klasse enthält alle Pakete, die Signale tragen und einen Bereitstellungspunkt für physische Komponenten bereitstellen können, z. B. Chips oder andere physische Pakete, z. B. andere Karten.

</dd> <dt>

[**CIM \_ CardInSlot**](cim-cardinslot.md)
</dt> <dd>

Die [**CIM \_ CardInSlot-Klasse**](cim-cardinslot.md) ordnet dem Container, in den sie eingefügt wird, eine Adapterkarte zu.

</dd> <dt>

[**CIM \_ CardOnCard**](cim-cardoncard.md)
</dt> <dd>

Die [**CIM \_ CardOnCard-Zuordnung**](cim-cardoncard.md) beschreibt Beziehungen zu Karten, die in Hauptplatinen/Baseboards, Intokcards eines Adapters oder Karten, die spezielle kartenbasierte Module unterstützen, angeschlossen werden können.

</dd> <dt>

[**CIM \_ C CIMDrive**](cim-cdromdrive.md)
</dt> <dd>

Die [**CIM \_ C CIMDrive-Klasse**](cim-cdromdrive.md) stellt ein CD-ROM-Laufwerk auf dem Computer dar.

</dd> <dt>

[**\_CIM-Gehäuse**](cim-chassis.md)
</dt> <dd>

Die [**\_ CIM-Chassis-Klasse**](cim-chassis.md) stellt die physischen Elemente dar, die andere Elemente umschließen und definierbare Funktionen bereitstellen, z. B. desktop, verarbeitungsknoten, UPS, Datenträger- oder Bandspeicher oder eine Kombination dieser Elemente.

</dd> <dt>

[**CIM \_ ChassisInRack**](cim-chassisinrack.md)
</dt> <dd>

Die [**\_ CIM-ChassisInRack-Zuordnung**](cim-chassisinrack.md) stellt die "enthaltende" Beziehung zwischen einem Rack und einem darin enthaltenden Gehäuse dar.

</dd> <dt>

[**\_CIM-Überprüfung**](cim-check.md)
</dt> <dd>

Die [**CIM \_ Check-Klasse**](cim-check.md) stellt eine Bedingung oder ein Merkmal dar, die in einer Umgebung erfüllt sein soll, die von einer Instanz einer [**\_ CIM-ComputerSystem-Klasse**](cim-computersystem.md) definiert oder festgelegt wird. Die einem bestimmten Softwareelement zugeordneten Überprüfungen werden mithilfe der **Phase-Eigenschaft** der [**CIM \_ SoftwareElementChecks-Zuordnung**](cim-softwareelementchecks.md) in eine von zwei Gruppen organisiert.

</dd> <dt>

[**\_CIM-Chip**](cim-chip.md)
</dt> <dd>

Die [**\_ CIM-Chipklasse**](cim-chip.md) stellt den Typ der integrierten Leitungshardware dar, einschließlich ASICs, Prozessoren, Speicherchips usw.

</dd> <dt>

[**\_CIM-ClusteringSAP**](cim-clusteringsap.md)
</dt> <dd>

Die [**CIM \_ ClusteringSAP-Klasse**](cim-clusteringsap.md) stellt die Zugriffspunkte eines Clusteringdiensts dar.

</dd> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> <dd>

Die [**CIM \_ ClusteringService-Klasse**](cim-clusteringservice.md) stellt die von einem Cluster bereitgestellte Funktionalität dar. Beispielsweise kann die Failoverfunktion als Dienst eines Failoverclusters modelliert werden.

</dd> <dt>

[**\_CIM-ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

Die [**CIM \_ ClusterServiceAccessBySAP-Klasse**](cim-clusterserviceaccessbysap.md) stellt die Beziehung zwischen einem Clusteringdienst und seinen Zugriffspunkten dar.

</dd> <dt>

[**CIM \_ CollectedCollections**](cim-collectedcollections.md)
</dt> <dd>

Die [**CIM \_ CollectedCollections-Klasse**](cim-collectedcollections.md) ist eine Aggregationszuordnung, die eine Auflistung verwalteter Systemelemente (Managed System Elements, MSE) darstellt, die in einer Sammlung von MSEs enthalten sind.

</dd> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> <dd>

Die [**CIM \_ CollectedMSEs-Zuordnungsklasse**](cim-collectedmses.md) stellt die Member des Gruppierungsobjekts dar, eine [**CollectionOfMSEs-Klasse.**](cim-collectionofmses.md)

</dd> <dt>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> <dd>

Das [**CIM \_ CollectionOfMSEs-Objekt**](cim-collectionofmses.md) ermöglicht die Gruppierung von [**CIM \_ ManagedSystemElement-Objekten**](cim-managedsystemelement.md) zum Zuordnen von Einstellungen und Konfigurationen. Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.

</dd> <dt>

[**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md)
</dt> <dd>

Die [**CIM \_ CollectionOfSensors-Zuordnung**](cim-collectionofsensors.md) stellt die binären Sensoren dar, aus denen der Sensor mit mehreren States zusammenfällt.

</dd> <dt>

[**CIM \_ CollectionSetting**](cim-collectionsetting.md)
</dt> <dd>

Die [**CIM \_ CollectionSetting-Klasse**](cim-collectionsetting.md) stellt die Zuordnung zwischen einer [**CIM \_ CollectionOfMSEs-Klasse**](cim-collectionofmses.md) und der für sie definierten Einstellungsklasse dar.

</dd> <dt>

[**CIM \_ CompatibleProduct**](cim-compatibleproduct.md)
</dt> <dd>

Die [**CIM \_ CompatibleProduct-Klasse**](cim-compatibleproduct.md) stellt eine Zuordnung zwischen Produkten dar, die angibt, ob zwei Referenzprodukte interoperabel sind, z. B. ob sie zusammen installiert werden können oder ob eines der physischen Container für das andere sein kann usw.

</dd> <dt>

[**\_CIM-Komponente**](cim-component.md)
</dt> <dd>

Die [**\_ CIM-Komponentenzuordnung**](cim-component.md) stellt die Teile einer Beziehung zwischen MSEs dar.

</dd> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> <dd>

Eine [**CIM \_ ComputerSystem-Klasse**](cim-computersystem.md) stellt eine spezielle Sammlung von [**CIM \_ ManagedSystemElement-Instanzen**](cim-managedsystemelement.md) dar. Diese Sammlung bietet Computerfunktionen und dient als Aggregationspunkt, um eines oder mehrere der folgenden Elemente zuzuordnen: Dateisystem, Betriebssystem, Prozessor und Arbeitsspeicher (flüchtiger und nicht flüchtiger Speicher). Diese Klasse wird von [**CIM \_ System**](cim-system.md)abgeleitet.

</dd> <dt>

[**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md)
</dt> <dd>

Die [**CIM \_ ComputerSystemDMA-Klasse**](cim-computersystemdma.md) stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren DMA-Kanälen (Direct Memory Access) dar.

</dd> <dt>

[**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md)
</dt> <dd>

Die [**CIM \_ ComputerSystemIRQ-Klasse**](cim-computersystemirq.md) stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Interruptanforderungszeilen (IRQs) dar.

</dd> <dt>

[**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md)
</dt> <dd>

Die [**CIM \_ ComputerSystemMappedIO-Klasse**](cim-computersystemmappedio.md) stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren speicherzuordnungen E/A-Ports dar.

</dd> <dt>

[**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md)
</dt> <dd>

Die [**CIM \_ ComputerSystemPackage-Klasse**](cim-computersystempackage.md) stellt eine Zuordnung dar, die explizit die Beziehung zwischen unitären Computersystemen und einem oder mehreren physischen Paketen definiert. Die Zuordnung ähnelt der Art und Weise, wie logische Geräte durch physische Elemente realisiert werden.

</dd> <dt>

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> <dd>

Die [**CIM \_ ComputerSystemResource-Klasse**](cim-computersystemresource.md) stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Systemressourcen dar.

</dd> <dt>

[**\_CIM-Konfiguration**](cim-configuration.md)
</dt> <dd>

Das [**\_ CIM-Konfigurationsobjekt**](cim-configuration.md) ermöglicht die Gruppierung von Parametersätzen (definiert in [**CIM \_ Setting-Objekten)**](cim-setting.md) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente.

</dd> <dt>

[**CIM \_ ConnectedTo**](cim-connectedto.md)
</dt> <dd>

Die [**\_ CIM ConnectedTo-Klasse**](cim-connectedto.md) stellt eine Zuordnung dar, die angibt, dass zwei oder mehr physische Connectors verbunden sind.

</dd> <dt>

[**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md)
</dt> <dd>

Die [**CIM \_ ConnectorOnPackage-Klasse**](cim-connectoronpackage.md) stellt eine Zuordnung dar, die die Einschlussbeziehung zwischen Connectors und Paketen explizit macht. Physische Pakete enthalten Connectors sowie andere physische Elemente.

</dd> <dt>

[**\_CIM-Container**](cim-container.md)
</dt> <dd>

Die [**CIM \_ Container-Klasse**](cim-container.md) stellt eine Zuordnung zwischen einem enthaltenen und einem enthaltenden physischen Element dar. Ein enthaltenes -Objekt muss ein physisches Paket sein.

</dd> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dd>

Die [**CIM \_ ControlledBy-Beziehung**](cim-controlledby.md) gibt an, welche Geräte vom logischen Controllergerät gesteuert werden oder über das darauf zugegriffen wird.

</dd> <dt>

[**\_CIM-Controller**](cim-controller.md)
</dt> <dd>

Die [**CIM \_ Controller-Klasse**](cim-controller.md) ist eine übergeordnete Klasse zum Gruppieren verschiedener steuerelementbezogener Geräte. Beispiele für Controller sind SCSI-Controller, USB-Controller und serielle Controller.

</dd> <dt>

[**\_CIM-KühlungGeräte**](cim-coolingdevice.md)
</dt> <dd>

Die [**CIM \_ CoolingDevice-Klasse**](cim-coolingdevice.md) stellt die Funktionen und die Verwaltung von Kühlgeräten dar.

</dd> <dt>

[**CIM \_ CopyFileAction**](cim-copyfileaction.md)
</dt> <dd>

Die [**CIM \_ CopyFileAction-Klasse**](cim-copyfileaction.md) stellt das Verschieben oder Kopieren von Dateien von einem Computersystem an einen neuen Speicherort dar.

</dd> <dt>

[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)
</dt> <dd>

Die [**CIM \_ CreateDirectoryAction-Klasse**](cim-createdirectoryaction.md) erstellt leere Verzeichnisse für Softwareelemente, die lokal installiert werden sollen.

</dd> <dt>

[**CIM \_ CurrentSensor**](cim-currentsensor.md)
</dt> <dd>

Die [**CIM \_ CurrentSensor-Klasse**](cim-currentsensor.md) ist aus Gründen der Abwärtskompatibilität mit früheren CIM-Schemadefinitionen vorhanden.

</dd> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dd>

Die [**CIM \_ DataFile-Klasse**](cim-datafile.md) stellt eine benannte Auflistung von Daten oder ausführbarem Code dar. Es werden nur Instanzen von Dateien auf lokalen Festplatten zurückgegeben.

</dd> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> <dd>

Die [**\_ CIM-Abhängigkeitsklasse**](cim-dependency.md) stellt eine Zuordnung dar, die Abhängigkeitsbeziehungen zwischen Objekten herstellt.

</dd> <dt>

[**CIM \_ DependencyContext**](cim-dependencycontext.md)
</dt> <dd>

Die [**CIM \_ DependencyContext-Beziehung**](cim-dependencycontext.md) ordnet eine [**\_ CIM-Abhängigkeitsklasse**](cim-dependency.md) einem oder [**mehreren \_ CIM-Konfigurationsobjekten**](cim-configuration.md) zu. Beispielsweise können sich die Abhängigkeiten eines Computersystems basierend auf dem Netzwerk ändern, an das das System angefügt ist.

</dd> <dt>

[**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)
</dt> <dd>

Die [**CIM \_ DesktopMonitor-Klasse**](cim-desktopmonitor.md) stellt die Funktionen und die Verwaltung des logischen Desktopmonitorgeräts (CRT) dar.

</dd> <dt>

[**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md)
</dt> <dd>

Die [**CIM \_ DeviceAccessedByFile-Zuordnungsklasse**](cim-deviceaccessedbyfile.md) gibt das logische Gerät an, auf das mit der [**CIM \_ DeviceFile-Klasse**](cim-devicefile.md) zugegriffen wird, auf die verwiesen wird.

</dd> <dt>

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)
</dt> <dd>

Die [**CIM \_ DeviceConnection-Zuordnungsklasse**](cim-deviceconnection.md) stellt zwei oder mehr verbundene Geräte dar.

</dd> <dt>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)
</dt> <dd>

Die [**CIM \_ DeviceErrorCounts-Klasse**](cim-deviceerrorcounts.md) ist eine statistische Klasse, die fehlerbezogene Leistungsindikatoren für ein logisches Gerät enthält. Die Fehlertypen werden durch CCITT (Rec X.733) und ISO (IEC 10164-4) definiert.

</dd> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> <dd>

Die [**CIM \_ DeviceFile-Klasse**](cim-devicefile.md) stellt einen Typ logischer Datei dar, der ein Gerät darstellt. Diese Konvention ist für Betriebssysteme nützlich, die Geräte mit einem Bytestream-E/A-Modell verwalten. Das logische Gerät, das dieser Datei zugeordnet ist, wird mithilfe der [**CIM \_ DeviceAccessedByFile-Beziehung**](cim-deviceaccessedbyfile.md) angegeben.

</dd> <dt>

[**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dd>

Die [**CIM \_ DeviceSAPImplementation-Klasse**](cim-devicesapimplementation.md) stellt eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung dar. Wenn viele logische Geräte einem SAP zugeordnet sind, arbeiten die Elemente zusammen, um den Zugriffspunkt bereitzustellen. Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des SAP-Objekts.

</dd> <dt>

[**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md)
</dt> <dd>

Die [**CIM \_ DeviceServiceImplementation-Klasse**](cim-deviceserviceimplementation.md) stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung dar. Wenn mehrere Geräte einem Dienst zugeordnet sind, werden die Elemente zusammen ausgeführt, um den Dienst bereitzustellen. Wenn unterschiedliche Implementierungen eines Diensts vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des Dienstobjekts.

</dd> <dt>

[**CIM \_ DeviceSoftware**](cim-devicesoftware.md)
</dt> <dd>

Die [**Cim \_ DeviceSoftware-Beziehung**](cim-devicesoftware.md) identifiziert Software, die einem Gerät zugeordnet ist, z. B. Treiber, Konfigurations- oder Anwendungssoftware oder Firmware.

</dd> <dt>

[**\_CIM-Verzeichnis**](cim-directory.md)
</dt> <dd>

Die [**CIM \_ Directory-Klasse**](cim-directory.md) stellt einen Dateityp dar, der die darin enthaltenen Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt.

</dd> <dt>

[**CIM \_ DirectoryAction**](cim-directoryaction.md)
</dt> <dd>

Die abstrakte [**\_ CIM DirectoryAction-Klasse**](cim-directoryaction.md) verwaltet Verzeichnisse. Die Verzeichniserstellung wird von der [**CIM \_ CreateDirectoryAction-Klasse**](cim-createdirectoryaction.md) und das Entfernen des Verzeichnisses von der [**CIM \_ RemoveDirectoryAction-Klasse**](cim-removedirectoryaction.md) durchgeführt.

</dd> <dt>

[**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md)
</dt> <dd>

Die [**CIM \_ DirectoryContainsFile-Klasse**](cim-directorycontainsfile.md) stellt eine Zuordnung zwischen einem Verzeichnis und dateien dar, die in diesem Verzeichnis enthalten sind.

</dd> <dt>

[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)
</dt> <dd>

Die [**CIM \_ DirectorySpecification-Klasse**](cim-directoryspecification.md) erfasst die Hauptverzeichnisstruktur eines Softwareelements. Diese Klasse wird verwendet, um die Dateien eines Softwareelements in verwaltbare Einheiten zu organisieren, die auf einem Computersystem verschoben werden können.

</dd> <dt>

[**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md)
</dt> <dd>

Die [**CIM \_ DirectorySpecificationFile-Zuordnung**](cim-directoryspecificationfile.md) stellt das Verzeichnis dar, das die durch Verweisen auf die [**CIM \_ DirectorySpecification-Klasse**](cim-directoryspecification.md) angegebene Datei enthält.

</dd> <dt>

[**CIM \_ DiscreteSensor**](cim-discretesensor.md)
</dt> <dd>

Die [**CIM \_ DiscreteSensor-Klasse**](cim-discretesensor.md) verfügt über einen Satz von rechtlichen Zeichenfolgenwerten, die sie melden kann. Die Werte werden in der **PossibleValues-Eigenschaft** des Sensors aufzählt. Ein diskreter Sensor verfügt immer über einen aktuellen Messwert, der einem der aufzählten Werte entspricht.

</dd> <dt>

[**CIM \_ DiskDrive**](cim-diskdrive.md)
</dt> <dd>

Die [**CIM \_ DiskDrive-Klasse**](cim-diskdrive.md) stellt ein physisches Laufwerk dar, das vom Betriebssystem aus gesehen wird. Die Datenträgerfeatures entsprechen den logischen und Verwaltungsmerkmalen des Laufwerks und spiegeln in einigen Fällen möglicherweise nicht die physischen Merkmale des Geräts wider. Eine Schnittstelle zu einem physischen Laufwerk ist ein Member dieser Klasse. Ein Objekt, das auf einem anderen logischen Gerät basiert, ist jedoch kein Member dieser Klasse.

</dd> <dt>

[**CIM \_ DisketteDrive**](cim-diskettedrive.md)
</dt> <dd>

Die [**CIM \_ DisketteDrive-Klasse**](cim-diskettedrive.md) stellt die Funktionen und die Verwaltung eines Diskettenlaufwerks dar.

</dd> <dt>

[**CIM \_ DiskPartition**](cim-diskpartition.md)
</dt> <dd>

Die [**CIM \_ DiskPartition-Klasse**](cim-diskpartition.md) stellt einen zusammenhängenden Bereich logischer Blöcke dar, der vom Betriebssystem anhand der Felder typ und subtype der Partition identifiziert werden kann. Datenträgerpartitionen sollten direkt durch physische Medien (angegeben durch die [**CIM \_ RealizesDiskPartition-Zuordnung)**](cim-realizesdiskpartition.md) oder auf Speichervolumes erstellt werden.

</dd> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> <dd>

Die [**CIM \_ DiskSpaceCheck-Klasse**](cim-diskspacecheck.md) überprüft den verfügbaren Speicherplatz des Systems und gibt ihn in der **AvailableDiskSpace-Eigenschaft** an. Details werden mit dem Wert in der **AvailableSpace-Eigenschaft** des [**CIM \_ FileSystem-Objekts**](cim-filesystem.md) verglichen, das dem [**\_ CIM-ComputerSystem-Objekt**](cim-computersystem.md) zugeordnet ist, das die Systemumgebung beschreibt. Wenn der Wert der **AvailableSpace-Eigenschaft** größer oder gleich dem in der **AvailableDiskSpace-Eigenschaft** angegebenen Wert ist, wird die Bedingung erfüllt.

</dd> <dt>

[**\_CIM-Anzeige**](cim-display.md)
</dt> <dd>

Die [**CIM \_ Display-Klasse**](cim-display.md) ist eine übergeordnete Klasse zum Gruppieren verschiedener Anzeigegeräte.

</dd> <dt>

[**\_CIM-DMA**](cim-dma.md)
</dt> <dd>

Die [**\_ CIM-DMA-Klasse**](cim-dma.md) stellt den direkten Arbeitsspeicherzugriff (DMA) der Computerarchitektur dar.

</dd> <dt>

[**CIM \_ andockt**](cim-docked.md)
</dt> <dd>

Die [**\_ ANGED-Zuordnung**](cim-docked.md) stellt die Beziehung zwischen zwei Gehäusen dar. Beispielsweise kann ein Laptop (ein Gehäusetyp) an eine Andockstation (eine andere Art von Gehäuse) angedockt werden. Diese typische Beziehung wird explizit beschrieben.

</dd> <dt>

[**\_CIM-ElementCapacity**](cim-elementcapacity.md)
</dt> <dd>

Die [**\_ CIM-ElementCapacity-Klasse**](cim-elementcapacity.md) ordnet ein [**CIM \_ PhysicalCapacity-Objekt**](cim-physicalcapacity.md) einem oder mehrere physischen Elementen zu. Sie ordnet den beschriebenen physischen Elementen eine Beschreibung der minimalen und maximalen Hardwareanforderungen (oder Funktionen) zu.

</dd> <dt>

[**\_CIM-ElementKonfiguration**](cim-elementconfiguration.md)
</dt> <dd>

Die [**\_ CIM-ElementConfiguration-Zuordnung**](cim-elementconfiguration.md) bezieht ein [**\_ CIM-Konfigurationsobjekt**](cim-configuration.md) auf ein oder mehrere verwaltete Systemelemente. Das **\_ CIM-Konfigurationsobjekt** stellt ein bestimmtes Verhalten oder einen gewünschten Funktionszustand für das zugeordnete [**CIM \_ ManagedSystemElement dar.**](cim-managedsystemelement.md)

</dd> <dt>

[**\_CIM-ElementSetting**](cim-elementsetting.md)
</dt> <dd>

Die [**\_ CIM-ElementSetting-Klasse**](cim-elementsetting.md) stellt die Zuordnung zwischen verwalteten Systemelementen und der für sie definierten Einstellungsklasse dar.

</dd> <dt>

[**\_CIM-ElementeVerknlinkt**](cim-elementslinked.md)
</dt> <dd>

Die [**ZUORDNUNG CIM \_ ElementsLinked**](cim-elementslinked.md) stellt physische Elemente dar, die über eine physische Verbindung miteinander verkabelt werden.

</dd> <dt>

[**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md)
</dt> <dd>

Die [**\_ CIM-Klasse ErrorCountersForDevice**](cim-errorcountersfordevice.md) ordnet die [**CIM \_ DeviceErrorCounts-Klasse**](cim-deviceerrorcounts.md) dem logischen Gerät zu, auf das sie angewendet wird.

</dd> <dt>

[**CIM \_ ExecuteProgram**](cim-executeprogram.md)
</dt> <dd>

Die [**CIM \_ ExecuteProgram-Klasse**](cim-executeprogram.md) stellt Dateien dar, die auf dem System ausgeführt werden können, auf dem das Softwareelement installiert ist.

</dd> <dt>

[**\_CIM-Export**](cim-export.md)
</dt> <dd>

Die [**CIM \_ Export-Klasse**](cim-export.md) stellt eine Zuordnung zwischen einem lokalen Dateisystem und seinen Verzeichnissen dar, die angeben, dass die angegebenen Verzeichnisse für die Bereitstellung verfügbar sind. Beim Exportieren eines gesamten Dateisystems sollte das Verzeichnis auf das oberste Verzeichnis des Dateisystems verweisen.

</dd> <dt>

[**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md)
</dt> <dd>

Die [**CIM \_ ExtraCapacityGroup-Klasse**](cim-extracapacitygroup.md) wird von einer Redundanzgruppe abgeleitet, die angibt, dass die aggregierten Elemente über mehr Kapazität oder Funktionalität verfügen, als erforderlich ist. Ein Beispiel für diese Art von Redundanz ist die Installation von N+1-Netzteilen oder Lüftern in einem System.

</dd> <dt>

[**\_CIM-Lüfter**](cim-fan.md)
</dt> <dd>

Die [**\_ CIM-Lüfterklasse**](cim-fan.md) stellt die Funktionen und die Verwaltung eines Lüfter-Kühlgeräts dar.

</dd> <dt>

[**CIM \_ FileAction**](cim-fileaction.md)
</dt> <dd>

Mit [**der CIM \_ FileAction-Klasse**](cim-fileaction.md) kann der Autor Dateien suchen, die bereits auf dem Computer eines Benutzers vorhanden sind, und diese Dateien dann an einen neuen Speicherort verschieben oder kopieren.

</dd> <dt>

[**\_CIM-DateiSpezifizierung**](cim-filespecification.md)
</dt> <dd>

Die [**CIM \_ FileSpecification-Klasse**](cim-filespecification.md) stellt eine Datei dar, die sich entweder ein- oder aus dem System befindet. Die Datei befindet sich in dem Verzeichnis, das durch die [**CIM \_ DirectorySpecificationFile-Zuordnung identifiziert**](cim-directoryspecificationfile.md) wird. Die [**Invoke-Methode**](invoke-method-in-class-cim-filespecification.md) verwendet die Informationen, um das Vorhandensein der Datei zu überprüfen. Beachten Sie, dass Eigenschaften mit **einem NULL-Wert** nicht überprüft werden.

</dd> <dt>

[**CIM \_ FileStorage**](cim-filestorage.md)
</dt> <dd>

Die [**CIM \_ FileStorage-Zuordnung**](cim-filestorage.md) verknüpft das Dateisystem und die logischen Dateien, die über das Dateisystem adressiert werden.

</dd> <dt>

[**CIM \_ FileSystem**](cim-filesystem.md)
</dt> <dd>

Die [**CIM \_ FileSystem-Klasse**](cim-filesystem.md) stellt eine Datei oder ein DataSet dar, die lokal auf einem Computersystem oder remote von einem Dateiserver bereitgestellt wird.

</dd> <dt>

[**CIM \_ FlatPanel**](cim-flatpanel.md)
</dt> <dd>

Die [**CIM \_ FlatPanel-Klasse**](cim-flatpanel.md) stellt die Funktionen und die Verwaltung des logischen Flatpanelgeräts dar.

</dd> <dt>

[**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md)
</dt> <dd>

Die [**ZUORDNUNG CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifiziert das Quellverzeichnis für die Dateiaktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis durch eine vorherige Aktion erstellt wurde. Diese Zuordnung kann nicht mit einer [**CIM \_ FromDirectorySpecification-Zuordnung**](cim-fromdirectoryspecification.md) vorhanden sein. Eine Dateiaktion kann nur ein einzelnes Quellverzeichnis umfassen.

</dd> <dt>

[**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md)
</dt> <dd>

Die [**ZUORDNUNG CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifiziert das Quellverzeichnis für die Dateiaktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis bereits vorhanden ist. Diese Zuordnung kann nicht mit einer [**CIM \_ FromDirectoryAction-Zuordnung**](cim-fromdirectoryaction.md) vorhanden sein. Eine Dateiaktion kann nur ein einzelnes Quellverzeichnis umfassen.

</dd> <dt>

[**CIM \_ FRU**](cim-fru.md)
</dt> <dd>

Die [**CIM \_ FRU-Klasse**](cim-fru.md) stellt eine vom Hersteller definierte Sammlung von Produkten und physischen Elementen dar, die einer FRU (Field Replaceable Unit) zugeordnet sind, um ein Produkt am Kundenstandort zu unterstützen, zu warten oder zu aktualisieren.

</dd> <dt>

[**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md)
</dt> <dd>

Die [**CIM \_ FRUIncludesProduct-Klasse**](cim-fruincludesproduct.md) gibt an, dass eine FRU (Field Replaceable Unit) aus anderen Produkten bestehen kann.

</dd> <dt>

[**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md)
</dt> <dd>

Die [**CIM \_ FRUPhysicalElements-Klasse**](cim-fruphysicalelements.md) stellt die physischen Elemente dar, aus denen eine fru-Einheit (Field Replaceable Unit) erstellt wird.

</dd> <dt>

[**CIM \_ HeatPipe**](cim-heatpipe.md)
</dt> <dd>

Die [**CIM \_ HeatPipe-Klasse**](cim-heatpipe.md) stellt die Funktionen und die Verwaltung eines Wärmeleitungs-Kühlgeräts dar.

</dd> <dt>

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)
</dt> <dd>

Die [**CIM \_ HostedAccessPoint-Klasse**](cim-hostedaccesspoint.md) stellt eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und dem System dar, auf dem er bereitgestellt wird. Jedes System kann viele SAPs hosten.

</dd> <dt>

[**CIM \_ HostedBootSAP**](cim-hostedbootsap.md)
</dt> <dd>

Die [**CIM \_ HostedBootSAP-Klasse**](cim-hostedbootsap.md) definiert das hostend unitäre Computersystem für eine [**CIM \_ BootSAP-Klasse.**](cim-bootsap.md) Da diese Beziehung von [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)untergliedert ist, erbt sie das bereichs-/benennungsschema, das für [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)definiert ist, wobei ein Zugriffspunkt auf sein Hostingsystem zurückstellung. In diesem Fall muss **CIM \_ BootSAP** die Hostklasse [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) zurückführen.

</dd> <dt>

[**CIM \_ HostedBootService**](cim-hostedbootservice.md)
</dt> <dd>

Die [**CIM \_ HostedBootService-Klasse**](cim-hostedbootservice.md) ordnet ein Hostingsystem und einen Startdienst zu. Da diese Beziehung von [**CIM \_ HostedService**](cim-hostedservice.md)untergliedert ist, erbt sie das bereichs-/benennungsschema, das für den Dienst definiert ist, wobei ein Dienst auf sein Hostingsystem zurücktiert.

</dd> <dt>

[**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md)
</dt> <dd>

Die [**Cim \_ HostedFileSystem-Zuordnung**](cim-hostedfilesystem.md) stellt eine Verbindung zwischen dem Computersystem und dem Dateisystem dar, das auf dem Computersystem gehostet wird.

</dd> <dt>

[**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md)
</dt> <dd>

Die [**CIM \_ HostedJobDestination-Klasse**](cim-hostedjobdestination.md) stellt eine Zuordnung zwischen einem Auftragsziel und dem System dar, in dem es sich befindet. Ein System kann viele Auftragswarteschlangen hosten. Auftragsziele werden auf das Hostingsystem zurückstelle.

</dd> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dd>

Die [**CIM \_ HostedService-Klasse**](cim-hostedservice.md) stellt eine Zuordnung zwischen einem Dienst und dem System dar, in dem sich die Funktionalität befindet. Ein System kann viele Dienste hosten, die auf das Hostsystem zurückdringen. Das Modell stellt keine Dienste dar, die auf mehreren Systemen gehostet werden.

</dd> <dt>

[**\_CIM-Controller**](cim-infraredcontroller.md)
</dt> <dd>

Die [**\_ CIM-Klasse "ControllersController"**](cim-infraredcontroller.md) stellt die Funktionen und die Verwaltung eines Controller für Dieksteuerung dar.

</dd> <dt>

[**CIM \_ InstalledOS**](cim-installedos.md)
</dt> <dd>

Die [**CIM \_ InstalledOS-Zuordnungsklasse**](cim-installedos.md) stellt eine Verknüpfung zwischen dem Computersystem und dem installierten Betriebssystem dar. Ein Betriebssystem wird installiert, wenn es sich im Speicherbereich eines Computersystems befindet (z. B. auf ein Laufwerk kopiert oder in den Arbeitsspeicher heruntergeladen).

</dd> <dt>

[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)
</dt> <dd>

Die [**CIM \_ InstalledSoftwareElement-Klasse**](cim-installedsoftwareelement.md) ordnet ein Computersystem einem installierten Softwareelement zu.

</dd> <dt>

[**CIM \_ IRQ**](cim-irq.md)
</dt> <dd>

Die [**CIM \_ IRQ-Klasse**](cim-irq.md) stellt eine Intel Architecture Interrupt Request Line (IRQ) dar.

</dd> <dt>

[**\_CIM-Auftrag**](cim-job.md)
</dt> <dd>

Die [**\_ CIM-Auftragsklasse**](cim-job.md) stellt eine Arbeitseinheit für ein System dar, z. B. einen Druckauftrag. Ein Auftrag unterscheidet sich von einem Prozess, da ein Auftrag geplant werden kann.

</dd> <dt>

[**\_CIM-JobDestination**](cim-jobdestination.md)
</dt> <dd>

Die [**CIM \_ JobDestination-Klasse**](cim-jobdestination.md) stellt dar, wo ein Auftrag zur Verarbeitung übermittelt wird. Sie kann auf eine Warteschlange verweisen, die null oder mehr Aufträge enthält, z. B. eine Druckwarteschlange mit Druckaufträgen. Auftragsziele werden auf Systemen gehostet, ähnlich wie Dienste auf Systemen gehostet werden.

</dd> <dt>

[**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md)
</dt> <dd>

Die [**CIM \_ JobDestinationJobs-Zuordnung**](cim-jobdestinationjobs.md) beschreibt, wo ein Auftrag zur Verarbeitung übermittelt wird (d. h. an welches Auftragsziel).

</dd> <dt>

[**\_CIM-Tastatur**](cim-keyboard.md)
</dt> <dd>

Die [**\_ CIM-Tastaturklasse**](cim-keyboard.md) stellt die Funktionen und die Verwaltung des logischen Tastaturgeräts dar.

</dd> <dt>

[**CIM \_ LinkHasConnector**](cim-linkhasconnector.md)
</dt> <dd>

Die [**CIM \_ LinkHasConnector-Klasse**](cim-linkhasconnector.md) ordnet Kabel und Verbindungen zu, die als physische Connectors verwendet werden, die die physischen Elemente verbinden. Diese Zuordnung definiert explizit die Beziehung von Connectors für [**CIM \_ PhysicalLink**](cim-physicallink.md).

</dd> <dt>

[**CIM \_ LocalFileSystem**](cim-localfilesystem.md)
</dt> <dd>

Die [**CIM \_ LocalFileSystem-Klasse**](cim-localfilesystem.md) stellt den Dateispeicher dar, der von einem Computersystem auf lokale Weise gesteuert wird (z. B. direkter Gerätetreiberzugriff). Der Dateispeicher kann direkt vom Computersystem verwaltet werden, ohne dass ein anderer Computer als Dateiserver fungieren muss. Bei einem gruppierten Dateisystem ist das Dateisystem jedoch lokal und wird daher auf den Cluster übertragen.

</dd> <dt>

[**\_CIM-Speicherort**](cim-location.md)
</dt> <dd>

Die [**CIM \_ Location-Klasse**](cim-location.md) stellt die Position und Adresse eines physischen Elements dar.

</dd> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dd>

Die [**CIM \_ LogicalDevice-Klasse**](cim-logicaldevice.md) stellt eine Hardwareentität dar, die in physischer Hardware realisiert werden kann oder nicht.

</dd> <dt>

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)
</dt> <dd>

Die [**CIM \_ LogicalDisk-Klasse**](cim-logicaldisk.md) stellt einen zusammenhängenden Bereich logischer Blöcke dar, der von einem Dateisystem über das **Feld DeviceID** (Schlüssel) des Datenträgers identifiziert werden kann. In einer Windows-Umgebung enthält das Feld **DeviceID** beispielsweise einen Laufwerkbuchstaben. in einer UNIX-Umgebung enthält sie den Zugriffspfad. und in einer NetWare-Umgebung enthält sie den Volumenamen.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

Die [**CIM \_ LogicalDiskBasedOnPartition-Klasse**](cim-logicaldiskbasedonpartition.md) ordnet einen logischen Datenträger der Datenträgerpartition zu, auf der er sich befindet.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

Die [**CIM \_ LogicalDiskBasedOnVolumeSet-Zuordnung**](cim-logicaldiskbasedonvolumeset.md) verknüpft logische Datenträger mit dem Volume, auf dem sie gefunden werden. Logische Datenträger können auf einem einzelnen Volume (z. B. durch einen Softwarevolume-Manager verfügbar gemacht) oder auf einer Datenträgerpartition basieren.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

Die [**CIM \_ LogicalElement-Klasse**](cim-logicalelement.md) ist die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten wie Profile, Prozesse oder Systemfunktionen in Form von logischen Geräten darstellen.

</dd> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dd>

Die [**CIM \_ LogicalFile-Klasse**](cim-logicalfile.md) stellt eine benannte Sammlung von Daten dar, bei der es sich um ausführbaren Code handeln kann, der sich in einem Dateisystem in einem Speicherumfang befindet.

</dd> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dd>

Die [**CIM \_ LogicalIdentity-Klasse**](cim-logicalidentity.md) ist eine abstrakte und generische Zuordnung, die angibt, dass zwei logische Elemente verschiedene Aspekte derselben zugrunde liegenden Entität darstellen.

</dd> <dt>

[**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md)
</dt> <dd>

Die [**CIM \_ MagnetoOpticalDrive-Klasse**](cim-magnetoopticaldrive.md) stellt die Funktionen und die Verwaltung eines magnetooptischen Laufwerks dar, einem Untertyp des Medienzugriffsgeräts.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

Die [**CIM \_ ManagedSystemElement-Klasse**](cim-managedsystemelement.md) ist die Basisklasse für die Systemelementhierarchie. Jede unterscheidbare Systemkomponente ist ein Kandidat für die Aufnahme in diese Klasse.

</dd> <dt>

[**CIM \_ ManagementController**](cim-managementcontroller.md)
</dt> <dd>

Die [**CIM \_ ManagementController-Klasse**](cim-managementcontroller.md) bezieht sich auf die Funktionen und die Verwaltung eines Verwaltungscontrollers.

</dd> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> <dd>

Die [**CIM \_ MediaAccessDevice-Klasse**](cim-mediaaccessdevice.md) stellt die Möglichkeit dar, auf ein oder mehrere Medien zuzugreifen und diese dann zum Speichern und Abrufen von Daten zu verwenden.

</dd> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dd>

Die [**CIM \_ MediaPresent-Zuordnung**](cim-mediapresent.md) beschreibt eine Beziehung, in der über ein Medienzugriffsgerät auf einen Speicherbereich zugegriffen werden muss.

</dd> <dt>

[**\_CIM-Arbeitsspeicher**](cim-memory.md)
</dt> <dd>

Die [**CIM \_ Memory-Klasse**](cim-memory.md) stellt die Funktionen und die Verwaltung speicherbezogener logischer Geräte dar.

</dd> <dt>

[**CIM \_ MemoryCapacity**](cim-memorycapacity.md)
</dt> <dd>

Die [**CIM \_ MemoryCapacity-Klasse**](cim-memorycapacity.md) stellt Arbeitsspeicher dar, der auf einem physischen Element installiert werden kann, sowie die minimalen und maximalen Konfigurationen. Informationen zum derzeit installierten Arbeitsspeicher und den Mindest- und Maximalanforderungen eines Elements befinden sich in Instanzen der [**CIM \_ PhysicalMemory-Klasse.**](cim-physicalmemory.md)

</dd> <dt>

[**CIM \_ MemoryCheck**](cim-memorycheck.md)
</dt> <dd>

Die [**CIM \_ MemoryCheck-Klasse**](cim-memorycheck.md) gibt eine Bedingung für die Mindestmenge an Arbeitsspeicher an, die auf einem System verfügbar sein muss.

</dd> <dt>

[**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)
</dt> <dd>

Die [**CIM \_ MemoryMappedIO-Klasse**](cim-memorymappedio.md) stellt speicher abgebildete E/A-Auslastungen der Computerarchitektur dar. Diese Klasse bezieht sich auf Speicher- und Port-E/A-Ressourcen.

</dd> <dt>

[**CIM \_ MemoryOnCard**](cim-memoryoncard.md)
</dt> <dd>

Die [**CIM \_ MemoryOnCard-Klasse**](cim-memoryoncard.md) ordnet physischen Speicher zu, der sich auf Hostboards, Adapterkarten usw. befindet. Diese Zuordnung definiert explizit die Beziehung zwischen Arbeitsspeicher und Karten.

</dd> <dt>

[**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md)
</dt> <dd>

Die [**CIM \_ MemoryWithMedia-Klasse**](cim-memorywithmedia.md) ordnet physischen Speicher einem physischen Medium und dessen Bänder zu. Der Arbeitsspeicher ermöglicht die Medienidentifikation und speichert benutzerspezifische Daten.

</dd> <dt>

[**CIM \_ ModifySettingAction**](cim-modifysettingaction.md)
</dt> <dd>

Die [**CIM \_ ModifySettingAction-Klasse**](cim-modifysettingaction.md) stellt die Informationen zum Ändern einer bestimmten Einstellungsdatei für einen bestimmten Eintrag mit einem bestimmten Wert dar.

</dd> <dt>

[**\_CIM-MonitorResolution**](cim-monitorresolution.md)
</dt> <dd>

Die [**CIM \_ MonitorResolution-Klasse**](cim-monitorresolution.md) stellt die Beziehung zwischen horizontalen und vertikalen Auflösungen sowie die Aktualisierungsrate und den Scanmodus für einen Desktopmonitor dar. Werte werden im Videocontrollerobjekt angegeben.

</dd> <dt>

[**CIM \_ MonitorSetting**](cim-monitorsetting.md)
</dt> <dd>

Die [**CIM \_ MonitorSetting-Klasse**](cim-monitorsetting.md) ordnet die Monitorauflösung dem Desktopmonitor zu, auf den sie angewendet wird.

</dd> <dt>

[**\_CIM-Bereitstellung**](cim-mount.md)
</dt> <dd>

Die [**CIM \_ Mount-Klasse**](cim-mount.md) stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.

</dd> <dt>

[**CIM \_ MultiStateSensor**](cim-multistatesensor.md)
</dt> <dd>

Die [**CIM \_ MultiStateSensor-Klasse**](cim-multistatesensor.md) stellt einen Satz binärer Sensoren mit mehreren Membern dar, wobei jeder binäre Sensor ein boolesches Ergebnis meldet.

</dd> <dt>

[**CIM \_ NetworkAdapter**](cim-networkadapter.md)
</dt> <dd>

Die [**CIM \_ NetworkAdapter-Klasse**](cim-networkadapter.md) ist eine abstrakte Klasse, die allgemeine Netzwerkhardwarekonzepte definiert (z. B. permanente Adresse oder Betriebsgeschwindigkeit). Die Informationen werden mithilfe der [**CIM \_ DeviceSAPImplementation-Zuordnung**](cim-devicesapimplementation.md) übermittelt.

</dd> <dt>

[**CIM \_ NFS**](cim-nfs.md)
</dt> <dd>

Die [**\_ CIM-NFS-Klasse**](cim-nfs.md) stellt ein Remotedateisystem dar, das mithilfe des NFS-Protokolls (Network File System) von einem Computersystem bereitgestellt wird.

</dd> <dt>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> <dd>

Die [**\_ CIM NonVolatileStorage-Klasse**](cim-nonvolatilestorage.md) stellt die Funktionen und die Verwaltung von nicht flüchtigem Speicher dar. Nicht flüchtiger Arbeitsspeicher umfasst nativ Flash- und ROM-Speicher.

</dd> <dt>

[**CIM \_ NumericSensor**](cim-numericsensor.md)
</dt> <dd>

Die [**CIM \_ NumericSensor-Klasse**](cim-numericsensor.md) stellt einen numerischen Sensor dar, der numerische Messwerte zurückgibt und optional Schwellenwerteinstellungen unterstützt.

</dd> <dt>

[**CIM \_ OperatingSystem**](cim-operatingsystem.md)
</dt> <dd>

Die [**CIM \_ OperatingSystem-Klasse**](cim-operatingsystem.md) stellt ein Computerbetriebssystem dar, das aus Software und Firmware besteht, die die Hardware eines Computersystems nutzbar machen.

</dd> <dt>

[**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

Die [**CIM \_ OperatingSystemSoftwareFeature-Klasse**](cim-operatingsystemsoftwarefeature.md) stellt die Softwarefeatures dar, die das Betriebssystem bilden.

</dd> <dt>

[**CIM \_ OSProcess**](cim-osprocess.md)
</dt> <dd>

Die [**CIM \_ OSProcess-Klasse**](cim-osprocess.md) ordnet das Betriebssystem und einen oder mehrere Prozesse zu, die im Kontext des Betriebssystems ausgeführt werden.

</dd> <dt>

[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)
</dt> <dd>

Die [**CIM \_ OSVersionCheck-Klasse**](cim-osversioncheck.md) gibt die Versionen des Betriebssystems an, die ein Softwareelement unterstützen können.

</dd> <dt>

[**CIM \_ PackageAlarm**](cim-packagealarm.md)
</dt> <dd>

Die [**CIM \_ PackageAlarm-Zuordnung**](/windows/desktop/SecCrypto/extendedproperties-newenum) stellt die Beziehung dar, in der ein Alarmgerät als Teil eines Pakets installiert wird. Die Installation weist auf Probleme mit der Umgebung des Pakets hin, d. h. mit dem Sicherheitsstatus oder der Gesamtzustand des Pakets.

</dd> <dt>

[**CIM \_ Package Auspacken**](cim-packagecooling.md)
</dt> <dd>

Die [**CIM \_ Package Rolling-Zuordnung**](cim-packagecooling.md) stellt die Beziehung dar, in der ein Kühlgerät in einem Paket installiert wird, z. B. einem Gehäuse oder Rack, um die Kühlung des Pakets zu unterstützen.

</dd> <dt>

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dd>

Die [**CIM \_ PackagedComponent-Zuordnung**](cim-packagedcomponent.md) stellt eine explizite Beziehung dar, in der eine Komponente in der Regel in einem physischen Paket enthalten ist, z. B. einem Gehäuse oder einer Karte.

</dd> <dt>

[**CIM \_ PackageInChassis**](cim-packageinchassis.md)
</dt> <dd>

Die [**CIM \_ PackageInChassis-Zuordnung**](cim-packageinchassis.md) stellt die Beziehung dar, in der ein Gehäuse andere Pakete enthalten kann, z. B. andere Gehäuse und Karten.

</dd> <dt>

[**CIM \_ PackageInSlot**](cim-packageinslot.md)
</dt> <dd>

Die [**CIM \_ PackageInSlot-Zuordnung**](cim-packageinslot.md) stellt die Beziehung zwischen Gerätekarten und dem Gehäuse dar, in dem sie eingebunden sind.

</dd> <dt>

[**CIM \_ PackageTempSensor**](cim-packagetempsensor.md)
</dt> <dd>

Die [**CIM \_ PackageTempSensor-Zuordnung**](cim-packagetempsensor.md) stellt die Beziehung dar, in der ein Temperatursensor häufig in einem Paket installiert wird, z. B. einem Gehäuse oder rack, um die Umgebung des Pakets zu überwachen.

</dd> <dt>

[**CIM \_ ParallelController**](cim-parallelcontroller.md)
</dt> <dd>

Die [**CIM \_ ParallelController-Zuordnung**](cim-parallelcontroller.md) bezieht sich auf die Funktionen und die Verwaltung des logischen Parallelportgeräts.

</dd> <dt>

[**CIM \_ ParticipatesInSet**](cim-participatesinset.md)
</dt> <dd>

Die [**CIM \_ ParticipatesInSet-Klasse**](cim-participatesinset.md) identifiziert physische Elemente, die zusammen ersetzt werden sollen.

</dd> <dt>

[**CIM \_ PCIController**](cim-pcicontroller.md)
</dt> <dd>

Die [**CIM \_ PCIController-Klasse**](cim-pcicontroller.md) stellt die Eigenschaften und die Verwaltung eines PCI-Controllers dar. Die Eigenschaften in dieser Klasse und ihre Unterklassen werden in den verschiedenen PCI-Spezifikationen definiert, die vom PCI SIG veröffentlicht werden.

</dd> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> <dd>

Die [**CIM \_ PCMCIAController-Klasse**](cim-pcmciacontroller.md) stellt die Funktionen und die Verwaltung eines PCMCIA-Controllers (Personal Computer Memory Card International Association) dar.

</dd> <dt>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> <dd>

Cim [**\_ PCVideoController**](cim-pcvideocontroller.md) stellt die Funktionen und die Verwaltung eines Pc-Videocontrollers dar, einem Untertyp eines Videocontrollers.

</dd> <dt>

[**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md)
</dt> <dd>

Die [**\_ CIM-Klasse PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) stellt die physischen Erweiterungen dar, die teil einer Speicherredundanzgruppe sind.

</dd> <dt>

[**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)
</dt> <dd>

Die [**CIM \_ PhysicalCapacity-Klasse**](cim-physicalcapacity.md) ist eine abstrakte Klasse, die die minimalen und maximalen Anforderungen eines physischen Elements und seine Fähigkeit zur Unterstützung verschiedener Hardwaretypen darstellt. Beispielsweise können minimale und maximale Arbeitsspeicheranforderungen als Unterklasse von **CIM \_ PhysicalCapacity** modelliert werden.

</dd> <dt>

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> <dd>

Die [**CIM \_ PhysicalComponent-Klasse**](cim-physicalcomponent.md) stellt eine Low-Level- oder Basic-Komponente innerhalb eines Pakets dar. Ein physisches Element, das kein Link, Connector oder Paket ist, ist ein Nachfolger (oder Member) dieser Klasse.

</dd> <dt>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> <dd>

Die [**CIM \_ PhysicalConnector-Klasse**](cim-physicalconnector.md) stellt jedes physische Element dar, das zum Herstellen einer Verbindung mit anderen Elementen verwendet wird. Jedes Objekt, das Signale oder Strom zwischen zwei oder mehr physischen Elementen verbinden und übertragen kann, ist ein Nachfolger (oder Member) dieser Klasse.

</dd> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> <dd>

Die [**CIM \_ PhysicalElement-Unterklassen**](cim-physicalelement.md) definieren jede Komponente eines Systems, die über eine eigene physische Identität verfügt. Instanzen dieser Klasse können als Bezeichnungen definiert werden, die physisch an das Objekt angefügt werden können.

</dd> <dt>

[**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md)
</dt> <dd>

Die [**CIM \_ PhysicalElementLocation-Klasse**](cim-physicalelementlocation.md) ordnet ein physisches Element zu Inventar- oder Ersetzungszwecken einem [**CIM \_ Location-Objekt**](cim-location.md) zu.

</dd> <dt>

[**CIM \_ PhysicalExtent**](cim-physicalextent.md)
</dt> <dd>

Die [**CIM \_ PhysicalExtent-Klasse**](cim-physicalextent.md) stellt eine SCC RAID-Implementierung dar. Sie definiert die aufeinander folgenden adressierbaren Blockadressen auf einem einzelnen Speichergerät, die als einzelner Speicherblock in derselben [**CIM \_ StorageRedundancyGroup-Klasse**](cim-storageredundancygroup.md) behandelt werden. Wenn die automatische Konfiguration verwendet wird, besteht eine Alternative darin, die [**CIM \_ AggregatePExtent-Klasse**](cim-aggregatepextent.md) zu instanziieren oder zu erweitern.

</dd> <dt>

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> <dd>

Die [**CIM \_ PhysicalFrame-Klasse**](cim-physicalframe.md) ist eine übergeordnete Klasse von Racks, Gehäusen und anderen Rahmengehäusen, da sie in Erweiterungsklassen definiert sind. Eigenschaften wie **VisibleAlarm** und **HörbleAlarm** sowie Daten im Zusammenhang mit Sicherheitsverletzungen sind in dieser übergeordneten Klasse enthalten.

</dd> <dt>

[**CIM \_ PhysicalLink**](cim-physicallink.md)
</dt> <dd>

Die [**CIM \_ PhysicalLink-Klasse**](cim-physicallink.md) stellt die Verkabelung physischer Elemente dar.

</dd> <dt>

[**CIM \_ PhysicalMedia**](cim-physicalmedia.md)
</dt> <dd>

Die [**CIM \_ PhysicalMedia-Klasse**](cim-physicalmedia.md) stellt Typen von Dokumentation und Speichermedien wie Bänder, CD ROMs usw. dar.

</dd> <dt>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dd>

Die [**\_ CIM PhysicalMemory-Klasse**](cim-physicalmemory.md) stellt Speichergeräte auf niedriger Ebene dar, z. B. SIMMS, DIMMs, Rohspeicherchips usw.

</dd> <dt>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)
</dt> <dd>

Die [**CIM \_ PhysicalPackage-Klasse**](cim-physicalpackage.md) stellt physische Elemente dar, die andere Komponenten enthalten oder hosten. Beispiele hierfür sind ein Rackgehäuse oder eine Adapterkarte.

</dd> <dt>

[**CIM \_ PointingDevice**](cim-pointingdevice.md)
</dt> <dd>

Die [**CIM \_ PointingDevice-Klasse**](cim-pointingdevice.md) stellt ein Gerät dar, das auf Bereiche auf dem Display zeigt. Jedes Gerät, das einen Zeiger bearbeitet oder auf Bereiche auf einer visuellen Anzeige zeigt, ist ein Member dieser Klasse. Beispielsweise eine Maus, ein Tablettstift, ein Touchpad oder ein Tablet.

</dd> <dt>

[**CIM \_ CIM CIMSModem**](cim-potsmodem.md)
</dt> <dd>

Die [**CIM \_ CIM CIMSModem-Klasse**](cim-potsmodem.md) stellt ein Gerät dar, das binäre Daten für die soundbasierte Übertragung in Wellenbandbreiten übersetzt, indem eine Verbindung mit dem PLAIN OLD Phone System-Netzwerk (CIMS) hergestellt wird.

</dd> <dt>

[**CIM \_ PowerSupply**](cim-powersupply.md)
</dt> <dd>

Die [**CIM \_ PowerSupply-Klasse**](cim-powersupply.md) stellt die Funktionen und die Verwaltung des logischen Stromversorgungsgeräts dar.

</dd> <dt>

[**\_CIM-Drucker**](cim-printer.md)
</dt> <dd>

Die [**CIM \_ Printer-Klasse**](cim-printer.md) stellt die Funktionen und die Verwaltung des logischen Druckergeräts dar.

</dd> <dt>

[**\_CIM-Prozess**](cim-process.md)
</dt> <dd>

Die [**CIM \_ Process-Klasse**](cim-process.md) stellt eine einzelne Instanz eines ausgeführten Programms dar. Ein Benutzer sieht einen Prozess in der Regel als Anwendung oder Aufgabe.

</dd> <dt>

[**CIM \_ ProcessExecutable**](cim-processexecutable.md)
</dt> <dd>

Die [**CIM \_ ProcessExecutable-Klasse**](cim-processexecutable.md) stellt eine Verknüpfung zwischen einem Prozess und einer Datendatei dar und gibt an, dass die Datei an der Ausführung des Prozesses beteiligt ist.

</dd> <dt>

[**\_CIM-Prozessor**](cim-processor.md)
</dt> <dd>

Die [**\_ CIM-Prozessorklasse**](cim-processor.md) stellt die Funktionen und die Verwaltung des logischen Prozessorgeräts dar.

</dd> <dt>

[**CIM \_ ProcessThread**](cim-processthread.md)
</dt> <dd>

Die [**CIM \_ ProcessThread-Klasse**](cim-processthread.md) stellt eine Verknüpfung zwischen einem Prozess und den Threads dar, die im Kontext des Prozesses ausgeführt werden.

</dd> <dt>

[**\_CIM-Produkt**](cim-product.md)
</dt> <dd>

Die [**\_ CIM-Produktklasse**](cim-product.md) ist eine konkrete Klasse, die eine Sammlung physischer Elemente, Softwarefeatures und anderer Produkte darstellt, die als Einheit erworben wurden. Der Erwerb impliziert eine Vereinbarung zwischen dem Lieferanten und dem Verbraucher, die Auswirkungen auf die Produktlizenzierung, den Support und die Garantie haben kann.

</dd> <dt>

[**CIM \_ ProductFRU**](cim-productfru.md)
</dt> <dd>

Die [**CIM \_ ProductFRU-Klasse**](cim-productfru.md) stellt eine Zuordnung zwischen dem Produkt und einer FRU (Field Replaceable Unit) dar, die Informationen zu Produktkomponenten bereitstellt, die ersetzt wurden oder ersetzt werden.

</dd> <dt>

[**CIM \_ ProductParentChild**](cim-productparentchild.md)
</dt> <dd>

Die [**\_ CIM-Zuordnung ProductParentChild**](cim-productparentchild.md) definiert eine Über-/Unterordnungshierarchie zwischen Produkten. Beispielsweise kann ein Produkt zusammen mit anderen Produkten enthalten sein.

</dd> <dt>

[**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md)
</dt> <dd>

Die [**\_ CIM-Klasse ProductPhysicalElements**](cim-productphysicalelements.md) stellt die physischen Elemente dar, aus denen sich ein Produkt zusammen setzt.

</dd> <dt>

[**CIM \_ ProductProductDependency**](cim-productproductdependency.md)
</dt> <dd>

Die [**CIM \_ ProductProductDependency-Klasse**](cim-productproductdependency.md) stellt eine Zuordnung zwischen zwei Produkten dar, die angibt, dass eines installiert werden muss oder nicht vorhanden sein muss, damit das andere funktioniert. Dies entspricht konzeptionell der [**CIM \_ ServiceServiceDependency-Zuordnung.**](cim-serviceservicedependency.md)

</dd> <dt>

[**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md)
</dt> <dd>

Die [**\_ CIM-Zuordnung ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifiziert die Softwarefeatures für ein bestimmtes Produkt.

</dd> <dt>

[**CIM \_ ProductSupport**](cim-productsupport.md)
</dt> <dd>

Die [**CIM \_ ProductSupport-Klasse**](cim-productsupport.md) stellt eine Zuordnung zwischen Produkt- und Supportzugriff dar, die vermittelt, wie Support für das Produkt erhalten wird. Für ein Produkt stehen verschiedene Arten von Support zur Verfügung. dasselbe Unterstützungsobjekt kann Unterstützung für mehrere Produkte bereitstellen.

</dd> <dt>

[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)
</dt> <dd>

Die [**CIM \_ ProtectedSpaceExtent-Klasse**](cim-protectedspaceextent.md) stellt adressierbare logische Blockadressen dar, die als einzelner Speicherbereich behandelt werden, sich aber in einem einzelnen physischen Block befinden.

</dd> <dt>

[**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md)
</dt> <dd>

Die [**CIM \_ PSExtentBasedOnPExtent-Klasse**](cim-psextentbasedonpextent.md) ordnet geschützte Speicherplatzerweiterungen zu, die auf einem physischen Extent basieren.

</dd> <dt>

[**\_CIM-Rack**](cim-rack.md)
</dt> <dd>

Die [**CIM \_ Rack-Klasse**](cim-rack.md) stellt ein Rack (einen physischen Rahmen oder ein Gehäuse) dar, in dem Gehäuse gespeichert werden. In der Regel stellt ein Rack das Gehäuse dar. alle funktionierenden Komponenten werden im Gehäuse verpackt.

</dd> <dt>

[**CIM \_ realisiert**](cim-realizes.md)
</dt> <dd>

Die [**CIM \_ Realizes-Klasse**](cim-realizes.md) stellt die Zuordnung dar, die die Zuordnung zwischen einem logischen Gerät und der physischen Komponente definiert, die das Gerät implementiert.

</dd> <dt>

[**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md)
</dt> <dd>

Die [**CIM \_ RealizesAggregatePExtent-Zuordnung**](cim-realizesaggregatepextent.md) stellt die Beziehung dar, in der die [**CIM \_ AggregatePExtent-Klasse**](cim-aggregatepextent.md) auf einem physischen Medium realisiert wird.

</dd> <dt>

[**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md)
</dt> <dd>

Die [**CIM \_ RealizesDiskPartition-Klasse**](cim-realizesdiskpartition.md) stellt eine Datenträgerpartition auf einem physischen Medium dar, die die Erstellung von Partitionen auf einem unformatierten SCSI- oder IDE-Laufwerk modelliert.

</dd> <dt>

[**CIM \_ RealizesPExtent**](cim-realizespextent.md)
</dt> <dd>

Die [**CIM \_ RealizesPExtent-Zuordnung**](cim-realizespextent.md) stellt die Beziehung dar, in der physische Erweiterungen auf einem physischen Medium realisiert werden. Darüber hinaus wird die Startadresse des physischen Extents auf dem physischen Medium angegeben.

</dd> <dt>

[**CIM \_ RebootAction**](cim-rebootaction.md)
</dt> <dd>

Die [**CIM \_ RebootAction-Klasse**](cim-rebootaction.md) verursacht einen Systemneustart, bei dem das Softwareelement installiert ist.

</dd> <dt>

[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)
</dt> <dd>

Die [**CIM \_ RedundancyComponent-Klasse**](cim-redundancycomponent.md) ordnet eine Redundanzgruppe zu, die aus verwalteten Systemelementen besteht, und gibt an, dass die Elemente zusammen Redundanz bereitstellen. Alle elemente, die in einer Redundanzgruppe aggregiert werden, sollten Instanziierungen derselben Objektklasse sein.

</dd> <dt>

[**CIM \_ RedundancyGroup**](cim-redundancygroup.md)
</dt> <dd>

Die [**CIM \_ RedundancyGroup-Klasse**](cim-redundancygroup.md) stellt eine Auflistung verwalteter Systemelemente dar, die angibt, dass die aggregierten Komponenten zusammen Redundanz bereitstellen. Alle elemente, die in einer Redundanzgruppe aggregiert werden, sollten Instanziierungen derselben Objektklasse sein.

</dd> <dt>

[**\_CIM-Kühlung**](cim-refrigeration.md)
</dt> <dd>

Die [**CIM \_ Refrigeration-Klasse**](cim-refrigeration.md) stellt die Funktionen und die Verwaltung eines Kühlgeräts dar.

</dd> <dt>

[**CIM \_ RelatedStatistics**](cim-relatedstatistics.md)
</dt> <dd>

Die [**CIM \_ RelatedStatistics-Zuordnung**](cim-relatedstatistics.md) stellt Hierarchien und Abhängigkeiten verwandter [**CIM \_ StatisticalInformation-Klassen**](cim-statisticalinformation.md) dar.

</dd> <dt>

[**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md)
</dt> <dd>

Die [**CIM \_ RemoteFileSystem-Klasse**](cim-remotefilesystem.md) stellt ein Remotedateisystem dar, auf das über einen netzwerkbezogenen Dienst zugegriffen wird. In diesem Fall wird der Dateispeicher von einem Computer gehostet, der als Dateiserver fungiert.

</dd> <dt>

[**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md)
</dt> <dd>

Die [**CIM \_ RemoveDirectoryAction-Klasse**](cim-removedirectoryaction.md) entfernt Verzeichnisse für Softwareelemente.

</dd> <dt>

[**CIM \_ RemoveFileAction**](cim-removefileaction.md)
</dt> <dd>

Die [**CIM \_ RemoveFileAction-Klasse**](cim-removefileaction.md) deinstalliert Dateien.

</dd> <dt>

[**CIM \_ ReplacementSet**](cim-replacementset.md)
</dt> <dd>

Die [**CIM \_ ReplacementSet-Klasse**](cim-replacementset.md) aggregiert physische Elemente, die zusammen ersetzt werden müssen. Wenn Sie beispielsweise eine Grafikkarte ersetzen, können die Komponentenspeicherchips auch entfernt und ersetzt werden. Alternativ kann diese Zuordnung verwendet werden, um einen Satz von Speicherchips zu ersetzen oder zu aktualisieren.

</dd> <dt>

[**CIM \_ ResidesOnExtent**](cim-residesonextent.md)
</dt> <dd>

Die [**CIM \_ ResidesOnExtent-Klasse**](cim-residesonextent.md) stellt eine Zuordnung zwischen einem Dateisystem und dem Speicherumfang dar, in dem es sich befindet. In der Regel befindet sich ein Dateisystem auf einem logischen Datenträger.

</dd> <dt>

[**CIM \_ RunningOS**](cim-runningos.md)
</dt> <dd>

Die [**CIM \_ RunningOS-Klasse**](cim-runningos.md) stellt das derzeit ausgeführte Betriebssystem dar. Höchstens ein Betriebssystem kann jederzeit auf einem Computersystem ausgeführt werden. Das Computersystem ist derzeit möglicherweise nicht gestartet, oder sein Betriebssystem ist unbekannt.

</dd> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> <dd>

Die [**CIM \_ SAPSAPDependency-Klasse**](cim-sapsapdependency.md) ist eine Zuordnung zwischen zwei Dienstzugriffspunkten (SAPs), die angibt, dass der zweite SAP erforderlich ist, damit der erste SAP eine Verbindung mit seinem Dienst herstellen kann.

</dd> <dt>

[**\_CIM-Scanner**](cim-scanner.md)
</dt> <dd>

Der [**\_ CIM-Scanner**](cim-scanner.md) stellt die Funktionen und die Verwaltung des logischen Scannergeräts dar.

</dd> <dt>

[**CIM \_ SCSIController**](cim-scsicontroller.md)
</dt> <dd>

Die [**CIM \_ SCSIController-Klasse**](cim-scsicontroller.md) stellt die Funktionen und die Verwaltung des logischen SCSI-Controllergeräts dar.

</dd> <dt>

[**CIM \_ SCSIInterface**](cim-scsiinterface.md)
</dt> <dd>

stellt eine [**CIM \_ ControlledBy-Beziehung**](cim-controlledby.md) dar, die angibt, auf welche Geräte über einen SCSI-Controller zugegriffen wird und welche Zugriffsmerkmale vorliegen.

</dd> <dt>

[**\_CIM-Sensor**](cim-sensor.md)
</dt> <dd>

Die [**CIM \_ Sensor-Klasse**](cim-sensor.md) stellt ein Hardwaregerät dar, das die Merkmale einer physischen Eigenschaft messen kann (z. B. die Temperatur- oder Spannungseigenschaften eines unitären Computersystems).

</dd> <dt>

[**CIM \_ SerialController**](cim-serialcontroller.md)
</dt> <dd>

Die [**CIM \_ SerialController-Klasse**](cim-serialcontroller.md) stellt die Funktionen und die Verwaltung des logischen Seriellen Anschlussgeräts dar.

</dd> <dt>

[**CIM \_ SerialInterface**](cim-serialinterface.md)
</dt> <dd>

Die [**CIM \_ SerialInterface-Klasse**](cim-serialinterface.md) stellt eine [**CIM \_ ControlledBy-Beziehung**](cim-controlledby.md) dar, die angibt, auf welche Geräte über den seriellen Controller zugegriffen wird, und die Eigenschaften des Zugriffs.

</dd> <dt>

[**\_CIM-Dienst**](cim-service.md)
</dt> <dd>

Die [**\_ CIM-Dienstklasse**](cim-service.md) stellt ein logisches Element dar, das Informationen zum Darstellen und Verwalten der Funktionalität enthält, die von einem Gerät oder softwarefeature bereitgestellt wird. Ein Dienst ist ein allgemeines Objekt zum Konfigurieren und Verwalten der Implementierung von Funktionen. es ist nicht die Funktionalität selbst.

</dd> <dt>

[**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md)
</dt> <dd>

Die [**CIM \_ ServiceAccessBySAP-Zuordnungsklasse**](cim-serviceaccessbysap.md) stellt die Zugriffspunkte für einen Dienst dar. Auf einen Drucker kann beispielsweise über NetWare, Macintosh oder Windows Service Access Points (SAPs) zugegriffen werden, die möglicherweise auf verschiedenen Systemen gehostet werden.

</dd> <dt>

[**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)
</dt> <dd>

Die [**CIM \_ ServiceAccessPoint-Klasse**](cim-serviceaccesspoint.md) stellt die Möglichkeit dar, einen Dienst zu verwenden oder aufzurufen. Zugriffspunkte stellen Dienste dar, die für die Verwendung durch andere Entitäten verfügbar sind.

</dd> <dt>

[**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md)
</dt> <dd>

Die [**CIM \_ ServiceSAPDependency-Klasse**](cim-servicesapdependency.md) stellt eine Zuordnung zwischen einem Dienst und einem Dienstzugriffspunkt (SAP) dar, die angibt, dass die referenzierte SAP vom Dienst verwendet wird, um seine Funktionalität bereitzustellen.

</dd> <dt>

[**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)
</dt> <dd>

Die [**CIM \_ ServiceServiceDependency-Klasse**](cim-serviceservicedependency.md) stellt eine Zuordnung zwischen zwei Diensten dar.

</dd> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dd>

Die [**CIM \_ Setting-Klasse**](cim-setting.md) stellt konfigurationsbezogene und betriebsbezogene Parameter für mindestens ein verwaltetes Systemelement dar.

</dd> <dt>

[**\_CIM-EinstellungÜberprüfung**](cim-settingcheck.md)
</dt> <dd>

Die [**CIM \_ SettingCheck-Klasse**](cim-settingcheck.md) gibt Informationen an, die erforderlich sind, um eine bestimmte Einstellungsdatei auf einen bestimmten Eintrag zu überprüfen, der einen Wert enthält, der dem angegebenen Wert entspricht. Bei allen Vergleichen wird davon ausgegangen, dass die Groß-/Kleinschreibung nicht beachtet wird.

</dd> <dt>

[**CIM \_ SettingContext**](cim-settingcontext.md)
</dt> <dd>

Die [**CIM \_ SettingContext-Klasse**](cim-settingcontext.md) ordnet Konfigurationsobjekte Einstellungsobjekten zu.

</dd> <dt>

[**\_CIM-Slot**](cim-slot.md)
</dt> <dd>

Die [**CIM \_ Slot-Klasse**](cim-slot.md) stellt Connectors dar, in die Pakete eingefügt werden.

</dd> <dt>

[**CIM \_ SlotInSlot**](cim-slotinslot.md)
</dt> <dd>

Die [**CIM \_ SlotInSlot-Beziehung**](cim-slotinslot.md) stellt die Fähigkeit eines speziellen Adapters dar, die vorhandene Slotstruktur zu erweitern, damit ansonsten inkompatible Karten in einen Frame oder ein Hostingboard integriert werden können.

</dd> <dt>

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> <dd>

Die [**CIM \_ SoftwareElement-Klasse**](cim-softwareelement.md) zerlegt ein [**CIM \_ SoftwareFeature-Objekt**](cim-softwarefeature.md) in eine Reihe von einzeln verwaltbaren oder bereitstellbaren Teilen für eine bestimmte Plattform. Die Plattform eines Softwareelements wird durch die zugrunde liegende Hardwarearchitektur und das Betriebssystem eindeutig identifiziert.

</dd> <dt>

[**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)
</dt> <dd>

Die [**CIM \_ SoftwareElementActions-Zuordnung**](cim-softwareelementactions.md) identifiziert die Aktionen für ein Softwareelement.

</dd> <dt>

[**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)
</dt> <dd>

Die [**CIM \_ SoftwareElementChecks-Zuordnungsklasse**](cim-softwareelementchecks.md) verknüpft ein Softwareelement mit Bedingungs- oder Standortinformationen, die ein Feature möglicherweise erfordert.

</dd> <dt>

[**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md)
</dt> <dd>

Die [**CIM \_ SoftwareElementVersionCheck-Klasse**](cim-softwareelementversioncheck.md) stellt einen Typ von Softwareelement dar, das in der Umgebung vorhanden sein muss.

</dd> <dt>

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)
</dt> <dd>

Die [**CIM \_ SoftwareFeature-Klasse**](cim-softwarefeature.md) stellt eine bestimmte Funktion oder Funktion eines Produkt- oder Anwendungssystems dar.

</dd> <dt>

[**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

Die [**CIM \_ SoftwareFeatureSAPImplementation-Klasse**](cim-softwarefeaturesapimplementation.md) stellt eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und ihrer Implementierung in Software dar.

</dd> <dt>

[**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

Die [**CIM \_ SoftwareFeatureServiceImplementation-Klasse**](cim-softwarefeatureserviceimplementation.md) stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung in Software dar.

</dd> <dt>

[**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

Die [**CIM \_ SoftwareFeatureSoftwareElements-Zuordnung**](cim-softwarefeaturesoftwareelements.md) identifiziert die Softwareelemente, die ein bestimmtes Softwarefeature bilden.

</dd> <dt>

[**CIM \_ SpareGroup**](cim-sparegroup.md)
</dt> <dd>

Die [**\_ CIM-SpareGroup-Klasse**](cim-sparegroup.md) wird von der [**CIM \_ RedundancyGroup-Klasse**](cim-redundancygroup.md) abgeleitet und gibt an, dass mindestens eines der aggregierten Elemente vermieden werden kann.

</dd> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dd>

Die [**CIM \_ StatisticalInformation-Klasse**](cim-statisticalinformation.md) ist eine Stammklasse für die beliebige Sammlung statistischer Daten oder Metriken, die auf ein oder mehrere verwaltete Systemelemente anwendbar sind.

</dd> <dt>

[**\_CIM-Statistiken**](cim-statistics.md)
</dt> <dd>

Die [**CIM \_ Statistics-Klasse**](cim-statistics.md) stellt eine Zuordnung dar, die verwaltete Systemelemente mit den statistischen Gruppen verknüpft, die für sie gelten.

</dd> <dt>

[**CIM \_ StorageDefect**](cim-storagedefect.md)
</dt> <dd>

Die [**CIM \_ StorageDefect-Aggregation**](cim-storagedefect.md) erfasst die Speicherfehler für einen Speicherumfang.

</dd> <dt>

[**CIM \_ StorageError**](cim-storageerror.md)
</dt> <dd>

Die [**CIM \_ StorageError-Klasse**](cim-storageerror.md) stellt Blöcke von Medien oder Arbeitsspeicher dar, die aufgrund von Fehlern nicht mehr verwendet werden können. Der Schlüssel der -Klasse ist die **StartingAddress-Eigenschaft** der fehlerhaften Bytes.

</dd> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> <dd>

Die [**CIM \_ StorageExtent-Klasse**](cim-storageextent.md) stellt die Funktionen und die Verwaltung der verschiedenen Medien dar, die vorhanden sind, um Daten zu speichern und den Datenabruf zu ermöglichen. Diese übergeordnete Klasse kann die verschiedenen Komponenten von RAID (Hardware oder Software) oder einen unformatierten logischen Umfang auf physischen Medien darstellen.

</dd> <dt>

[**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md)
</dt> <dd>

Die [**CIM \_ StorageRedundancyGroup-Klasse**](cim-storageredundancygroup.md) stellt Massenspeicherbezogene Redundanzinformationen dar.

</dd> <dt>

[**\_CIM-UnterstützungZugriff**](cim-supportaccess.md)
</dt> <dd>

Die [**CIM \_ SupportAccess-Klasse**](cim-supportaccess.md) definiert, wie Sie Unterstützung für ein Produkt erhalten.

</dd> <dt>

[**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md)
</dt> <dd>

Die [**CIM \_ SwapSpaceCheck-Klasse**](cim-swapspacecheck.md) gibt die Menge an Auslagerungsspeicherplatz an, der auf dem System verfügbar sein muss.

</dd> <dt>

[**\_CIM-System**](cim-system.md)
</dt> <dd>

Die [**\_ CIM-Systemklasse**](cim-system.md) aggregiert einen aufzählbaren Satz verwalteter Systemelemente. Die Aggregation fungiert als funktionales Ganzes. Innerhalb einer bestimmten Unterklasse des Systems gibt es eine klar definierte Liste verwalteter Systemelementklassen, deren Instanzen aggregiert werden müssen.

</dd> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dd>

eine cim-Zuordnungsklasse (Common Information Model), die Beziehungen zwischen einem System und den verwalteten Systemelementen herstellt, aus denen es besteht.

</dd> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dd>

Die [**\_ CIM-SystemGerätezuordnung**](cim-systemdevice.md) stellt eine explizite Beziehung dar, in der logische Geräte von einem System aggregiert werden können.

</dd> <dt>

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> <dd>

Die [**CIM \_ SystemResource-Klasse**](cim-systemresource.md) stellt eine Entität dar, die vom BIOS verwaltet wird, oder ein Betriebssystem, das für die Verwendung durch Software und logische Geräte verfügbar ist.

</dd> <dt>

[**\_CIM-Tachometer**](cim-tachometer.md)
</dt> <dd>

Die [**CIM \_ Tachometer-Klasse**](cim-tachometer.md) ist aus Gründen der Abwärtskompatibilität mit früheren CIM-Schemadefinitionen vorhanden.

</dd> <dt>

[**CIM \_ TapeDrive**](cim-tapedrive.md)
</dt> <dd>

Die [**CIM \_ TapeDrive-Klasse**](cim-tapedrive.md) stellt ein Bandlaufwerk auf dem System dar. Bandlaufwerke unterscheiden sich hauptsächlich darin, dass auf sie nur sequenziell zugegriffen werden kann.

</dd> <dt>

[**CIM \_ TemperatureSensor**](cim-temperaturesensor.md)
</dt> <dd>

Die [**CIM \_ TemperatureSensor-Klasse**](cim-temperaturesensor.md) ist aus Gründen der Abwärtskompatibilität mit früheren CIM-Schemadefinitionen vorhanden.

</dd> <dt>

[**\_CIM-Thread**](cim-thread.md)
</dt> <dd>

Die [**\_ CIM-Threadklasse**](cim-thread.md) stellt die Möglichkeit dar, Einheiten eines Prozesses oder Tasks parallel auszuführen. Ein Prozess kann viele Threads enthalten, von denen jeder für den Prozess schwach ist.

</dd> <dt>

[**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md)
</dt> <dd>

Die [**CIM \_ ToDirectoryAction-Zuordnung**](cim-todirectoryaction.md) identifiziert das Zielverzeichnis für die Dateiaktion.

</dd> <dt>

[**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md)
</dt> <dd>

Die [**\_ CIM-Zuordnung ToDirectorySpecification**](cim-todirectoryspecification.md) identifiziert das Zielverzeichnis für die Dateiaktion.

</dd> <dt>

[**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

Die [**CIM \_ UninterruptiblePowerSupply-Klasse**](cim-uninterruptiblepowersupply.md) stellt die Funktionen und die Verwaltung einer unterbrechungslosen Stromversorgung (USV) dar.

</dd> <dt>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dd>

Die [**CIM \_ UnitaryComputerSystem-Klasse**](cim-unitarycomputersystem.md) stellt einen Desktop, einen mobilen Computer, einen Netzwerkcomputer, einen Server oder einen anderen Computersystemtyp mit einem einzelnen Knoten dar.

</dd> <dt>

[**CIM \_ USBController**](cim-usbcontroller.md)
</dt> <dd>

Die [**CIM \_ USBController-Klasse**](cim-usbcontroller.md) stellt die Funktionen und die Verwaltung eines USB-Controllers dar.

</dd> <dt>

[**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md)
</dt> <dd>

Die [**CIM \_ USBControllerHasHub-Klasse**](cim-usbcontrollerhashub.md) definiert die Hubs, die dem USB-Controller nachgeschaltet sind.

</dd> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> <dd>

Die [**CIM \_ USBDevice-Klasse**](cim-usbdevice.md) stellt die Verwaltungsmerkmale eines USB-Geräts dar.

</dd> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> <dd>

Die [**CIM \_ USBHub-Klasse**](cim-usbhub.md) stellt die Funktionen und die Verwaltung eines USB-Hubs dar.

</dd> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> <dd>

Die [**CIM \_ UserDevice-Klasse**](cim-userdevice.md) ist eine übergeordnete Klasse, von der andere Klassen, z. B. [**\_ CIM-Tastatur**](cim-keyboard.md) oder [**CIM \_ DesktopMonitor,**](cim-desktopmonitor.md)absteigen. Benutzergeräte sind logische Geräte, die es dem Benutzer eines Computersystems ermöglichen, Daten einzugeben, anzuzeigen oder zu hören.

</dd> <dt>

[**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md)
</dt> <dd>

Die [**CIM \_ VersionCompatibilityCheck-Klasse**](cim-versioncompatibilitycheck.md) gibt an, ob es zulässig ist, den nächsten Zustand eines Softwareelements zu erstellen.

</dd> <dt>

[**CIM \_ VideoBIOSElement**](cim-videobioselement.md)
</dt> <dd>

Die [**CIM \_ VideoBIOSElement-Klasse**](cim-videobioselement.md) stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen wird und zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computersystems verwendet wird.

</dd> <dt>

[**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md)
</dt> <dd>

Die [**CIM \_ VideoBIOSFeature-Klasse**](cim-videobiosfeature.md) stellt die Funktionen der Low-Level-Software dar, die verwendet wird, um den Videocontroller und die Anzeige eines Computersystems zu konfigurieren und darauf zuzugreifen.

</dd> <dt>

[**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

Die [**CIM \_ VideoBIOSFeatureVideoBIOSElements-Klasse**](cim-videobiosfeaturevideobioselements.md) ordnet ein Video-BIOS-Feature und die zugehörigen aggregierten BioS-Videoelemente zu.

</dd> <dt>

[**CIM \_ VideoController**](cim-videocontroller.md)
</dt> <dd>

Die [**CIM \_ VideoController-Klasse**](cim-videocontroller.md) stellt die Funktionen und die Verwaltung des Videocontrollers dar.

</dd> <dt>

[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)
</dt> <dd>

Die [**CIM \_ VideoControllerResolution-Klasse**](cim-videocontrollerresolution.md) stellt die verschiedenen Videomodi dar, die ein Videocontroller unterstützen kann.

</dd> <dt>

[**CIM \_ VideoSetting**](cim-videosetting.md)
</dt> <dd>

Die [**CIM \_ VideoSetting-Klasse**](cim-videosetting.md) ordnet das [**CIM \_ VideoControllerResolution-Einstellungsobjekt**](cim-videocontrollerresolution.md) dem Controller zu, auf den es angewendet wird.

</dd> <dt>

[**CIM \_ VolatileStorage**](cim-volatilestorage.md)
</dt> <dd>

Die [**CIM \_ VolatileStorage-Klasse**](cim-volatilestorage.md) stellt die Funktionen und die Verwaltung von flüchtigem Speicher dar.

</dd> <dt>

[**CIM \_ VoltageSensor**](cim-voltagesensor.md)
</dt> <dd>

Die [**CIM \_ VoltageSensor-Klasse**](cim-voltagesensor.md) ist aus Gründen der Abwärtskompatibilität mit früheren CIM-Schemadefinitionen vorhanden. Mit Ergänzungen der Cim [**\_ Sensor-**](cim-sensor.md) und [**CIM \_ NumericSensor-Klassen**](cim-numericsensor.md) in Version 2.2 ist dies nicht mehr erforderlich.

</dd> <dt>

[**CIM \_ VolumeSet**](cim-volumeset.md)
</dt> <dd>

Die [**CIM \_ VolumeSet-Klasse**](cim-volumeset.md) stellt einen zusammenhängenden Bereich logischer Blöcke dar, die der Betriebsumgebung zum Lesen und Schreiben von Benutzerdaten angezeigt werden.

</dd> <dt>

[**CIM \_ WORMDrive**](cim-wormdrive.md)
</dt> <dd>

Die [**CIM \_ WORMDrive-Klasse**](cim-wormdrive.md) stellt die Funktionen und die Verwaltung eines WORM-Laufwerks dar, einem Untertyp des Medienzugriffsgeräts.

</dd> </dl>

 

 
