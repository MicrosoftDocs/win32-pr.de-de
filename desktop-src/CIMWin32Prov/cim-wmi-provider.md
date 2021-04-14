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
# <a name="cim-wmi-provider"></a>CIM-WMI-Anbieter

Diese WMI-Klassen werden in cimwin32. MOF deklariert.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**CIM- \_ Aktion**](cim-action.md)
</dt> <dd>

Eine [**CIM- \_ Aktions**](cim-action.md) Klasse ist ein Vorgang, der Teil eines Prozesses ist, um entweder ein Softwareelement im nächsten Zustand zu erstellen oder das Softwareelement im aktuellen Zustand zu entfernen.

</dd> <dt>

[**CIM- \_ Aktions Sequenz**](cim-actionsequence.md)
</dt> <dd>

Die CIM-Aktion " [**\_ aktionequenz**](cim-actionsequence.md) " definiert eine Reihe von Vorgängen, die das Softwareelement (auf das durch die [**CIM- \_ softwareelementactions**](cim-softwareelementactions.md) -Zuordnung verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.

</dd> <dt>

[**CIM- \_ acsiasspare**](cim-actsasspare.md)
</dt> <dd>

Die [**CIM- \_ aczasspare-Zuordnung**](cim-actsasspare.md) gibt an, welche Elemente Spares sein können oder andere aggregierte Elemente ersetzen. Ein Ersatz kann im Modus "Hot-Standby" ausgeführt werden, wie auf Element Weise angegeben.

</dd> <dt>

[**CIM- \_ annäheringslots**](cim-adjacentslots.md)
</dt> <dd>

Die [**CIM \_**](cim-adjacentslots.md) -Zuordnungs Slots-Zuordnung beschreibt das Layout von Slots auf einem hostboard oder einer Adapterkarte. Informationen, wie z. b. der Abstand zwischen den Slots und ob Sie "Shared" sind (wenn eine aufgefüllt wird, der andere Slot kann nicht verwendet werden), werden als Zuordnungs Eigenschaften übermittelt.

</dd> <dt>

[**CIM- \_ aggregatepblock**](cim-aggregatepextent.md)
</dt> <dd>

Die [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) -Klasse bietet zusammenfassende Informationen über adressierbare logische Blöcke, die sich in derselben Speicher Redundanz Gruppe befinden und sich auf demselben physischen Medium befinden.

</dd> <dt>

[**CIM \_ aggregatepsextent**](cim-aggregatepsextent.md)
</dt> <dd>

Die [**CIM- \_ aggregatepsextent**](cim-aggregatepsextent.md) -Klasse definiert die Anzahl der adressierbaren logischen Blöcke auf einem einzelnen Speichergerät, ausgenommen logische Blöcke, die als Prüfdaten zugeordnet sind. Wenn Volumesets definiert sind, sind die logischen Blöcke innerhalb eines einzelnen Volumesatzes enthalten. Dies ist eine alternative Gruppierung für [**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md), wenn nur Zusammenfassungs Informationen benötigt werden oder wenn die automatische Konfiguration verwendet wird.

</dd> <dt>

[**CIM \_ aggregateredundancycomponent**](cim-aggregateredundancycomponent.md)
</dt> <dd>

Die [**CIM- \_ aggregateredundancycomponent**](cim-aggregateredundancycomponent.md) -Klasse beschreibt den aggregierten physischen Block in einer Speicher Redundanz Gruppe.

</dd> <dt>

[**CIM- \_ alarmdevice**](cim-alarmdevice.md)
</dt> <dd>

Die [**CIM \_ alarmdevice**](cim-alarmdevice.md) -Klasse ist ein Alarmgerät, das akustische oder sichtbare Anzeichen für eine Problemsituation ausgibt.

</dd> <dt>

[**CIM- \_ Verteilungs Quelle**](cim-allocatedresource.md)
</dt> <dd>

Die CIM-Klasse " [**\_ Zuweisungs**](cim-allocatedresource.md) Klasse" stellt eine Zuordnung zwischen logischen Geräten und Systemressourcen dar und zeigt an, dass die Ressource dem Gerät zugewiesen ist.

</dd> <dt>

[**CIM- \_ applicationsystem**](cim-applicationsystem.md)
</dt> <dd>

Die [**CIM \_ applicationsystem**](cim-applicationsystem.md) -Klasse stellt ein Anwendungs-oder Softwaresystem dar, das eine bestimmte Geschäftsfunktion unterstützt, die als unabhängige Einheit verwaltet werden kann. Ein solches System kann mithilfe der [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Klasse in seine funktionalen Komponenten zerlegt werden. Die Software Features für eine bestimmte Anwendung oder ein bestimmtes Softwaresystem werden mithilfe der [**CIM \_ applicationsystemsoftwarefeature-Zuordnung**](cim-applicationsystemsoftwarefeature.md) gefunden.

</dd> <dt>

[**CIM \_ applicationsystemsoftwarefeature**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

Die [**CIM \_ applicationsystemsoftwarefeature**](cim-applicationsystemsoftwarefeature.md) -Klasse stellt eine Zuordnung dar, mit der die Software Features identifiziert werden, die ein bestimmtes Anwendungssystem bilden. Die Software Features können in verschiedene Produkte eingeschlossen werden.

</dd> <dt>

[**CIM \_ associatedalarm**](cim-associatedalarm.md)
</dt> <dd>

Die [**CIM \_ associatedalarm**](cim-associatedalarm.md) -Abhängigkeit ordnet einem logischen Gerät einen Alarm zu.

</dd> <dt>

[**CIM \_ associatedakku**](cim-associatedbattery.md)
</dt> <dd>

Die [**CIM \_ associatedakku**](cim-associatedbattery.md) -Abhängigkeit ordnet einen Akku einem logischen Gerät zu. Verwenden Sie diese Zuordnung, um einzelne Batterien zu modellieren, die eine unterbrechungsfreie Stromversorgung (USV) bilden.

</dd> <dt>

[**CIM \_ associatedcooling**](cim-associatedcooling.md)
</dt> <dd>

Die [**CIM \_ associatedcooling**](cim-associatedcooling.md) -Zuordnung gibt an, wann die Lüfter oder andere Kühlgeräte für ein Gerät spezifisch sind (im Gegensatz zur Bereitstellung von Gehäuse oder CAB-Kühlung).

</dd> <dt>

[**CIM \_ associatedmemory**](cim-associatedmemory.md)
</dt> <dd>

Die [**CIM \_ associatememory**](cim-associatedmemory.md) -Klasse ordnet installierten oder zugeordneten Arbeitsspeicher zu, z. b. Cache Speicher mit einem logischen Gerät.

</dd> <dt>

[**CIM \_ associatedprocessormemory**](cim-associatedprocessormemory.md)
</dt> <dd>

Die [**CIM \_ associatedprocessormemory**](cim-associatedprocessormemory.md) -Klasse ordnet den Prozessor-und Systemspeicher oder den Cache eines Prozessors zu.

</dd> <dt>

[**CIM \_ associatedsensor**](cim-associatedsensor.md)
</dt> <dd>

Die [**CIM \_ associatedsensor**](cim-associatedsensor.md) -Klasse ordnet einen installierten Sensor einem logischen Gerät zu. Der Sensor misst wichtige Eingabe-und Ausgabe Eigenschaften und kann im Gerät enthalten oder in der Nähe installiert werden.

</dd> <dt>

[**CIM \_ associatedsupplycurrentsensor**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

Die [**CIM \_ associatedsupplycurrentsensor**](cim-associatedsupplycurrentsensor.md) -Klasse ordnet eine Stromversorgung einem aktuellen (AMPERAGE) Sensor zu, der die Eingabe Häufigkeit überwacht.

</dd> <dt>

[**CIM \_ associatedsupplyvoltagesensor**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Verknüpft eine Stromversorgung mit einem Spannungssensor, der die Eingangsspannung überwacht.

</dd> <dt>

[**CIM- \_ BasedOn**](cim-basedon.md)
</dt> <dd>

Die [**CIM- \_ BasedOn**](cim-basedon.md) -Klasse stellt eine Zuordnung dar, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können. Physische Blöcke enthalten beispielsweise Blöcke mit geschütztem Speicherplatz. Volumesätze werden daher aus einem oder mehreren physischen oder geschützten Speicherplatz Blöcken zusammengestellt. Der Cache Speicher kann unabhängig voneinander definiert und in einem physischen Element realisiert werden. er kann aber auch auf flüchtigen oder nicht flüchtigen Speicherblöcken basieren.

</dd> <dt>

[**CIM- \_ Akku**](cim-battery.md)
</dt> <dd>

Die [**CIM- \_ Akku**](cim-battery.md) Klasse stellt die Funktionen und die Verwaltung des logischen Akku Geräts dar. Diese Klasse gilt für Akkus in Laptop Systemen und anderen internen und externen Akkus.

</dd> <dt>

[**CIM- \_ BinarySensor**](cim-binarysensor.md)
</dt> <dd>

Die [**CIM \_ BinarySensor**](cim-binarysensor.md) -Klasse stellt eine boolesche Ausgabe bereit. Die Eigenschaften " **CurrentState** " und " **possiblestates** " wurden für die sensorung hinzugefügt, sodass die **CIM- \_ BinarySensor** -Unterklasse nicht mehr benötigt wird, obwohl Sie aus Gründen der Abwärtskompatibilität beibehalten wird. Ein binärer Sensor kann erstellt werden, indem ein Sensor mit zwei möglichen Zuständen instanziiert wird.

</dd> <dt>

[**CIM- \_ bioselare**](cim-bioselement.md)
</dt> <dd>

Die [**CIM \_ bioselfigure**](cim-bioselement.md) -Klasse stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems verwendet wird.

</dd> <dt>

[**CIM- \_ biosfeature**](cim-biosfeature.md)
</dt> <dd>

stellt die Funktionen der Low-Level-Software dar, die zum Starten und Konfigurieren eines Computer Systems verwendet wird.

</dd> <dt>

[**CIM \_ biosfeaturebioselements**](cim-biosfeaturebioselements.md)
</dt> <dd>

Die [**CIM \_ biosfeaturebioselements**](cim-biosfeaturebioselements.md) -Klasse ordnet eine BIOS-Funktion und deren aggregierte BIOS-Elemente zu.

</dd> <dt>

[**CIM \_ biosloadedinnv**](cim-biosloadedinnv.md)
</dt> <dd>

Die [**CIM \_ biosloadedinnv**](cim-biosloadedinnv.md) -Klasse ordnet ein BIOS-Element und den nicht flüchtigen Speicher zu, in dem er geladen ist.

</dd> <dt>

[**CIM \_ bootosfromfs**](cim-bootosfromfs.md)
</dt> <dd>

Die [**CIM \_ bootosfromfs**](cim-bootosfromfs.md) -Klasse ordnet das Betriebssystem und die Dateisysteme zu, von denen das Betriebssystem geladen wurde. Die Zuordnung ist m:n-. ein verteiltes Betriebssystem kann davon abhängen, dass mehrere Dateisysteme ordnungsgemäß und vollständig geladen werden.

</dd> <dt>

[**CIM- \_ bootsap**](cim-bootsap.md)
</dt> <dd>

Die [**CIM- \_ bootsap**](cim-bootsap.md) -Klasse stellt die Zugriffspunkte eines Start Dienstanbieter dar.

</dd> <dt>

[**CIM- \_ Bootservice**](cim-bootservice.md)
</dt> <dd>

Die [**CIM- \_ Bootservice**](cim-bootservice.md) -Klasse stellt die Funktionalität dar, die von einem Gerät oder einer Software oder von einem Netzwerk bereitgestellt wird, um ein Betriebssystem auf einem einheitlichen Computersystem zu laden.

</dd> <dt>

[**CIM \_ bootserviceaccessbysap**](cim-bootserviceaccessbysap.md)
</dt> <dd>

Die [**CIM \_ bootserviceaccessbysap**](cim-bootserviceaccessbysap.md) -Klasse ordnet einen Start Dienst und seine Zugriffspunkte zu.

</dd> <dt>

[**CIM- \_ CacheMemory**](cim-cachememory.md)
</dt> <dd>

Die [**CIM \_ CacheMemory**](cim-cachememory.md) -Klasse definiert die Funktionen und die Verwaltung des Cache Speichers.

</dd> <dt>

[**CIM- \_ Karte**](cim-card.md)
</dt> <dd>

Die [**CIM- \_ Karten**](cim-card.md) Klasse stellt einen Typ von physischem Container dar, der an eine andere Karte oder ein hostingboard angeschlossen werden kann oder selbst ein hostingboard/-Motherboard in einem Chassis ist. Diese Klasse enthält alle Pakete, die Signale ausführen können und einen Bereitstellungs Punkt für physische Komponenten bereitstellen, wie z. b. Chips oder andere physische Pakete, wie z. b. andere Karten.

</dd> <dt>

[**CIM- \_ cardinslot**](cim-cardinslot.md)
</dt> <dd>

Die [**CIM \_ cardinslot**](cim-cardinslot.md) -Klasse ordnet eine Adapterkarte dem Container zu, in den Sie eingefügt wird.

</dd> <dt>

[**CIM- \_ kardoncard**](cim-cardoncard.md)
</dt> <dd>

Die [**CIM \_ cardoncard**](cim-cardoncard.md) -Zuordnung beschreibt die Beziehungen zu Karten, die an den über Ladungen/Baseboards, daughtercards eines Adapters oder Karten mit speziellen Karten ähnlichen Modulen angeschlossen werden können.

</dd> <dt>

[**CIM- \_ cdromdrive**](cim-cdromdrive.md)
</dt> <dd>

Die [**CIM- \_ cdromdrive**](cim-cdromdrive.md) -Klasse stellt ein CD-ROM-Laufwerk auf dem Computer dar.

</dd> <dt>

[**CIM- \_ Chassis**](cim-chassis.md)
</dt> <dd>

Die [**CIM- \_ Chassis**](cim-chassis.md) -Klasse stellt die physischen Elemente dar, die andere Elemente einschließen und definierbare Funktionen bereitstellen, wie z. b. einen Desktop, Verarbeitungs Knoten, UPS, Datenträger-oder Band Speicher oder eine Kombination dieser Elemente.

</dd> <dt>

[**CIM \_ chassisinrack**](cim-chassisinrack.md)
</dt> <dd>

Die [**CIM \_ chassisinrack**](cim-chassisinrack.md) -Zuordnung stellt die "enthaltende" Beziehung zwischen einem Gestell und einem darin enthaltenen Chassis dar.

</dd> <dt>

[**CIM- \_ Überprüfung**](cim-check.md)
</dt> <dd>

Die [**CIM- \_ Check**](cim-check.md) -Klasse stellt eine Bedingung oder ein Merkmal dar, die in einer Umgebung erwartungsgemäß definiert ist, die von einer Instanz einer [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse definiert oder festgelegt wird. Die Überprüfungen, die einem bestimmten Softwareelement zugeordnet sind, werden in einer von zwei Gruppen organisiert, wobei die **Phase** -Eigenschaft der [**CIM- \_ softwareelementchecks**](cim-softwareelementchecks.md) -Zuordnung verwendet wird.

</dd> <dt>

[**CIM- \_ Chip**](cim-chip.md)
</dt> <dd>

Die [**CIM- \_ Chip**](cim-chip.md) Klasse stellt den Typ der integrierten Verbindungs Hardware dar, einschließlich ASICs, Prozessoren, Speicherchips usw.

</dd> <dt>

[**CIM \_ clusteringsap**](cim-clusteringsap.md)
</dt> <dd>

Die [**CIM \_ clusteringsap**](cim-clusteringsap.md) -Klasse stellt die Zugriffspunkte eines Clustering-Dienstanbieter dar.

</dd> <dt>

[**CIM- \_ clusteringservice**](cim-clusteringservice.md)
</dt> <dd>

Die [**CIM \_ clusteringservice**](cim-clusteringservice.md) -Klasse stellt die Funktionalität dar, die von einem Cluster bereitgestellt wird. Beispielsweise können Failoverfunktionen als Dienst eines Failoverclusters modelliert werden.

</dd> <dt>

[**CIM \_ clusterserviceaccessbysap**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

Die [**CIM \_ clusterserviceaccessbysap**](cim-clusterserviceaccessbysap.md) -Klasse stellt die Beziehung zwischen einem Clustering-Dienst und seinen Zugriffs Punkten dar.

</dd> <dt>

[**CIM \_ collectedcollections**](cim-collectedcollections.md)
</dt> <dd>

Die [**CIM \_ collectedcollections**](cim-collectedcollections.md) -Klasse ist eine Aggregations Zuordnung, die eine Auflistung verwalteter System Elemente (MSE) darstellt, die in einer Auflistung von MSES enthalten sind.

</dd> <dt>

[**CIM \_ collectedmses**](cim-collectedmses.md)
</dt> <dd>

Die [**CIM \_ collectedmses**](cim-collectedmses.md) Association-Klasse stellt die Member des Gruppierungs Objekts dar, eine [**CollectionOfMSEs**](cim-collectionofmses.md) -Klasse.

</dd> <dt>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> <dd>

Das [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) -Objekt ermöglicht das Gruppieren von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten zum Zweck der Zuordnung von Einstellungen und Konfigurationen. Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.

</dd> <dt>

[**CIM \_ collectionofsensors**](cim-collectionofsensors.md)
</dt> <dd>

Die [**CIM \_ collectionofsensors**](cim-collectionofsensors.md) -Zuordnung stellt die binären Sensoren dar, die den Multistate-Sensor bilden.

</dd> <dt>

[**CIM- \_ CollectionSetting**](cim-collectionsetting.md)
</dt> <dd>

Die [**CIM \_ CollectionSetting**](cim-collectionsetting.md) -Klasse stellt die Zuordnung zwischen einem [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) und der Einstellungs Klasse dar, die für Sie definiert ist.

</dd> <dt>

[**CIM- \_ Kompatibilitäts Produkt**](cim-compatibleproduct.md)
</dt> <dd>

Die [**CIM \_ compatibleproduct**](cim-compatibleproduct.md) -Klasse stellt eine Zuordnung zwischen Produkten dar, die angibt, ob zwei referenzierte Produkte interoperabel sind, z. b. ob Sie gemeinsam installiert werden können oder ob es sich um den physischen Container für den anderen handeln kann usw.

</dd> <dt>

[**CIM- \_ Komponente**](cim-component.md)
</dt> <dd>

Die [**CIM- \_ Komponenten**](cim-component.md) Zuordnung stellt die Bestandteile einer Beziehung zwischen MSES dar.

</dd> <dt>

[**CIM- \_ Computersystem**](cim-computersystem.md)
</dt> <dd>

Eine [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse stellt eine spezielle Auflistung von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Instanzen dar. Diese Sammlung bietet Computerfunktionen und dient als Aggregations Punkt zum Zuordnen eines oder mehrerer der folgenden Elemente: Dateisystem, Betriebssystem, Prozessor und Arbeitsspeicher (flüchtiger und nicht flüchtiger Speicher). Diese Klasse wird vom [**CIM- \_ System**](cim-system.md)abgeleitet.

</dd> <dt>

[**CIM \_ computersystemdma**](cim-computersystemdma.md)
</dt> <dd>

Die [**CIM \_ computersystemdma**](cim-computersystemdma.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren DMA-Kanälen (Direct Memory Access) dar.

</dd> <dt>

[**CIM \_ computersystemirq**](cim-computersystemirq.md)
</dt> <dd>

Die [**CIM \_ computersystemirq**](cim-computersystemirq.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Interrupt Request Lines (unqs) dar.

</dd> <dt>

[**CIM \_ computersystemmappedio**](cim-computersystemmappedio.md)
</dt> <dd>

Die [**CIM \_ computersystemmappedio**](cim-computersystemmappedio.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Speicher Abbild-e/a-Ports dar.

</dd> <dt>

[**CIM \_ computersystempackage**](cim-computersystempackage.md)
</dt> <dd>

Die [**CIM \_ computersystempackage**](cim-computersystempackage.md) -Klasse stellt eine Zuordnung dar, die explizit die Beziehung zwischen einheitlichen Computersystemen und einem oder mehreren physischen Paketen definiert. Die Zuordnung ähnelt der Art und Weise, in der logische Geräte durch physische Elemente realisiert werden.

</dd> <dt>

[**CIM \_ computersystemresource**](cim-computersystemresource.md)
</dt> <dd>

Die [**CIM \_ computersystemresource**](cim-computersystemresource.md) -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren Systemressourcen dar.

</dd> <dt>

[**CIM- \_ Konfiguration**](cim-configuration.md)
</dt> <dd>

Das [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt ermöglicht die Gruppierung von Parametersätzen (definiert in [**CIM- \_ Einstellungs**](cim-setting.md) Objekten) und Abhängigkeiten für ein oder mehrere verwaltete Systemelemente.

</dd> <dt>

[**CIM \_ connectedto**](cim-connectedto.md)
</dt> <dd>

Die [**CIM \_ connectedto**](cim-connectedto.md) -Klasse stellt eine Zuordnung dar, die angibt, dass zwei oder mehr physische Connectors verbunden sind.

</dd> <dt>

[**CIM \_ connectorionpackage**](cim-connectoronpackage.md)
</dt> <dd>

Die [**CIM \_ connectoronpackage**](cim-connectoronpackage.md) -Klasse stellt eine Zuordnung dar, die die Einschluss Beziehung zwischen Connectors und Paketen explizit macht. Physische Pakete enthalten Connectors und andere physische Elemente.

</dd> <dt>

[**CIM- \_ Container**](cim-container.md)
</dt> <dd>

Die [**CIM- \_ Container**](cim-container.md) Klasse stellt eine Zuordnung zwischen einem enthaltenen und einem enthaltenden physischen Element dar. Ein enthaltende Objekt muss ein physisches Paket sein.

</dd> <dt>

[**CIM- \_ controlledby**](cim-controlledby.md)
</dt> <dd>

Die [**CIM \_ controlledby**](cim-controlledby.md) -Beziehung gibt an, welche Geräte von dem logischen Controller Gerät befohlen werden bzw. darauf zugreifen.

</dd> <dt>

[**CIM- \_ Controller**](cim-controller.md)
</dt> <dd>

Die [**CIM- \_ Controller**](cim-controller.md) Klasse ist eine übergeordnete Klasse zum Gruppieren von verschiedenen Steuerelement bezogenen Geräten. Beispiele für Controller sind SCSI-Controller, USB-Controller und serielle Controller.

</dd> <dt>

[**CIM \_ coolingdevice**](cim-coolingdevice.md)
</dt> <dd>

Die [**CIM \_ coolingdevice**](cim-coolingdevice.md) -Klasse stellt die Funktionen und die Verwaltung von Kühlgeräten dar.

</dd> <dt>

[**CIM- \_ copyfileaction**](cim-copyfileaction.md)
</dt> <dd>

Die [**CIM \_ copyfileaction**](cim-copyfileaction.md) -Klasse stellt das Verschieben oder Kopieren von Dateien von einem Computersystem an einen neuen Speicherort dar.

</dd> <dt>

[**CIM- \_ Aktion**](cim-createdirectoryaction.md)
</dt> <dd>

Die CIM-Klasse " [**\_ kreatedirectoryaction**](cim-createdirectoryaction.md) " erstellt leere Verzeichnisse für Software Elemente, die lokal installiert werden sollen.

</dd> <dt>

[**CIM \_ CurrentSensor**](cim-currentsensor.md)
</dt> <dd>

Die [**CIM \_ CurrentSensor**](cim-currentsensor.md) -Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.

</dd> <dt>

[**CIM- \_ Datendatei**](cim-datafile.md)
</dt> <dd>

Die [**CIM \_ DataFile**](cim-datafile.md) -Klasse stellt eine benannte Auflistung von Daten oder ausführbarem Code dar. Es werden nur Instanzen von Dateien auf lokalen Festplatten Datenträgern zurückgegeben.

</dd> <dt>

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> <dd>

Die [**CIM- \_ Abhängigkeits**](cim-dependency.md) Klasse stellt eine Zuordnung dar, die Abhängigkeitsbeziehungen zwischen Objekten herstellt.

</dd> <dt>

[**CIM \_ dependencycontext**](cim-dependencycontext.md)
</dt> <dd>

Die [**CIM \_ dependencycontext**](cim-dependencycontext.md) -Beziehung ordnet eine [**CIM- \_ Abhängigkeits**](cim-dependency.md) Klasse einem oder mehreren [**CIM- \_ Konfigurations**](cim-configuration.md) Objekten zu. Beispielsweise können die Abhängigkeiten eines Computer Systems je nach Netzwerk, an das das System angefügt ist, geändert werden.

</dd> <dt>

[**CIM- \_ Desktop Monitor**](cim-desktopmonitor.md)
</dt> <dd>

Die [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md) -Klasse stellt die Funktionen und die Verwaltung des logischen CRT-Geräts (Desktop Monitor) dar.

</dd> <dt>

[**CIM \_ deviceaccessedbyfile**](cim-deviceaccessedbyfile.md)
</dt> <dd>

Die [**CIM \_ deviceaccessedbyfile**](cim-deviceaccessedbyfile.md) -Zuordnungs Klasse gibt das logische Gerät an, auf das über die [**CIM \_ Devicefile**](cim-devicefile.md) -Klasse zugegriffen wird.

</dd> <dt>

[**CIM-Geräte \_ Steuerung**](cim-deviceconnection.md)
</dt> <dd>

Die [**CIM- \_ deviceconnetction**](cim-deviceconnection.md) -Zuordnungs Klasse stellt zwei oder mehr verbundene Geräte dar.

</dd> <dt>

[**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md)
</dt> <dd>

Die [**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md) -Klasse ist eine statistische Klasse, die Fehler bezogene Leistungsindikatoren für ein logisches Gerät enthält. Die Fehlertypen werden von CCITT (REC X. 733) und ISO (IEC 10164-4) definiert.

</dd> <dt>

[**CIM- \_ Devicefile**](cim-devicefile.md)
</dt> <dd>

Die [**CIM \_ Devicefile**](cim-devicefile.md) -Klasse stellt einen logischen Dateityp dar, der ein Gerät darstellt. Diese Konvention eignet sich für Betriebssysteme, die Geräte mit einem Bytestream-e/a-Modell verwalten. Das logische Gerät, das dieser Datei zugeordnet ist, wird mithilfe der [**CIM \_ deviceaccessedbyfile**](cim-deviceaccessedbyfile.md) -Beziehung angegeben.

</dd> <dt>

[**CIM-Geräte \_ Implementierung**](cim-devicesapimplementation.md)
</dt> <dd>

Die [**CIM-Klasse \_ devicesapimplementation**](cim-devicesapimplementation.md) stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und der Art der Implementierung dar. Wenn einem SAP Viele logische Geräte zugeordnet sind, werden die Elemente zusammen mit dem Zugriffspunkt bereitgestellt. Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des SAP-Objekts.

</dd> <dt>

[**CIM-Geräte \_ Erweiterung**](cim-deviceserviceimplementation.md)
</dt> <dd>

Die [**CIM- \_ deviceserviceimplementation**](cim-deviceserviceimplementation.md) -Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung dar. Wenn mehrere Geräte einem Dienst zugeordnet sind, werden die Elemente zusammen verwendet, um den Dienst bereitzustellen. Wenn verschiedene Implementierungen eines Dienstanbieter vorhanden sind, führt jede Implementierung zu einzelnen Instanziierungen des Dienst Objekts.

</dd> <dt>

[**CIM-Geräte \_ Abteilung**](cim-devicesoftware.md)
</dt> <dd>

Die [**CIM- \_ devicesoftware**](cim-devicesoftware.md) -Beziehung identifiziert Software, die einem Gerät zugeordnet ist, z. b. Treiber, Konfigurations-oder Anwendungssoftware oder Firmware.

</dd> <dt>

[**CIM- \_ Verzeichnis**](cim-directory.md)
</dt> <dd>

Die [**CIM- \_ Verzeichnis**](cim-directory.md) Klasse stellt einen Dateityp dar, der die darin enthaltenen Datendateien logisch gruppiert und Pfadinformationen für die gruppierten Dateien bereitstellt.

</dd> <dt>

[**CIM \_ Director Action**](cim-directoryaction.md)
</dt> <dd>

Die [**abstrakte \_ directoryaction**](cim-directoryaction.md) -Klasse wird Verzeichnisse verwaltet. Die Verzeichnis Erstellung wird von der CIM-Klasse " [**\_ kreatedirectoryaction**](cim-createdirectoryaction.md) " verarbeitet, und die Verzeichnis Entfernung erfolgt durch die [**CIM- \_ removedirectoryaction**](cim-removedirectoryaction.md) -Klasse.

</dd> <dt>

[**CIM \_ directoriykontainsfile**](cim-directorycontainsfile.md)
</dt> <dd>

Die [**CIM \_ directorykontainsfile**](cim-directorycontainsfile.md) -Klasse stellt eine Zuordnung zwischen einem Verzeichnis und den Dateien dar, die in diesem Verzeichnis enthalten sind.

</dd> <dt>

[**CIM- \_ directspecification**](cim-directoryspecification.md)
</dt> <dd>

Die [**CIM- \_ directoryspecification**](cim-directoryspecification.md) -Klasse erfasst die Hauptverzeichnis Struktur eines Software Elements. Diese Klasse wird verwendet, um die Dateien eines Software Elements in verwaltbaren Einheiten zu organisieren, die auf einem Computersystem verschoben werden können.

</dd> <dt>

[**CIM \_ directoriyspecificationfile**](cim-directoryspecificationfile.md)
</dt> <dd>

Die [**CIM- \_ directoryspecificationfile-Zuordnung**](cim-directoryspecificationfile.md) stellt das Verzeichnis dar, das die Datei enthält, die durch Verweisen auf die CIM- [**\_ directoryspecification**](cim-directoryspecification.md) -Klasse angegeben wird.

</dd> <dt>

[**CIM \_ diskretesensor**](cim-discretesensor.md)
</dt> <dd>

Die [**CIM \_ diskretesensor**](cim-discretesensor.md) -Klasse verfügt über einen Satz gültiger Zeichen folgen Werte, die Sie melden kann. Die Werte werden in der **PossibleValues** -Eigenschaft des Sensors aufgelistet. Ein diskreter Sensor verfügt immer über einen aktuellen Lesevorgang, der einem der-Enumerationswerte entspricht.

</dd> <dt>

[**CIM- \_ diskdrive**](cim-diskdrive.md)
</dt> <dd>

Die [**CIM \_ diskdrive**](cim-diskdrive.md) -Klasse stellt ein physisches Laufwerk dar, das vom Betriebssystem erkannt wird. Die Festplattenlaufwerke entsprechen den logischen und Verwaltungs Merkmalen des Laufwerks, und in manchen Fällen werden die physischen Merkmale des Geräts möglicherweise nicht angezeigt. Eine Schnittstelle zu einem physischen Laufwerk ist ein Member dieser Klasse. Ein Objekt, das auf einem anderen logischen Gerät basiert, ist jedoch kein Member dieser Klasse.

</dd> <dt>

[**CIM- \_ Diskettelaufwerk**](cim-diskettedrive.md)
</dt> <dd>

Die [**CIM \_ diskettedrive**](cim-diskettedrive.md) -Klasse stellt die Funktionen und die Verwaltung eines Disketten Laufwerks dar.

</dd> <dt>

[**CIM \_ Diskpartition**](cim-diskpartition.md)
</dt> <dd>

Die [**CIM \_ Diskpartition**](cim-diskpartition.md) -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, der vom Betriebssystem mithilfe der Felder Typ und Untertyp der Partition identifiziert werden kann. Datenträger Partitionen sollten direkt durch physische Medien (angegeben durch die [**CIM- \_**](cim-realizesdiskpartition.md) Neuzuordnung) oder auf Speichervolumes erstellt werden.

</dd> <dt>

[**CIM \_ diskspacecheck**](cim-diskspacecheck.md)
</dt> <dd>

Die [**CIM \_ diskspacecheck**](cim-diskspacecheck.md) -Klasse überprüft die Menge an verfügbarem Speicherplatz des Systems und gibt Sie in der **AvailableDiskSpace** -Eigenschaft an. Details werden mit dem Wert in der **AvailableSpace** -Eigenschaft des [**CIM- \_ Dateisystem**](cim-filesystem.md) Objekts verglichen, das dem [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt zugeordnet ist, in dem die Systemumgebung beschrieben wird. Wenn der Wert der **AvailableSpace** -Eigenschaft größer oder gleich dem Wert ist, der in der **AvailableDiskSpace** -Eigenschaft angegeben ist, wird die Bedingung erfüllt.

</dd> <dt>

[**CIM- \_ Anzeige**](cim-display.md)
</dt> <dd>

Die [**CIM- \_ Anzeige**](cim-display.md) Klasse ist eine übergeordnete Klasse zum Gruppieren von verschiedenen Anzeigegeräten.

</dd> <dt>

[**CIM \_ DMA**](cim-dma.md)
</dt> <dd>

Die [**CIM- \_ DMA**](cim-dma.md) -Klasse stellt die Computerarchitektur für den direkten Speicherzugriff (DMA) dar.

</dd> <dt>

[**CIM \_ angedockt**](cim-docked.md)
</dt> <dd>

Die in [**CIM \_ angedockte**](cim-docked.md) Zuordnung stellt die Beziehung zwischen zwei Chassis dar. Beispielsweise kann ein Laptop (ein Typ von Chassis) an einer Docking Station (einem anderen Typ von Chassis) angedockt werden. Diese typische Beziehung wird explizit beschrieben.

</dd> <dt>

[**CIM- \_ Element Kapazität**](cim-elementcapacity.md)
</dt> <dd>

Die [**CIM \_ elementcapacity**](cim-elementcapacity.md) -Klasse ordnet ein [**CIM \_ physicalcapacity**](cim-physicalcapacity.md) -Objekt einem oder mehreren physischen Elementen zu. Es ordnet eine Beschreibung der minimalen und maximalen Hardwareanforderungen (bzw.-Funktionen) den physischen Elementen zu, die beschrieben werden.

</dd> <dt>

[**CIM- \_ Element Konfiguration**](cim-elementconfiguration.md)
</dt> <dd>

Die [**CIM- \_ ElementConfiguration**](cim-elementconfiguration.md) -Zuordnung verknüpft ein [**CIM- \_ Konfigurations**](cim-configuration.md) Objekt mit einem oder mehreren verwalteten Systemelementen. Das **CIM- \_ Konfigurations** Objekt stellt ein bestimmtes Verhalten oder einen gewünschten funktionalen Zustand für das zugeordnete [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)dar.

</dd> <dt>

[**CIM- \_ Element Setting**](cim-elementsetting.md)
</dt> <dd>

Die [**CIM- \_ ElementSetting**](cim-elementsetting.md) -Klasse stellt die Zuordnung zwischen verwalteten Systemelementen und der Einstellungs Klasse dar, die für Sie definiert ist.

</dd> <dt>

[**CIM- \_ elementslinked**](cim-elementslinked.md)
</dt> <dd>

Die [**CIM \_ elementslinked**](cim-elementslinked.md) Association stellt physische Elemente dar, die von einem physischen Link miteinander verkabelt werden.

</dd> <dt>

[**CIM \_ errorcountersfordevice**](cim-errorcountersfordevice.md)
</dt> <dd>

Die [**CIM-Klasse \_ errorcountersfordevice**](cim-errorcountersfordevice.md) ordnet dem logischen Gerät, auf das Sie angewendet wird, die [**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md) -Klasse zu.

</dd> <dt>

[**CIM \_ executeprogram**](cim-executeprogram.md)
</dt> <dd>

Die [**CIM \_ executeprogram**](cim-executeprogram.md) -Klasse stellt Dateien dar, die auf dem System ausgeführt werden können, auf dem das Softwareelement installiert ist.

</dd> <dt>

[**CIM- \_ Export**](cim-export.md)
</dt> <dd>

Die [**CIM- \_ Export**](cim-export.md) Klasse stellt eine Zuordnung zwischen einem lokalen Dateisystem und den zugehörigen Verzeichnissen dar, die angeben, dass die angegebenen Verzeichnisse zum Einbinden verfügbar sind. Beim Exportieren eines vollständigen Dateisystems sollte das Verzeichnis auf das oberste Verzeichnis des Dateisystems verweisen.

</dd> <dt>

[**CIM \_ extracapacitygroup**](cim-extracapacitygroup.md)
</dt> <dd>

Die [**CIM \_ extracapacitygroup**](cim-extracapacitygroup.md) -Klasse wird von einer Redundanz Gruppe abgeleitet, die angibt, dass die aggregierten Elemente mehr Kapazität oder mehr Kapazität aufweisen, als erforderlich sind. Ein Beispiel für diese Art von Redundanz ist die Installation von N + 1 Stromversorgungen oder Lüfter in einem System.

</dd> <dt>

[**CIM- \_ Lüfter**](cim-fan.md)
</dt> <dd>

Die [**CIM- \_ Lüfter**](cim-fan.md) -Klasse stellt die Funktionen und die Verwaltung eines Lüfter-kühl Geräts dar.

</dd> <dt>

[**CIM- \_ fileaction**](cim-fileaction.md)
</dt> <dd>

Mit der [**CIM \_ fileaction**](cim-fileaction.md) -Klasse kann der Autor Dateien suchen, die bereits auf dem Computer eines Benutzers vorhanden sind, und diese Dateien dann verschieben oder an einen neuen Speicherort kopieren.

</dd> <dt>

[**CIM- \_ Datei Spezifikation**](cim-filespecification.md)
</dt> <dd>

Die [**CIM- \_ filespecification**](cim-filespecification.md) -Klasse stellt eine Datei dar, die sich entweder in einem oder aus dem System befindet. Die Datei befindet sich in dem Verzeichnis, das durch die [**CIM \_ Director yspecificationfile-Zuordnung**](cim-directoryspecificationfile.md) identifiziert wird. Die [**Aufruf**](invoke-method-in-class-cim-filespecification.md) Methode verwendet die Informationen, um zu überprüfen, ob die Datei vorhanden ist. Beachten Sie, dass Eigenschaften mit einem **null** -Wert nicht geprüft werden.

</dd> <dt>

[**CIM- \_ FileStorage**](cim-filestorage.md)
</dt> <dd>

Die [**CIM- \_ FileStorage**](cim-filestorage.md) -Zuordnung verknüpft das Dateisystem und die logischen Dateien, die über das Dateisystem adressiert werden.

</dd> <dt>

[**CIM- \_ Dateisystem**](cim-filesystem.md)
</dt> <dd>

Die [**CIM- \_ Dateisystem**](cim-filesystem.md) Klasse stellt eine Datei oder ein DataSet dar, die sich lokal auf einem Computersystem befinden oder von einem Dateiserver Remote eingebunden werden.

</dd> <dt>

[**CIM- \_ Flatpanel**](cim-flatpanel.md)
</dt> <dd>

Die [**CIM- \_ Flatpanel**](cim-flatpanel.md) -Klasse stellt die Funktionen und die Verwaltung des logischen Flatpanel-Geräts dar.

</dd> <dt>

[**CIM \_ fromdirector Action**](cim-fromdirectoryaction.md)
</dt> <dd>

Die [**CIM \_ fromdirector Action**](cim-fromdirectoryaction.md) -Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis durch eine vorherige Aktion erstellt wurde. Diese Zuordnung darf nicht mit einer [**CIM \_ fromdirector yspecification**](cim-fromdirectoryspecification.md) -Zuordnung vorhanden sein. eine Datei Aktion kann nur ein einzelnes Quellverzeichnis umfassen.

</dd> <dt>

[**CIM \_ fromdirectoriyspecification**](cim-fromdirectoryspecification.md)
</dt> <dd>

Die [**CIM \_ fromdirector yspecification**](cim-fromdirectoryspecification.md) -Zuordnung identifiziert das Quellverzeichnis für die Datei Aktion. Wenn diese Zuordnung verwendet wird, wird davon ausgegangen, dass das Quellverzeichnis bereits vorhanden ist. Diese Zuordnung darf nicht mit einer [**CIM \_ fromdirector yaction**](cim-fromdirectoryaction.md) -Zuordnung vorhanden sein. eine Datei Aktion kann nur ein einzelnes Quellverzeichnis umfassen.

</dd> <dt>

[**CIM \_ FRU**](cim-fru.md)
</dt> <dd>

Die [**CIM \_ FRU**](cim-fru.md) -Klasse stellt eine Hersteller definierte Auflistung von Produkten und physischen Elementen dar, die einer von einem Feld ersetzbaren Einheit (FRU) zugeordnet sind, um ein Produkt am Standort des Kunden zu unterstützen, zu warten oder zu aktualisieren.

</dd> <dt>

[**CIM- \_ fruincluentsproduct**](cim-fruincludesproduct.md)
</dt> <dd>

Die CIM-Klasse " [**\_ fruincludesproduct**](cim-fruincludesproduct.md) " zeigt an, dass eine ersetzbare Feld Einheit (FRU) aus anderen Produkten bestehen kann.

</dd> <dt>

[**CIM \_ fruphysicalelements**](cim-fruphysicalelements.md)
</dt> <dd>

Die CIM-Klasse " [**\_ fruphysicalelements**](cim-fruphysicalelements.md) " stellt die physischen Elemente dar, die eine ersetzbare (Feld) Einheit (FRU) bilden.

</dd> <dt>

[**CIM- \_ Heatpipe**](cim-heatpipe.md)
</dt> <dd>

Die [**CIM- \_ Heatpipe**](cim-heatpipe.md) -Klasse stellt die Funktionen und die Verwaltung eines wärmepipe-kühl Geräts dar.

</dd> <dt>

[**CIM- \_ hubspoint**](cim-hostedaccesspoint.md)
</dt> <dd>

Die CIM-Klasse " [**\_ stestedaccesspoint**](cim-hostedaccesspoint.md) " stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und dem System dar, auf dem es bereitgestellt wird. Jedes System hostet möglicherweise viele SAPS.

</dd> <dt>

[**CIM- \_ boostedbootsap**](cim-hostedbootsap.md)
</dt> <dd>

Die CIM-Klasse " [**\_ shostedbootsap**](cim-hostedbootsap.md) " definiert das Hosting-einheitliche Computersystem für eine [**CIM- \_ bootsap**](cim-bootsap.md) -Klasse. Da diese Beziehung von [**CIM \_ hostspoint**](cim-hostedaccesspoint.md)untergeordnet ist, erbt Sie das für [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)definierte Bereichs Schema/Benennungs Schema, bei dem ein Zugriffspunkt dem Hostingsystem entspricht. In diesem Fall muss **CIM \_ bootsap** auf seine hostende [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md) -Klasse zurückgreifen.

</dd> <dt>

[**CIM- \_ Boots Dienst**](cim-hostedbootservice.md)
</dt> <dd>

Die CIM-Klasse " [**\_ hostbootservice**](cim-hostedbootservice.md) " ordnet ein Hostingsystem und einen Start Dienst zu. Da diese Beziehung vom [**CIM- \_ Hostingdienst**](cim-hostedservice.md)untergeordnet ist, erbt Sie das für den Dienst definierte Bereichs Schema/Benennungs Schema, bei dem ein Dienst auf das Hostingsystem beschränkt wird.

</dd> <dt>

[**CIM- \_ Dateisystem**](cim-hostedfilesystem.md)
</dt> <dd>

Die [**CIM \_ hostedfile**](cim-hostedfilesystem.md) System-Zuordnung stellt eine Verknüpfung zwischen dem Computersystem und dem Dateisystem dar, das auf dem Computersystem gehostet wird.

</dd> <dt>

[**CIM-Host- \_ jobdestination**](cim-hostedjobdestination.md)
</dt> <dd>

Die CIM-Klasse " [**\_ hostjobdestination**](cim-hostedjobdestination.md) " stellt eine Zuordnung zwischen einem Auftrags Ziel und dem System dar, auf dem es sich befindet. Ein System kann viele Auftrags Warteschlangen hosten. Auftrags Ziele werden an das Hostingsystem zurück verschoben.

</dd> <dt>

[**CIM- \_ Dienst**](cim-hostedservice.md)
</dt> <dd>

Die CIM-Klasse " [**\_ Hostdienst**](cim-hostedservice.md) " stellt eine Zuordnung zwischen einem Dienst und dem System dar, auf dem sich die Funktionalität befindet. Ein System kann viele Dienste hosten, die auf das Hostingsystem zurückgreifen. Das Modell stellt keine Dienste dar, die auf mehreren Systemen gehostet werden.

</dd> <dt>

[**CIM- \_ infraredcontroller**](cim-infraredcontroller.md)
</dt> <dd>

Die CIM-Klasse " [**\_ infraredcontroller**](cim-infraredcontroller.md) " stellt die Funktionen und die Verwaltung eines Infrarot Controllers dar.

</dd> <dt>

[**CIM- \_ instanalledos**](cim-installedos.md)
</dt> <dd>

Die [**CIM \_ installedos**](cim-installedos.md) Association-Klasse stellt eine Verknüpfung zwischen dem Computersystem und dem installierten Betriebssystem dar. Ein Betriebssystem wird installiert, wenn es sich im Speicherbereich eines Computer Systems befindet (z. b. auf ein Laufwerk kopiert oder in den Arbeitsspeicher heruntergeladen wird).

</dd> <dt>

[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)
</dt> <dd>

Die [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) -Klasse ordnet ein Computersystem einem installierten Softwareelement zu.

</dd> <dt>

[**CIM \_ -Antwort**](cim-irq.md)
</dt> <dd>

Die CIM-Klasse " [**\_ iriq**](cim-irq.md) " stellt eine Intel Architecture Interrupt Request Line (UNQ) dar.

</dd> <dt>

[**CIM- \_ Auftrag**](cim-job.md)
</dt> <dd>

Die [**CIM- \_ Auftrags**](cim-job.md) Klasse stellt eine Arbeitseinheit für ein System dar, z. b. einen Druckauftrag. Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant werden kann.

</dd> <dt>

[**CIM \_ jobdestination**](cim-jobdestination.md)
</dt> <dd>

Die [**CIM \_ jobdestination**](cim-jobdestination.md) -Klasse stellt dar, wo ein Auftrag zur Verarbeitung übermittelt wird. Sie kann auf eine Warteschlange verweisen, die NULL oder mehr Aufträge enthält, z. b. eine Druck Warteschlange, die Druckaufträge enthält. Auftrags Ziele werden auf Systemen gehostet, ähnlich der Art, in der Dienste auf Systemen gehostet werden.

</dd> <dt>

[**CIM \_ jobdestinationjobs**](cim-jobdestinationjobs.md)
</dt> <dd>

Die [**CIM \_ jobdestinationjobs-Zuordnung**](cim-jobdestinationjobs.md) beschreibt, wo ein Auftrag zur Verarbeitung übermittelt wird (d. h. an welches Auftrags Ziel).

</dd> <dt>

[**CIM- \_ Tastatur**](cim-keyboard.md)
</dt> <dd>

Die [**CIM- \_ Tastatur**](cim-keyboard.md) Klasse stellt die Funktionen und die Verwaltung des logischen Tastatur Geräts dar.

</dd> <dt>

[**CIM \_ linkhasconnector**](cim-linkhasconnector.md)
</dt> <dd>

Die [**CIM \_ linkhasconnector**](cim-linkhasconnector.md) -Klasse ordnet Kabel und Verknüpfungen zu, die als physische Connectors verwendet werden, die die physischen Elemente verbinden. Diese Zuordnung definiert explizit die Beziehung von Connectors für [**CIM \_ physicallink**](cim-physicallink.md).

</dd> <dt>

[**CIM \_ LocalFile System**](cim-localfilesystem.md)
</dt> <dd>

Die [**CIM \_ LocalFile**](cim-localfilesystem.md) System-Klasse stellt den Dateispeicher dar, der von einem Computersystem über lokale Mittel (z. b. direkten Zugriff auf Gerätetreiber) gesteuert wird. Der Dateispeicher kann direkt vom Computersystem verwaltet werden, ohne dass ein anderer Computer als Dateiserver fungieren muss. Bei einem Cluster Dateisystem ist das Dateisystem jedoch lokal und wird daher auf den Cluster abgehandelt.

</dd> <dt>

[**CIM- \_ Speicherort**](cim-location.md)
</dt> <dd>

Die [**CIM- \_ Location**](cim-location.md) -Klasse stellt die Position und die Adresse eines physischen Elements dar.

</dd> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dd>

Die [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse stellt eine Hardware Entität dar, die in physischer Hardware erkannt werden kann oder nicht.

</dd> <dt>

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)
</dt> <dd>

Die [**CIM \_ LogicalDisk**](cim-logicaldisk.md) -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die von einem Dateisystem über das **DeviceID** (Key)-Feld des Datenträgers identifiziert werden. Beispielsweise enthält das Feld " **DeviceID** " in einer Windows-Umgebung einen Laufwerk Buchstaben. in einer UNIX-Umgebung enthält Sie den Zugriffs Pfad. und in einer NetWare-Umgebung enthält Sie den Volumenamen.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

Die [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) -Klasse ordnet der Festplatten Partition, auf der Sie sich befindet, einen logischen Datenträger zu.

</dd> <dt>

[**CIM \_ logicaldiskbasedonvolumeset**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

Die [**CIM \_ logicaldiskbasedonvolumeset**](cim-logicaldiskbasedonvolumeset.md) -Zuordnung bezieht logische Datenträger mit dem Volume, auf dem Sie gefunden werden. Logische Datenträger können auf einem einzelnen Volume (z. b. von einem Software Volume-Manager verfügbar gemacht) oder auf einer Datenträger Partition basieren.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

Die [**CIM \_ LogicalElement**](cim-logicalelement.md) -Klasse ist die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten, z. b. profile, Prozesse oder Systemfunktionen, in Form logischer Geräte darstellen.

</dd> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dd>

Die [**CIM \_ LogicalFile**](cim-logicalfile.md) -Klasse stellt eine benannte Auflistung von Daten dar, bei der es sich um ausführbaren Code handeln kann, der sich in einem Dateisystem in einem Speicherblock befindet.

</dd> <dt>

[**CIM- \_ logikalidentität**](cim-logicalidentity.md)
</dt> <dd>

Die [**CIM \_ logicalidentity**](cim-logicalidentity.md) -Klasse ist eine abstrakte und generische Zuordnung, die angibt, dass zwei logische Elemente verschiedene Aspekte der gleichen zugrunde liegenden Entität darstellen.

</dd> <dt>

[**CIM- \_ Magnet Laufwerk**](cim-magnetoopticaldrive.md)
</dt> <dd>

Die CIM-Klasse " [**\_ magnetyopticaldrive**](cim-magnetoopticaldrive.md) " stellt die Funktionen und die Verwaltung eines "Magneto-Optical"-Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

Die [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse ist die Basisklasse für die System Element Hierarchie. Jede unterscheidbare Systemkomponente ist ein Kandidat für die Einbindung in diese Klasse.

</dd> <dt>

[**CIM- \_ Managementcontroller**](cim-managementcontroller.md)
</dt> <dd>

Die [**CIM \_ Managementcontroller**](cim-managementcontroller.md) -Klasse bezieht sich auf die Funktionen und die Verwaltung eines Verwaltungs Controllers.

</dd> <dt>

[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)
</dt> <dd>

Die [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md) -Klasse stellt die Möglichkeit dar, auf ein oder mehrere Medien zuzugreifen und dann die Medien zum Speichern und Abrufen von Daten zu verwenden.

</dd> <dt>

[**CIM- \_ mediapresent**](cim-mediapresent.md)
</dt> <dd>

Die [**CIM \_ mediapresent**](cim-mediapresent.md) -Zuordnung beschreibt eine Beziehung, bei der über ein Medien Zugriffsgerät auf einen Speicherblock zugegriffen werden muss.

</dd> <dt>

[**CIM- \_ Speicher**](cim-memory.md)
</dt> <dd>

Die [**CIM- \_ Speicher**](cim-memory.md) Klasse stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.

</dd> <dt>

[**CIM- \_ memorycapacity**](cim-memorycapacity.md)
</dt> <dd>

Die [**CIM \_ memorycapacity**](cim-memorycapacity.md) -Klasse stellt den Arbeitsspeicher dar, der auf einem physischen Element und dessen minimalen und maximalen Konfigurationen installiert werden kann. Informationen zu derzeit installiertem Arbeitsspeicher und den minimalen und maximalen Anforderungen eines Elements befinden sich in Instanzen der [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) -Klasse.

</dd> <dt>

[**CIM- \_ memorycheck**](cim-memorycheck.md)
</dt> <dd>

Die [**CIM \_ memorycheck**](cim-memorycheck.md) -Klasse gibt eine Bedingung für die minimale Arbeitsspeicher Menge an, die auf einem System verfügbar sein muss.

</dd> <dt>

[**CIM \_ memorymappedio**](cim-memorymappedio.md)
</dt> <dd>

Die [**CIM \_ memorymappedio**](cim-memorymappedio.md) -Klasse stellt die Computerarchitektur-e/a mit Speicher Abbild dar. Diese Klasse adressiert Arbeitsspeicher-und Port-e/a-Ressourcen.

</dd> <dt>

[**CIM \_ memoryoncard**](cim-memoryoncard.md)
</dt> <dd>

Die [**CIM \_ memoryoncard**](cim-memoryoncard.md) -Klasse ordnet physischen Speicher zu, der sich auf hostingboards, Adapterkarten usw. befindet. Diese Zuordnung definiert explizit die Beziehung Zwischenspeicher und Karten.

</dd> <dt>

[**CIM- \_ memorywithmedia**](cim-memorywithmedia.md)
</dt> <dd>

Die [**CIM- \_ memorywithmedia**](cim-memorywithmedia.md) -Klasse ordnet physischen Speicher einem physischen Medium und der zugehörigen Cartridge zu. Der Arbeitsspeicher bietet Medien Identifikation und speichert benutzerspezifische Daten.

</dd> <dt>

[**CIM \_ modifysettingaction**](cim-modifysettingaction.md)
</dt> <dd>

Die [**CIM \_ modifysettingaction**](cim-modifysettingaction.md) -Klasse stellt die Informationen zum Ändern einer bestimmten Einstellungsdatei für einen bestimmten Eintrag mit einem bestimmten Wert dar.

</dd> <dt>

[**CIM- \_ Monitorauflösung**](cim-monitorresolution.md)
</dt> <dd>

Die [**CIM- \_ monitorresolution**](cim-monitorresolution.md) -Klasse stellt die Beziehung zwischen horizontaler und vertikaler Auflösung und der Aktualisierungsrate und dem Überprüfungs Modus für einen Desktop Monitor dar. Werte werden im Videocontroller Objekt angegeben.

</dd> <dt>

[**CIM- \_ monitorsetting**](cim-monitorsetting.md)
</dt> <dd>

Die [**CIM- \_ monitorsetting**](cim-monitorsetting.md) -Klasse ordnet die Monitor Auflösung dem Desktop Monitor zu, auf den Sie angewendet wird.

</dd> <dt>

[**CIM- \_ einbinden**](cim-mount.md)
</dt> <dd>

Die [**CIM \_**](cim-mount.md) -Bereitstellungs Klasse stellt eine Zuordnung zwischen einem Dateisystem und einem Verzeichnis dar, an das es angefügt ist.

</dd> <dt>

[**CIM- \_ multistaatensor**](cim-multistatesensor.md)
</dt> <dd>

Die [**CIM \_ multistaatensor**](cim-multistatesensor.md) -Klasse stellt eine multimember-Gruppe von binären Sensoren dar, in der jeder binäre Sensor ein boolesches Ergebnis meldet.

</dd> <dt>

[**CIM- \_ Netzwerkadapter**](cim-networkadapter.md)
</dt> <dd>

Die [**CIM- \_ netzwerkadapterklasse**](cim-networkadapter.md) ist eine abstrakte Klasse, die allgemeine Konzepte der Netzwerkhardware definiert (z. b. permanente Adresse oder Geschwindigkeit der Operation). Die Informationen werden mithilfe der CIM-Zuordnung " [**\_ devicesapimplementation**](cim-devicesapimplementation.md) " übermittelt.

</dd> <dt>

[**CIM- \_ NFS**](cim-nfs.md)
</dt> <dd>

Die [**CIM- \_ NFS**](cim-nfs.md) -Klasse stellt ein Remote Dateisystem dar, das mit dem NFS-Protokoll (Network File System) von einem Computersystem bereitgestellt wird.

</dd> <dt>

[**CIM- \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> <dd>

Die [**CIM-Klasse \_ NonVolatileStorage**](cim-nonvolatilestorage.md) stellt die Funktionen und die Verwaltung von nichtflüchtigem Speicher dar. Nicht flüchtiger Speicher umfasst nativ Flash-und ROM-Speicher.

</dd> <dt>

[**CIM- \_ numericsensor**](cim-numericsensor.md)
</dt> <dd>

Die [**CIM- \_ numericsensor**](cim-numericsensor.md) -Klasse stellt einen numerischen Sensor dar, der numerische Messwerte zurückgibt und optional Schwellenwert Einstellungen unterstützt.

</dd> <dt>

[**CIM- \_ OperatingSystem**](cim-operatingsystem.md)
</dt> <dd>

Die [**CIM \_ OperatingSystem**](cim-operatingsystem.md) -Klasse stellt ein Computerbetriebssystem dar, das aus Software und Firmware besteht, mit denen die Hardware eines Computer Systems verwendbar ist.

</dd> <dt>

[**CIM- \_ operatingsystemsoftwarefeature**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

Die [**CIM \_ operatingsystemsoftwarefeature**](cim-operatingsystemsoftwarefeature.md) -Klasse stellt die Softwarefunktionen dar, aus denen das Betriebssystem besteht.

</dd> <dt>

[**CIM- \_ osprocess**](cim-osprocess.md)
</dt> <dd>

Die [**CIM \_ osprocess**](cim-osprocess.md) -Klasse ordnet das Betriebssystem und einen oder mehrere Prozesse zu, die im Kontext des Betriebssystems ausgeführt werden.

</dd> <dt>

[**CIM- \_ osversioncheck**](cim-osversioncheck.md)
</dt> <dd>

Die [**CIM \_ osversioncheck**](cim-osversioncheck.md) -Klasse gibt die Versionen des Betriebssystems an, die ein Softwareelement unterstützen können.

</dd> <dt>

[**CIM- \_ packagealarm**](cim-packagealarm.md)
</dt> <dd>

Die [**CIM \_ packagealarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) -Zuordnung stellt die Beziehung dar, in der ein Alarmgerät als Teil eines Pakets installiert wird. Die Installation zeigt Probleme mit der Umgebung des Pakets an – den Sicherheitsstatus oder den Gesamtzustand.

</dd> <dt>

[**CIM- \_ packagecooling**](cim-packagecooling.md)
</dt> <dd>

Die [**CIM \_ packagecooling**](cim-packagecooling.md) -Zuordnung stellt die Beziehung dar, in der ein Kühlgerät in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Kühlung des Pakets zu unterstützen.

</dd> <dt>

[**CIM \_ packagedcomponent**](cim-packagedcomponent.md)
</dt> <dd>

Die [**CIM \_ packagedcomponent**](cim-packagedcomponent.md) -Zuordnung stellt eine explizite Beziehung dar, in der eine Komponente in der Regel in einem physischen Paket (z. b. einem Chassis oder einer Karte) enthalten ist.

</dd> <dt>

[**CIM \_ packageingechassis**](cim-packageinchassis.md)
</dt> <dd>

Die [**CIM \_ packageinchassis**](cim-packageinchassis.md) -Zuordnung stellt die Beziehung dar, in der ein Chassis Andere Pakete enthalten kann, z. b. anderes Chassis und Karten.

</dd> <dt>

[**CIM- \_ packageinslot**](cim-packageinslot.md)
</dt> <dd>

Die [**CIM \_ packageinslot**](cim-packageinslot.md) -Zuordnung stellt die Beziehung zwischen den Geräte Karten und dem Gehäuse dar, in dem Sie eingebunden werden.

</dd> <dt>

[**CIM \_ packagetempsensor**](cim-packagetempsensor.md)
</dt> <dd>

Die [**CIM \_ packagetempsensor**](cim-packagetempsensor.md) -Zuordnung stellt die Beziehung dar, in der ein Temperatursensor häufig in einem Paket installiert wird, z. b. ein Chassis oder Rack, um die Umgebung des Pakets zu überwachen.

</dd> <dt>

[**CIM- \_ parallelcontroller**](cim-parallelcontroller.md)
</dt> <dd>

Die [**CIM \_ parallelcontroller**](cim-parallelcontroller.md) -Zuordnung bezieht sich auf die Funktionen und die Verwaltung des logischen Parallel Port-Geräts.

</dd> <dt>

[**CIM- \_ participatesinset**](cim-participatesinset.md)
</dt> <dd>

Die [**CIM \_ participatesinset**](cim-participatesinset.md) -Klasse identifiziert physische Elemente, die zusammen ersetzt werden sollen.

</dd> <dt>

[**CIM- \_ PCIController**](cim-pcicontroller.md)
</dt> <dd>

Die [**CIM \_ PCIController**](cim-pcicontroller.md) -Klasse stellt die Eigenschaften und die Verwaltung eines PCI-Controllers dar. Die Eigenschaften in dieser Klasse und deren Unterklassen werden in den verschiedenen PCI-Spezifikationen definiert, die von PCI SIG veröffentlicht werden.

</dd> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> <dd>

Die [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) -Klasse stellt die Funktionen und die Verwaltung eines PCMCIA-Controllers (private Computer Memory Card International Association) dar.

</dd> <dt>

[**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md)
</dt> <dd>

Der [**CIM \_ pcvideocontroller**](cim-pcvideocontroller.md) stellt die Funktionen und die Verwaltung eines Video Controllers für persönliche Computer dar, einen Untertyp eines Video Controllers.

</dd> <dt>

[**CIM \_ pextentredundancycomponent**](cim-pextentredundancycomponent.md)
</dt> <dd>

Die [**CIM \_ pextentredundancycomponent**](cim-pextentredundancycomponent.md) -Klasse stellt die physischen Blöcke dar, die Teil einer Speicher Redundanz Gruppe sind.

</dd> <dt>

[**CIM- \_ physicalcapacity**](cim-physicalcapacity.md)
</dt> <dd>

Die [**CIM \_ physicalcapacity**](cim-physicalcapacity.md) -Klasse ist eine abstrakte Klasse, die die minimalen und maximalen Anforderungen eines physischen Elements und die Fähigkeit zur Unterstützung verschiedener Hardwaretypen darstellt. So können z. b. die minimalen und maximalen Arbeitsspeicher Anforderungen als eine Unterklasse von **CIM \_ physicalcapacity** modelliert werden.

</dd> <dt>

[**CIM- \_ physicalcomponent**](cim-physicalcomponent.md)
</dt> <dd>

Die [**CIM \_ physicalcomponent**](cim-physicalcomponent.md) -Klasse stellt eine Komponente auf niedriger Ebene oder eine grundlegende Komponente innerhalb eines Pakets dar. Ein physisches Element, bei dem es sich nicht um einen Link, einen Connector oder ein Paket handelt, ist ein Nachfolger (oder Member) dieser Klasse.

</dd> <dt>

[**CIM \_ physicalconnector**](cim-physicalconnector.md)
</dt> <dd>

Die [**CIM \_ physicalconnector**](cim-physicalconnector.md) -Klasse stellt ein beliebiges physisches Element dar, das verwendet wird, um eine Verbindung mit anderen Elementen herzustellen. Jedes Objekt, das eine Verbindung herstellen und Signale oder eine Stromversorgung zwischen mindestens zwei physischen Elementen übertragen kann, ist ein Nachfolger (oder Member) dieser Klasse.

</dd> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> <dd>

Die [**CIM \_ PhysicalElement**](cim-physicalelement.md) -Unterklassen definieren jede Komponente eines Systems, das über eine eindeutige physische Identität verfügt. Instanzen dieser Klasse können in Bezug auf Bezeichnungen definiert werden, die physisch an das Objekt angefügt werden können.

</dd> <dt>

[**CIM \_ physicalelementlocation**](cim-physicalelementlocation.md)
</dt> <dd>

Die [**CIM \_ physicalelementlocation**](cim-physicalelementlocation.md) -Klasse ordnet ein physisches Element einem [**CIM- \_ Speicherort**](cim-location.md) Objekt zu Inventur-oder Ersetzungs Zwecken zu.

</dd> <dt>

[**CIM- \_ physicalblock**](cim-physicalextent.md)
</dt> <dd>

Die [**CIM- \_ physicalblock**](cim-physicalextent.md) -Klasse stellt eine SCC RAID-Implementierung dar. Sie definiert die aufeinander folgenden adressierbaren Block Adressen auf einem einzelnen Speichergerät, die als einzelner Speicherblock in derselben [**CIM \_ storageredundancygroup**](cim-storageredundancygroup.md) -Klasse behandelt werden. Eine Alternative, wenn die automatische Konfiguration verwendet wird, besteht darin, die [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) -Klasse zu instanziieren oder zu erweitern.

</dd> <dt>

[**CIM- \_ physicalframe**](cim-physicalframe.md)
</dt> <dd>

Die [**CIM \_ physicalframe**](cim-physicalframe.md) -Klasse ist eine übergeordnete Klasse von Rack, Chassis und anderen Frame Gehäusen, die in Erweiterungs Klassen definiert sind. In dieser übergeordneten Klasse sind Eigenschaften wie **visiblewecker** und **audiblealarm** sowie Daten, die sich auf Sicherheitsverletzungen beziehen, enthalten.

</dd> <dt>

[**CIM \_ physicallink**](cim-physicallink.md)
</dt> <dd>

Die [**CIM \_ physicallink**](cim-physicallink.md) -Klasse stellt die Verkabelung physischer Elemente dar.

</dd> <dt>

[**CIM- \_ physicalmedia**](cim-physicalmedia.md)
</dt> <dd>

Die [**CIM \_ physicalmedia**](cim-physicalmedia.md) -Klasse stellt Typen von Dokumentation und Speichermedium (z. b. Bänder, CD-ROMs usw.) dar.

</dd> <dt>

[**CIM- \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dd>

Die [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) -Klasse stellt Speichergeräte auf niedriger Ebene dar, wie z. b. Simms, DIMMs, Rohdaten Speicher-Chips usw.

</dd> <dt>

[**CIM- \_ physicalpackage**](cim-physicalpackage.md)
</dt> <dd>

Die [**CIM \_ physicalpackage**](cim-physicalpackage.md) -Klasse stellt physische Elemente dar, die andere Komponenten enthalten oder hosten. Beispiele hierfür sind ein Regal Gehäuse oder eine Adapterkarte.

</dd> <dt>

[**CIM- \_ pointingdevice**](cim-pointingdevice.md)
</dt> <dd>

Die [**CIM \_ pointingdevice**](cim-pointingdevice.md) -Klasse stellt ein Gerät dar, das auf die Bereiche auf der Anzeige zeigt. Jedes Gerät, das einen Zeiger bearbeitet oder auf Bereiche in einer visuellen Anzeige zeigt, ist ein Member dieser Klasse. Beispielsweise eine Maus, einen Tablettstift, ein Touchpad oder ein Tablet.

</dd> <dt>

[**CIM- \_ potsmodem**](cim-potsmodem.md)
</dt> <dd>

Die CIM-Klasse " [**\_ potsmodem**](cim-potsmodem.md) " stellt ein Gerät dar, das binäre Daten in Wellen Modulationen für die Sound basierte Übertragung übersetzt, indem eine Verbindung mit dem reinen Telefon System ("Pots") hergestellt wird.

</dd> <dt>

[**CIM- \_ Netzteil**](cim-powersupply.md)
</dt> <dd>

Die [**CIM- \_ PowerSupply**](cim-powersupply.md) -Klasse stellt die Funktionen und die Verwaltung des logischen netzwerknetzwerkgeräts dar.

</dd> <dt>

[**CIM- \_ Drucker**](cim-printer.md)
</dt> <dd>

Die [**CIM- \_ Drucker**](cim-printer.md) Klasse stellt die Funktionen und die Verwaltung des logischen Drucker Geräts dar.

</dd> <dt>

[**CIM- \_ Prozess**](cim-process.md)
</dt> <dd>

Die [**CIM- \_ Prozess**](cim-process.md) Klasse stellt eine einzelne Instanz eines laufenden Programms dar. Ein Benutzer sieht in der Regel einen Prozess als Anwendung oder Aufgabe.

</dd> <dt>

[**CIM- \_ processexecutable**](cim-processexecutable.md)
</dt> <dd>

Die [**CIM \_ processexecutable**](cim-processexecutable.md) -Klasse stellt einen Link zwischen einem Prozess und einer Datendatei dar und gibt an, dass die Datei an der Ausführung des Prozesses beteiligt ist.

</dd> <dt>

[**CIM- \_ Prozessor**](cim-processor.md)
</dt> <dd>

Die [**CIM- \_ Prozessor**](cim-processor.md) Klasse stellt die Funktionen und die Verwaltung des logischen Prozessor Geräts dar.

</dd> <dt>

[**CIM- \_ ProcessThread**](cim-processthread.md)
</dt> <dd>

Die [**CIM- \_ ProcessThread**](cim-processthread.md) -Klasse stellt einen Link zwischen einem Prozess und den Threads dar, die im Kontext des Prozesses ausgeführt werden.

</dd> <dt>

[**CIM- \_ Produkt**](cim-product.md)
</dt> <dd>

Die [**CIM- \_ Produkt**](cim-product.md) Klasse ist eine konkrete Klasse, die eine Auflistung physischer Elemente, Software Features und anderer Produkte darstellt, die als Einheit erworben wurden. Der Erwerb impliziert eine Vereinbarung zwischen dem Lieferanten und dem Consumer, die Auswirkungen auf die Produkt Lizenzierung, den Support und die Gewährleistung haben kann.

</dd> <dt>

[**CIM \_ productfru**](cim-productfru.md)
</dt> <dd>

Die [**CIM \_ productfru**](cim-productfru.md) -Klasse stellt eine Zuordnung zwischen dem Produkt und einer ersetzbaren (Feld) Einheit (FRU) dar, die Informationen zu Produktkomponenten bereitstellt, die bereits waren oder ersetzt werden.

</dd> <dt>

[**CIM \_ productparser**](cim-productparentchild.md)
</dt> <dd>

Die [**CIM \_ productparser**](cim-productparentchild.md) -Zuordnung definiert eine Hierarchie mit über-und untergeordneten Elementen zwischen Produkten. Beispielsweise kann ein Produkt mit anderen Produkten gebündelt werden.

</dd> <dt>

[**CIM \_ productphysicalelements**](cim-productphysicalelements.md)
</dt> <dd>

Die [**CIM \_ productphysicalelements**](cim-productphysicalelements.md) -Klasse stellt die physischen Elemente dar, die ein Produkt bilden.

</dd> <dt>

[**CIM \_ productproductabhängigkeit**](cim-productproductdependency.md)
</dt> <dd>

Die [**CIM \_ productproductdepen-Klasse**](cim-productproductdependency.md) stellt eine Zuordnung zwischen zwei Produkten dar, die angibt, dass eine für die andere installiert werden muss oder nicht. Dies entspricht konzeptionell der [**CIM \_ serviceserviceabhängigkeiten**](cim-serviceservicedependency.md) -Zuordnung.

</dd> <dt>

[**CIM \_ productsoftwarefeatures**](cim-productsoftwarefeatures.md)
</dt> <dd>

Die [**CIM \_ productsoftwarefeatures**](cim-productsoftwarefeatures.md) -Zuordnung identifiziert die Software Features für ein bestimmtes Produkt.

</dd> <dt>

[**CIM- \_ productsupport**](cim-productsupport.md)
</dt> <dd>

Die [**CIM \_ productsupport**](cim-productsupport.md) -Klasse stellt eine Zuordnung Zwischenprodukt und Support Zugriff dar, die die Art der Unterstützung für das Produkt übermittelt. Für ein Produkt sind verschiedene Support Typen verfügbar. das gleiche Support Objekt bietet Unterstützung für mehrere Produkte.

</dd> <dt>

[**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md)
</dt> <dd>

Die [**CIM \_ protectedspaceblock**](cim-protectedspaceextent.md) -Klasse stellt adressierbare logische Block Adressen dar, die als einzelner Speicherblock behandelt werden, sich jedoch in einem einzelnen physischen Block befinden.

</dd> <dt>

[**CIM \_ psextentbasedonpblock**](cim-psextentbasedonpextent.md)
</dt> <dd>

Die [**CIM \_ psextentbasedonpblock**](cim-psextentbasedonpextent.md) -Klasse ordnet Blöcke mit geschütztem Speicherplatz zu, die auf einem physischen Block basieren.

</dd> <dt>

[**CIM- \_ Rack**](cim-rack.md)
</dt> <dd>

Die [**CIM- \_ Rack**](cim-rack.md) -Klasse stellt ein Gestell (ein physischer Frame oder Gehäuse) dar, in dem das Chassis gespeichert wird. In der Regel stellt ein Rack das Gehäuse dar. Alle funktionierenden Komponenten werden in das Chassis gepackt.

</dd> <dt>

[**CIM \_ erkennt**](cim-realizes.md)
</dt> <dd>

Die [**CIM \_**](cim-realizes.md) -Klasse stellt die Zuordnung dar, die die Zuordnung zwischen einem logischen Gerät und der physischen Komponente definiert, die das Gerät implementiert.

</dd> <dt>

[**CIM \_ realizesaggregatepblock**](cim-realizesaggregatepextent.md)
</dt> <dd>

Die CIM-Erweiterung " [**\_ realizesaggregatepblock**](cim-realizesaggregatepextent.md) " stellt die Beziehung dar, in der die [**CIM- \_ aggregatepblock**](cim-aggregatepextent.md) -Klasse auf einem physischen Medium realisiert wird.

</dd> <dt>

[**CIM- \_ realizesdiskpartition**](cim-realizesdiskpartition.md)
</dt> <dd>

Die CIM-Klasse " [**\_ realizesdiskpartition**](cim-realizesdiskpartition.md) " stellt eine Datenträger Partition auf einem physischen Medium dar, die die Erstellung von Partitionen auf einem unformatierten SCSI-oder IDE-Laufwerk modelliert.

</dd> <dt>

[**CIM- \_ realizespblock**](cim-realizespextent.md)
</dt> <dd>

Die CIM-Erweiterung " [**\_ realizespblock**](cim-realizespextent.md) " stellt die Beziehung dar, in der physische Blöcke auf einem physischen Medium realisiert werden. Außerdem wird die Startadresse des physischen Wertebereichs auf dem physischen Medium angegeben.

</dd> <dt>

[**CIM- \_ rebootaction**](cim-rebootaction.md)
</dt> <dd>

Die [**CIM \_ rebootaction**](cim-rebootaction.md) -Klasse verursacht einen Systemneustart, bei dem das Softwareelement installiert ist.

</dd> <dt>

[**CIM \_ redundant cycomponent**](cim-redundancycomponent.md)
</dt> <dd>

Die [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) -Klasse ordnet eine Redundanz Gruppe zu, die aus verwalteten Systemelementen besteht, und gibt an, dass die Elemente zusammen Redundanz bereitstellen. Alle Elemente, die in einer Redundanz Gruppe aggregiert werden, sollten Instanziierungen der gleichen Objektklasse sein.

</dd> <dt>

[**CIM- \_ RedundancyGroup**](cim-redundancygroup.md)
</dt> <dd>

Die [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) -Klasse stellt eine Auflistung verwalteter Systemelemente dar, die angibt, dass die aggregierten Komponenten zusammen Redundanz bereitstellen. Alle Elemente, die in einer Redundanz Gruppe aggregiert werden, sollten Instanziierungen der gleichen Objektklasse sein.

</dd> <dt>

[**CIM- \_ Kühlung**](cim-refrigeration.md)
</dt> <dd>

Die [**CIM- \_ kühl**](cim-refrigeration.md) Klasse stellt die Funktionen und die Verwaltung eines kühl Geräts dar.

</dd> <dt>

[**CIM \_ relatedstatistics**](cim-relatedstatistics.md)
</dt> <dd>

Die [**CIM \_ relatedstatistics**](cim-relatedstatistics.md) -Zuordnung stellt Hierarchien und Abhängigkeiten verwandter [**CIM \_ statisticalinformation**](cim-statisticalinformation.md) -Klassen dar.

</dd> <dt>

[**CIM- \_ remotefile System**](cim-remotefilesystem.md)
</dt> <dd>

Die [**CIM- \_ remotefile**](cim-remotefilesystem.md) System-Klasse stellt ein Remote Dateisystem dar, auf das über einen netzwerkbezogenen Dienst zugegriffen wird. In diesem Fall wird der Dateispeicher von einem Computer gehostet, der als Dateiserver fungiert.

</dd> <dt>

[**CIM \_ removedirectoriyaction**](cim-removedirectoryaction.md)
</dt> <dd>

Die [**CIM \_ removedirectoryaction**](cim-removedirectoryaction.md) -Klasse entfernt Verzeichnisse für Software Elemente.

</dd> <dt>

[**CIM- \_ removefileaction**](cim-removefileaction.md)
</dt> <dd>

Mit der [**CIM \_ removefileaction**](cim-removefileaction.md) -Klasse werden Dateien deinstalliert.

</dd> <dt>

[**CIM-Ersatz \_ Satz**](cim-replacementset.md)
</dt> <dd>

Die [**CIM \_ replacementset**](cim-replacementset.md) -Klasse aggregiert physische Elemente, die zusammen ersetzt werden müssen. Wenn Sie z. b. eine Speicherkarte austauschen, können die Komponenten Speicher-Chips auch entfernt und ersetzt werden. Oder diese Zuordnung kann verwendet werden, um einen Satz von Speicherchips zu ersetzen oder zu aktualisieren.

</dd> <dt>

[**CIM \_ resiwisonblock**](cim-residesonextent.md)
</dt> <dd>

Die [**CIM \_ residesonblock**](cim-residesonextent.md) -Klasse stellt eine Zuordnung zwischen einem Dateisystem und dem Speicherblock dar, in dem es sich befindet. In der Regel befindet sich ein Dateisystem auf einem logischen Datenträger.

</dd> <dt>

[**CIM- \_ runningos**](cim-runningos.md)
</dt> <dd>

Die [**CIM \_ runningos**](cim-runningos.md) -Klasse stellt das aktuell ausgeführte Betriebssystem dar. Höchstens ein Betriebssystem kann zu einem beliebigen Zeitpunkt auf einem Computersystem ausgeführt werden. das Computersystem ist möglicherweise nicht gestartet, oder sein Betriebssystem ist unbekannt.

</dd> <dt>

[**CIM \_ sapsapabhängigkeit**](cim-sapsapdependency.md)
</dt> <dd>

Die [**CIM \_ sapsapabhängigkeits**](cim-sapsapdependency.md) -Klasse ist eine Zuordnung zwischen zwei Dienst Zugriffs Punkten (SAPS), mit der angegeben wird, dass die zweite SAP-Komponente erforderlich ist, damit der erste SAP eine Verbindung mit dem Dienst herstellt.

</dd> <dt>

[**CIM- \_ Scanner**](cim-scanner.md)
</dt> <dd>

Der [**CIM- \_ Scanner**](cim-scanner.md) stellt die Funktionen und die Verwaltung des logischen Scanner-Geräts dar.

</dd> <dt>

[**CIM- \_ SCSIController**](cim-scsicontroller.md)
</dt> <dd>

Die [**CIM \_ SCSIController**](cim-scsicontroller.md) -Klasse stellt die Funktionen und die Verwaltung des logischen SCSI-Controller Geräts dar.

</dd> <dt>

[**CIM- \_ scsiinterface**](cim-scsiinterface.md)
</dt> <dd>

stellt eine [**CIM \_ controlledby**](cim-controlledby.md) -Beziehung dar, die angibt, auf welche Geräte über einen SCSI-Controller und die Zugriffs Eigenschaften zugegriffen wird.

</dd> <dt>

[**CIM- \_ Sensor**](cim-sensor.md)
</dt> <dd>

Die [**CIM- \_ Sensor**](cim-sensor.md) Klasse stellt ein Hardware Gerät dar, mit dem die Eigenschaften einer physischen Eigenschaft (z. b. die Temperatur-oder Spannungs Merkmale eines einheitlichen Computer Systems) gemessen werden können.

</dd> <dt>

[**CIM- \_ SerialController**](cim-serialcontroller.md)
</dt> <dd>

Die [**CIM \_ SerialController**](cim-serialcontroller.md) -Klasse stellt die Funktionen und die Verwaltung des logischen Geräts des seriellen Ports dar.

</dd> <dt>

[**CIM- \_ serialschnittstelle**](cim-serialinterface.md)
</dt> <dd>

Die [**CIM \_ serialinterface**](cim-serialinterface.md) -Klasse stellt eine [**CIM \_ controlledby**](cim-controlledby.md) -Beziehung dar, die angibt, auf welche Geräte über den seriellen Controller und die Eigenschaften des Zugriffs zugegriffen werden.

</dd> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> <dd>

Die [**CIM- \_ Dienst**](cim-service.md) Klasse stellt ein logisches Element dar, das Informationen zur Darstellung und Verwaltung der von einem Gerät oder einer Software Funktion bereitgestellten Funktionen enthält. Bei einem Dienst handelt es sich um ein allgemeines Objekt, um die Implementierung von Funktionen zu konfigurieren und zu verwalten. Es handelt sich nicht um die eigentliche Funktionalität.

</dd> <dt>

[**CIM \_ serviceaccessbysap**](cim-serviceaccessbysap.md)
</dt> <dd>

Die [**CIM \_ serviceaccessbysap**](cim-serviceaccessbysap.md) Association-Klasse stellt die Zugriffspunkte für einen Dienst dar. Beispielsweise kann auf einen Drucker über NetWare, Macintosh oder Windows-Dienst Zugriffspunkte (SAPS) zugegriffen werden, die potenziell auf unterschiedlichen Systemen gehostet werden.

</dd> <dt>

[**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md)
</dt> <dd>

Die [**CIM \_ serviceaccesspoint**](cim-serviceaccesspoint.md) -Klasse stellt die Möglichkeit dar, einen Dienst zu verwenden oder aufzurufen. Zugriffspunkte stellen Dienste dar, die von anderen Entitäten verwendet werden können.

</dd> <dt>

[**CIM \_ servicesapabhängigkeit**](cim-servicesapdependency.md)
</dt> <dd>

Die [**CIM \_ servicesapdepen-Klasse**](cim-servicesapdependency.md) stellt eine Zuordnung zwischen einem Dienst und einem Dienst Zugriffspunkt (SAP) dar, der angibt, dass der referenzierte SAP vom Dienst verwendet wird, um seine Funktionalität bereitzustellen.

</dd> <dt>

[**CIM \_ serviceserviceabhängigkeiten**](cim-serviceservicedependency.md)
</dt> <dd>

Die [**CIM \_ serviceservicedepen-Klasse**](cim-serviceservicedependency.md) stellt eine Zuordnung zwischen zwei Diensten dar.

</dd> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dd>

Die [**CIM- \_ Einstellungs**](cim-setting.md) Klasse stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.

</dd> <dt>

[**CIM- \_ settingcheck**](cim-settingcheck.md)
</dt> <dd>

Die [**CIM \_ settingcheck**](cim-settingcheck.md) -Klasse gibt Informationen an, die erforderlich sind, um eine bestimmte Einstellungsdatei für einen bestimmten Eintrag zu überprüfen, der einen Wert gleich dem angegebenen Wert enthält. Bei allen vergleichen wird die Groß-/Kleinschreibung nicht beachtet.

</dd> <dt>

[**CIM- \_ settingcontext**](cim-settingcontext.md)
</dt> <dd>

Die [**CIM \_ settingcontext**](cim-settingcontext.md) -Klasse ordnet Konfigurationsobjekte Einstellungs Objekten zu.

</dd> <dt>

[**CIM- \_ Slot**](cim-slot.md)
</dt> <dd>

Die [**CIM- \_ Slot**](cim-slot.md) -Klasse stellt Connectors dar, in die Pakete eingefügt werden.

</dd> <dt>

[**CIM \_ slotinslot**](cim-slotinslot.md)
</dt> <dd>

Die [**CIM \_ slotinslot**](cim-slotinslot.md) -Beziehung stellt die Fähigkeit eines speziellen Adapters dar, die vorhandene slotstruktur zu erweitern, um ansonsten inkompatible Karten zu ermöglichen, die an einem Frame oder einem hostingboard angeschlossen werden.

</dd> <dt>

[**CIM- \_ Softwareelement**](cim-softwareelement.md)
</dt> <dd>

Die [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Klasse zerlegt ein [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Objekt in einen Satz individuell verwaltbarer oder bereitstell barer Teile für eine bestimmte Plattform. Die Plattform eines Software Elements wird durch die zugrunde liegende Hardwarearchitektur und das Betriebssystem eindeutig identifiziert.

</dd> <dt>

[**CIM- \_ softwareelementactions**](cim-softwareelementactions.md)
</dt> <dd>

Die [**CIM- \_ softwareelementactions**](cim-softwareelementactions.md) -Zuordnung identifiziert die Aktionen für ein Softwareelement.

</dd> <dt>

[**CIM- \_ softwareelementchecks**](cim-softwareelementchecks.md)
</dt> <dd>

Die [**CIM- \_ softwareelementchecks**](cim-softwareelementchecks.md) -Zuordnungs Klasse verknüpft ein Softwareelement mit Bedingungs-oder Standortinformationen, die für eine Funktion erforderlich sind.

</dd> <dt>

[**CIM- \_ softwareelementversioncheck**](cim-softwareelementversioncheck.md)
</dt> <dd>

Die [**CIM \_ softwareelementversioncheck**](cim-softwareelementversioncheck.md) -Klasse stellt einen Typ von Softwareelement dar, der in der Umgebung vorhanden sein muss.

</dd> <dt>

[**CIM- \_ Softwarefeature**](cim-softwarefeature.md)
</dt> <dd>

Die [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) -Klasse stellt eine bestimmte Funktion oder Funktion eines Produkts oder Anwendungs Systems dar.

</dd> <dt>

[**CIM- \_ softwarefeaturesapimplementation**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

Die [**CIM- \_ softwarefeaturesapimplementation**](cim-softwarefeaturesapimplementation.md) -Klasse stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und der Art der Implementierung in Software dar.

</dd> <dt>

[**CIM \_ softwarefeatureserviceimplementation**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

Die [**CIM \_ softwarefeatureserviceimplementation**](cim-softwarefeatureserviceimplementation.md) -Klasse stellt eine Zuordnung zwischen einem Dienst und seiner Implementierung in Software dar.

</dd> <dt>

[**CIM- \_ softwarefeaturesoftwareelements**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

Die [**CIM- \_ softwarefeaturesoftwareelements**](cim-softwarefeaturesoftwareelements.md) -Zuordnung identifiziert die Software Elemente, die ein bestimmtes Software Feature bilden.

</dd> <dt>

[**CIM- \_ SpareGroup**](cim-sparegroup.md)
</dt> <dd>

Die [**CIM \_ SpareGroup**](cim-sparegroup.md) -Klasse wird von der [**CIM \_ redundant cygroup**](cim-redundancygroup.md) -Klasse abgeleitet und gibt an, dass mindestens eines der aggregierten Elemente geschont werden kann.

</dd> <dt>

[**CIM- \_ statisticalinformation**](cim-statisticalinformation.md)
</dt> <dd>

Die [**CIM \_ statisticalinformation**](cim-statisticalinformation.md) -Klasse ist eine Stamm Klasse für die beliebige Auflistung von statistischen Daten oder Metriken, die für ein oder mehrere verwaltete Systemelemente anwendbar sind.

</dd> <dt>

[**CIM- \_ Statistik**](cim-statistics.md)
</dt> <dd>

Die [**CIM \_ Statistics**](cim-statistics.md) -Klasse stellt eine Zuordnung dar, die verwaltete Systemelemente mit den statistischen Gruppen verknüpft, die für Sie gelten.

</dd> <dt>

[**CIM- \_ storagemängel**](cim-storagedefect.md)
</dt> <dd>

Die [**CIM \_ storagemängel**](cim-storagedefect.md) -Aggregation sammelt die Speicherfehler für einen Speicherblock.

</dd> <dt>

[**CIM- \_ storageerror**](cim-storageerror.md)
</dt> <dd>

Die [**CIM \_ storageerror**](cim-storageerror.md) -Klasse stellt Blöcke von Medien oder Speicherplatz dar, die aufgrund von Fehlern nicht verwendeter Speicher zugeordnet sind. Der Schlüssel der-Klasse ist die **StartingAddress** -Eigenschaft der Bytes, die fehlerhaft sind.

</dd> <dt>

[**CIM- \_ storageblock**](cim-storageextent.md)
</dt> <dd>

Die [**CIM \_ storageblock**](cim-storageextent.md) -Klasse stellt die Funktionen und die Verwaltung der verschiedenen Medien dar, die zum Speichern von Daten und zum Abrufen des Datenabrufs vorhanden sind. Diese übergeordnete Klasse kann die verschiedenen Komponenten von RAID (Hardware oder Software) oder einen logischen Bereich auf physischen Medien darstellen.

</dd> <dt>

[**CIM \_ storageredundancygroup**](cim-storageredundancygroup.md)
</dt> <dd>

Die [**CIM \_ storageredundancygroup**](cim-storageredundancygroup.md) -Klasse stellt Massenspeicher bezogene Redundanz Informationen dar.

</dd> <dt>

[**CIM- \_ supportaccess**](cim-supportaccess.md)
</dt> <dd>

Die [**CIM \_ supportaccess**](cim-supportaccess.md) -Klasse definiert, wie Sie Unterstützung für ein Produkt erhalten.

</dd> <dt>

[**CIM- \_ Swap-Papier**](cim-swapspacecheck.md)
</dt> <dd>

Die [**CIM \_ swapspacecheck**](cim-swapspacecheck.md) -Klasse gibt die Menge an Auslagerungs Bereich an, die auf dem System verfügbar sein muss.

</dd> <dt>

[**CIM- \_ System**](cim-system.md)
</dt> <dd>

Die [**CIM- \_ System**](cim-system.md) Klasse aggregiert einen Aufzähl baren Satz verwalteter System Elemente. Die Aggregation funktioniert als Ganzes funktionstüchtig. Innerhalb einer bestimmten Unterklasse des Systems gibt es eine klar definierte Liste der verwalteten System Element Klassen, deren Instanzen aggregiert werden müssen.

</dd> <dt>

[**CIM- \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dd>

eine Common Information Model (CIM)-Zuordnungs Klasse, mit der Beziehungen zwischen einem System und den verwalteten Systemelementen hergestellt werden, von denen es zusammengesetzt wird.

</dd> <dt>

[**CIM- \_ System Gerät**](cim-systemdevice.md)
</dt> <dd>

Die [**CIM- \_ SystemDevice**](cim-systemdevice.md) -Zuordnung stellt eine explizite Beziehung dar, in der logische Geräte von einem System aggregiert werden können.

</dd> <dt>

[**CIM- \_ Systemresource**](cim-systemresource.md)
</dt> <dd>

Die [**CIM- \_ systemressourcenklasse**](cim-systemresource.md) stellt eine Entität dar, die von BIOS verwaltet wird, oder ein Betriebssystem, das für die Verwendung durch Software und logische Geräte verfügbar ist.

</dd> <dt>

[**CIM- \_ Tachometer**](cim-tachometer.md)
</dt> <dd>

Die CIM-Klasse " [**\_ Tachometer**](cim-tachometer.md) " ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.

</dd> <dt>

[**CIM- \_ TapeDrive**](cim-tapedrive.md)
</dt> <dd>

Die [**CIM \_ TapeDrive**](cim-tapedrive.md) -Klasse stellt ein Bandlaufwerk auf dem System dar. Bandlaufwerke unterscheiden sich hauptsächlich darin, dass nur sequenziell auf Sie zugegriffen werden kann.

</dd> <dt>

[**CIM- \_ Temperatursensor**](cim-temperaturesensor.md)
</dt> <dd>

Die [**CIM- \_ Temperatursensor**](cim-temperaturesensor.md) Klasse ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden.

</dd> <dt>

[**CIM- \_ Thread**](cim-thread.md)
</dt> <dd>

Die [**CIM- \_ Thread**](cim-thread.md) Klasse stellt die Möglichkeit dar, gleichzeitig Einheiten eines Prozesses oder einer Aufgabe auszuführen. Ein Prozess kann über viele Threads verfügen, von denen jede für den Prozess schwach ist.

</dd> <dt>

[**CIM- \_ Verzeichnis Aktion**](cim-todirectoryaction.md)
</dt> <dd>

Die [**CIM \_**](cim-todirectoryaction.md) -Verzeichnis Verbindungs Zuordnung identifiziert das Zielverzeichnis für die Datei Aktion.

</dd> <dt>

[**CIM- \_ Verzeichnis Spezifikation**](cim-todirectoryspecification.md)
</dt> <dd>

Die [**CIM \_**](cim-todirectoryspecification.md) -Verzeichnisdienst Spezifikation identifiziert das Zielverzeichnis für die Datei Aktion.

</dd> <dt>

[**CIM- \_ uninterruptiblepowersupply**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

Die [**CIM-Klasse \_ uninterruptiblepowersupply**](cim-uninterruptiblepowersupply.md) stellt die Funktionen und die Verwaltung einer unterbrechungsfreien Stromversorgung (UPS) dar.

</dd> <dt>

[**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md)
</dt> <dd>

Die [**CIM \_ unitarycomputersystem**](cim-unitarycomputersystem.md) -Klasse stellt einen Desktop-, Mobil-, Netzwerk Computer-, Server-oder anderen Typ eines Computer Systems mit einem einzelnen Knoten dar.

</dd> <dt>

[**CIM-Start \_ Controller**](cim-usbcontroller.md)
</dt> <dd>

Die [**CIM \_**](cim-usbcontroller.md) -Klasse "Start Controller" stellt die Funktionen und die Verwaltung eines USB-Controllers dar.

</dd> <dt>

[**CIM-Start \_ Controller-controllerhashub**](cim-usbcontrollerhashub.md)
</dt> <dd>

Die [**CIM \_**](cim-usbcontrollerhashub.md) -Klasse "-Klasse" definiert die Hubs, die dem USB-Controller nachgelagert werden.

</dd> <dt>

[**CIM-Start \_ Gerät**](cim-usbdevice.md)
</dt> <dd>

Die [**CIM \_**](cim-usbdevice.md) -Klasse "-Klasse" stellt die Verwaltungsmerkmale eines USB-Geräts dar.

</dd> <dt>

[**CIM-Startseite \_**](cim-usbhub.md)
</dt> <dd>

Die [**CIM \_**](cim-usbhub.md) -Klasse "-Klasse" stellt die Funktionen und die Verwaltung eines USB-Hubs dar.

</dd> <dt>

[**CIM- \_ userdevice**](cim-userdevice.md)
</dt> <dd>

Die [**CIM- \_ userdevice**](cim-userdevice.md) -Klasse ist eine übergeordnete Klasse, von der andere Klassen, z. b. [**CIM- \_ Tastatur**](cim-keyboard.md) oder [**CIM \_ Desktopmonitor**](cim-desktopmonitor.md), abgeleitet werden. Benutzer Geräte sind logische Geräte, die es einem Computersystem ermöglichen, Daten einzugeben, anzuzeigen oder zu hören.

</dd> <dt>

[**CIM \_ versioncompatibilitycheck**](cim-versioncompatibilitycheck.md)
</dt> <dd>

Die [**CIM \_ versioncompatibilitycheck**](cim-versioncompatibilitycheck.md) -Klasse gibt an, ob es zulässig ist, den nächsten Zustand eines Software Elements zu erstellen.

</dd> <dt>

[**CIM- \_ videobioselements**](cim-videobioselement.md)
</dt> <dd>

Die [**CIM \_ videobioselfigure**](cim-videobioselement.md) -Klasse stellt die Software auf niedriger Ebene dar, die in nicht flüchtigen Speicher geladen wird und zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.

</dd> <dt>

[**CIM \_ videobiosfeature**](cim-videobiosfeature.md)
</dt> <dd>

Die [**CIM \_ videobiosfeature**](cim-videobiosfeature.md) -Klasse stellt die Funktionen der Low-Level-Software dar, die zum Konfigurieren und Zugreifen auf den Videocontroller und die Anzeige eines Computer Systems verwendet wird.

</dd> <dt>

[**CIM \_ videobiosfeaturevideobioselements**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

Die [**CIM \_ videobiosfeaturevideobioselements**](cim-videobiosfeaturevideobioselements.md) -Klasse ordnet eine Video-BIOS-Funktion und ihre aggregierten Video-BIOS-Elemente zu.

</dd> <dt>

[**CIM- \_ Videocontroller**](cim-videocontroller.md)
</dt> <dd>

Die [**CIM \_ Videocontroller**](cim-videocontroller.md) -Klasse stellt die Funktionen und die Verwaltung des Video Controllers dar.

</dd> <dt>

[**CIM- \_ videocontrollerresolution**](cim-videocontrollerresolution.md)
</dt> <dd>

Die [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Klasse stellt die verschiedenen Video Modi dar, die von einem Videocontroller unterstützt werden können.

</dd> <dt>

[**CIM- \_ videosetting**](cim-videosetting.md)
</dt> <dd>

Die [**CIM- \_ videosetting**](cim-videosetting.md) -Klasse ordnet das [**CIM \_ videocontrollerresolution**](cim-videocontrollerresolution.md) -Einstellungs Objekt dem Controller zu, auf den es angewendet wird.

</dd> <dt>

[**CIM- \_ VolatileStorage**](cim-volatilestorage.md)
</dt> <dd>

Die [**CIM \_ VolatileStorage**](cim-volatilestorage.md) -Klasse stellt die Funktionen und die Verwaltung von flüchtigem Speicher dar.

</dd> <dt>

[**CIM- \_ Temperatursensor**](cim-voltagesensor.md)
</dt> <dd>

Die CIM-Klasse " [**\_ VoltageSensor**](cim-voltagesensor.md) " ist für die Abwärtskompatibilität mit früheren CIM-Schema Definitionen vorhanden. Mit Ergänzungen der [**CIM- \_ Sensor**](cim-sensor.md) -und [**CIM- \_ numericsensor**](cim-numericsensor.md) -Klassen in Version 2,2 ist es nicht mehr erforderlich.

</dd> <dt>

[**CIM- \_ volumeset**](cim-volumeset.md)
</dt> <dd>

Die [**CIM \_ volumeset**](cim-volumeset.md) -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, die der Betriebsumgebung zum Lesen und Schreiben von Benutzerdaten präsentiert werden.

</dd> <dt>

[**CIM- \_ Wurm Laufwerk**](cim-wormdrive.md)
</dt> <dd>

Die CIM-Klasse " [**\_ Wormdrive**](cim-wormdrive.md) " stellt die Funktionen und die Verwaltung eines Wurm Laufwerks dar, einen Untertyp des Medien Zugriffs Geräts.

</dd> </dl>

 

 
