---
description: Die COM+-Verwaltungssammlungen dienen zum Speichern und Organisieren von Konfigurationsdaten, die im COM+-Katalog gespeichert sind.
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: COM+-Verwaltungssammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc19ff14959c151dc5736fb4a52c5346d0f5a30b6565551aca2f0edb3cee61b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308441"
---
# <a name="com-administration-collections"></a>COM+-Verwaltungssammlungen

Die COM+-Verwaltungssammlungen dienen zum Speichern und Organisieren von Konfigurationsdaten, die im COM+-Katalog gespeichert sind. Die Sammlungen entsprechen Ordnern in der Konsolenstruktur des Verwaltungstool Komponentendienste. Sie können mithilfe der COM+-Verwaltungsobjekte und -Schnittstellen auf diese Sammlungen zugreifen.

Sie initiieren die programmgesteuerte Verwaltung mithilfe von Objekten, die aus der [**COMAdminCatalog-Klasse**](comadmincatalog.md) erstellt wurden. Sie stellen alle Sammlungen im Katalog mithilfe von Objekten dar, die aus der [**COMAdminCatalogCollection-Klasse**](comadmincatalogcollection.md) erstellt wurden, und Sie stellen Elemente in Auflistungen mithilfe von Objekten dar, die aus der [**COMAdminCatalogObject-Klasse**](comadmincatalogobject.md) erstellt wurden.

Die Elemente in einer bestimmten Auflistung machen einen konsistenten Satz von Eigenschaften verfügbar. Beispielsweise stellt jedes Element in der [**Components-Auflistung**](components.md) eine Komponente dar, und die Elemente in der **Components-Auflistung** machen die gleichen Eigenschaften verfügbar, die zum Konfigurieren einer Komponente verwendet wurden. Auf diese Eigenschaften kann mithilfe der [**COMAdminCatalogObject-Klasse zugegriffen**](comadmincatalogobject.md) werden.

> [!Note]  
> Eigenschaften mit WriteOnce-Zugriff sind ReadWrite, während die [**Add-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) verwendet wird, und sind anschließend ReadOnly.

 

Eine Einführung in die programmgesteuerte Verwaltung von COM+ finden Sie unter [Automatisieren der COM+-Verwaltung.](automating-com--administration.md)

## <a name="collection-hierarchy"></a>Sammlungshierarchie

Die folgende Abbildung veranschaulicht die Beziehungen zwischen den Auflistungen. Die Auflistungen ganz links (in weißen und grauen Feldern) sind Sammlungen der obersten Ebene, auf die durch Aufrufen der [**GetCollection-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) eines Objekts zugegriffen wird, das aus der [**COMAdminCatalog-Klasse erstellt**](comadmincatalog.md) wurde. Auf die verbleibenden Auflistungen (in gelben Feldern) kann nur über die übergeordnete Auflistung zugegriffen werden, indem die [**GetCollection-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) des [**COMAdminCatalogCollection-Objekts**](comadmincatalogcollection.md) aufgerufen wird, das das übergeordnete Element darstellt. Die Pfeile zeigen von einer übergeordneten Auflistung auf die untergeordneten Auflistungen.

![Diagramm, das die Beziehungen zwischen den Auflistungen zeigt.](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

Die folgenden vier Auflistungen sind in der Abbildung nicht dargestellt: [**ErrorInfo**](errorinfo.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md)und [**Root**](root.md). Die **ErrorInfo-Sammlung** ist ein untergeordnetes Element jeder Sammlung in der Abbildung, mit Ausnahme von [**InprocServers**](inprocservers.md) und [**WOWInprocServers**](wowinprocservers.md) (in grauen Feldern). Die **PropertyInfo-** **und RelatedCollectionInfo-Auflistungen** sind children jeder Auflistung. Die **Root-Auflistung** ist eine Auflistung der obersten Ebene, die allen anderen Auflistungen der obersten Ebene über-übergeordnete Auflistungen ist. Es ist jedoch nicht erforderlich, vor dem Zugriff auf andere Sammlungen der obersten Ebene auf die **Stammsammlung** zu zugreifen.

## <a name="comadmin-library"></a>COMAdmin-Bibliothek

Die folgenden Sammlungen werden von der COMAdmin-Bibliothek unterstützt.



| Sammlung                                                             | Beschreibung                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | Enthält eine Liste der Server im Anwendungscluster.                                                                                            |
| [**ApplicationInstances**](applicationinstances.md)                   | Enthält ein -Objekt für jede Instanz einer ausgeführten COM+-Anwendung.                                                                                   |
| [**Anwendungen**](applications.md)                                   | Enthält ein -Objekt für jede COM+-Anwendung, die auf dem lokalen Computer installiert ist.                                                                         |
| [**Komponenten**](components.md)                                       | Enthält ein -Objekt für jede Komponente in der Anwendung, mit der sie verknüpft ist.                                                                      |
| [**ComputerList**](computerlist.md)                                   | Enthält eine Liste der Computer, die sich im Ordner **Computer** des Verwaltungstool Komponentendienste befinden.                                     |
| [**DCOMProtocols**](dcomprotocols.md)                                 | Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen. Sie enthält ein -Objekt für jedes Protokoll.                                                         |
| [**ErrorInfo**](errorinfo.md)                                         | Ruft erweiterte Fehlerinformationen zu Methoden ab, die mehrere Objekte behandeln.                                                               |
| [**EventClassesForIID**](eventclassesforiid.md)                       | Ruft Informationen zu Ereignisklassen ab.                                                                                                        |
| [**FilesForImport**](filesforimport.md)                               | Ruft Informationen zu einer Anwendung, die importiert werden kann, aus der MSI-Datei ab.                                                                    |
| [**InprocServers**](inprocservers.md)                                 | Enthält eine Liste der Prozessserver, die beim System registriert sind. Sie enthält ein -Objekt für jede Komponente.                                       |
| [**InterfacesForComponent**](interfacesforcomponent.md)               | Enthält ein -Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.                                                    |
| [**LegacyComponents**](legacycomponents.md)                           | Enthält ein -Objekt für jede nicht konfigurierte Komponente in der Anwendung, mit der sie verknüpft ist.                                                         |
| [**LegacyServers**](legacyservers.md)                                 | Identisch mit der [**InprocServers-Auflistung,**](inprocservers.md) mit dem Ausnahme, dass diese Sammlung auch lokale Server enthält.                           |
| [**LocalComputer**](localcomputer.md)                                 | Enthält ein einzelnes -Objekt, das Einstellungsinformationen auf Computerebene für den Computer enthält, auf den Sie zugreifen.                             |
| [**MethodsForInterface**](methodsforinterface.md)                     | Enthält ein -Objekt für jede Methode auf der Schnittstelle, mit der die Auflistung verknüpft ist.                                                               |
| [**Partitionen**](partitions.md)                                       | Wird verwendet, um die anwendungen anzugeben, die in jeder Partition enthalten sind.                                                                                         |
| [**PartitionUsers**](partitionusers.md)                               | Wird verwendet, um die in jeder Partition enthaltenen Benutzer anzugeben.                                                                                                |
| [**Propertyinfo**](propertyinfo.md)                                   | Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden.                                                                      |
| [**PublisherProperties**](publisherproperties.md)                     | Enthält ein -Objekt für jede Herausgebereigenschaft für die übergeordnete [**SubscriptionsForComponent-Auflistung.**](subscriptionsforcomponent.md)              |
| [**RelatedCollectionInfo**](relatedcollectioninfo.md)                 | Ruft Informationen zu anderen Auflistungen ab, die mit der Auflistung verknüpft sind, aus der sie aufgerufen wird.                                                      |
| [**Rollen**](roles.md)                                                 | Enthält ein -Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der sie verknüpft ist.                                                                  |
| [**RolesForComponent**](rolesforcomponent.md)                         | Enthält ein -Objekt für jede Rolle, die der Komponente zugewiesen ist, mit der die Auflistung verknüpft ist.                                                        |
| [**RolesForInterface**](rolesforinterface.md)                         | Enthält ein -Objekt für jede Rolle, die der Schnittstelle zugewiesen ist, mit der die Auflistung verknüpft ist.                                                        |
| [**RolesForMethod**](rolesformethod.md)                               | Enthält ein -Objekt für jede Rolle, die der Methode zugewiesen ist, mit der die Auflistung verknüpft ist.                                                           |
| [**RolesForPartition**](rolesforpartition.md)                         | Enthält ein -Objekt für jede Rolle, die der Partition zugewiesen ist, mit der die Auflistung verknüpft ist.                                                        |
| [**wurzel**](root.md)                                                   | Enthält die Auflistungen der obersten Ebene im Katalog.                                                                                                    |
| [**SubscriberProperties**](subscriberproperties.md)                   | Enthält ein -Objekt für jede Abonnenteneigenschaft für die übergeordnete [**SubscriptionsForComponent-Auflistung.**](subscriptionsforcomponent.md)             |
| [**SubscriptionsForComponent**](subscriptionsforcomponent.md)         | Enthält ein -Objekt für jedes Abonnement für die übergeordnete [**Components-Auflistung.**](components.md)                                                  |
| [**TransientPublisherProperties**](transientpublisherproperties.md)   | Enthält ein -Objekt für jede Herausgebereigenschaft für die übergeordnete [**TransientSubscriptions-Auflistung.**](transientsubscriptions.md)                    |
| [**TransientSubscriberProperties**](transientsubscriberproperties.md) | Enthält ein -Objekt für jede Abonnenteneigenschaft für die übergeordnete [**TransientSubscriptions-Auflistung.**](transientsubscriptions.md)                   |
| [**TransientSubscriptions**](transientsubscriptions.md)               | Enthält ein -Objekt für jedes vorübergehende Abonnement.                                                                                                   |
| [**UsersInPartitionRole**](usersinpartitionrole.md)                   | Enthält ein -Objekt für jeden Benutzer in der Partitionsrolle, mit der die Auflistung verknüpft ist.                                                            |
| [**UsersInRole**](usersinrole.md)                                     | Enthält ein -Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.                                                                      |
| [**WOWInprocServers**](wowinprocservers.md)                           | Enthält eine Liste der Prozessserver, die beim System für 32-Bit-Komponenten auf 64-Bit-Computern registriert sind.                                       |
| [**WOWLegacyServers**](wowlegacyservers.md)                           | Identisch mit der [**LegacyServers-Sammlung,**](legacyservers.md) außer dass diese Auflistung aus der 32-Bit-Registrierung auf 64-Bit-Computern gezeichnet wird. |



 

 

 



