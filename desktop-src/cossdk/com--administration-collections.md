---
description: Die com+-Verwaltungs Sammlungen dienen zum Speichern und organisieren von Konfigurationsdaten, die im com+-Katalog gespeichert sind.
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: Com+-Verwaltungs Sammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb49ecd382e5a5a570e3e479714ad905a5eaf5f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104555633"
---
# <a name="com-administration-collections"></a>Com+-Verwaltungs Sammlungen

Die com+-Verwaltungs Sammlungen dienen zum Speichern und organisieren von Konfigurationsdaten, die im com+-Katalog gespeichert sind. Die Sammlungen entsprechen Ordnern in der Konsolen Struktur des Verwaltungs Tools Komponenten Dienste. Sie können auf diese Sammlungen zugreifen, indem Sie die com+-Verwaltungs Objekte und-Schnittstellen verwenden.

Sie initiieren die programmgesteuerte Verwaltung mithilfe von Objekten, die aus der [**comadmincatalog**](comadmincatalog.md) -Klasse erstellt wurden. Sie stellen alle Auflistungen im Katalog mithilfe von Objekten dar, die aus der [**comadmincatalogcollection**](comadmincatalogcollection.md) -Klasse erstellt wurden, und stellen Elemente in Auflistungen mithilfe von Objekten dar, die aus der [**COMAdminCatalogObject**](comadmincatalogobject.md)

Die Elemente in einer bestimmten Sammlung machen einen konsistenten Satz von Eigenschaften verfügbar. Beispielsweise stellt jedes Element in der [**Komponenten**](components.md) Auflistung eine Komponente dar, und die Elemente in der **Komponenten** Auflistung machen dieselben Eigenschaften verfügbar, die zum Konfigurieren einer Komponente verwendet werden. Auf diese Eigenschaften kann mit der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse zugegriffen werden.

> [!Note]  
> Eigenschaften mit dem Zugriff auf den Schreibzugriff sind beim Verwenden der [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -Methode vor der Verwendung von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) schreibgeschützt und sind danach schreibgeschützt.

 

Eine Einführung in die programmgesteuerte Verwaltung von com+ finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).

## <a name="collection-hierarchy"></a>Sammlungs Hierarchie

In der folgenden Abbildung werden die Beziehungen zwischen den Auflistungen veranschaulicht. Die Auflistungen in der äußersten linken Ecke (in weißen und grauen Feldern) sind Auflistungen der obersten Ebene, auf die durch Aufrufen der [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode eines Objekts, das aus der [**comadmincatalog**](comadmincatalog.md) -Klasse erstellt wurde, zugegriffen wird. Auf die restlichen Auflistungen (in gelben Feldern) kann nur über die übergeordnete Sammlung zugegriffen werden, indem die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts aufgerufen wird, das das übergeordnete Element darstellt. Die Pfeile zeigen von einer übergeordneten Auflistung zu ihren untergeordneten Auflistungen.

![Diagramm, das die Beziehungen zwischen den Sammlungen anzeigt.](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

Die folgenden vier Auflistungen sind in der Abbildung nicht dargestellt: [**errorInfo**](errorinfo.md), [**PropertyInfo**](propertyinfo.md), [**relatedcollectioninfo**](relatedcollectioninfo.md)und [**root**](root.md). Die **errorInfo** -Auflistung ist ein untergeordnetes Element jeder Sammlung in der Abbildung mit Ausnahme von " [**inprocservers**](inprocservers.md) " und " [**wowinprocservers**](wowinprocservers.md) " (in grauen Feldern). Die **PropertyInfo** -und **relatedcollectioninfo** -Auflistungen sind untergeordnete Elemente jeder Auflistung. Die Stamm Auflistung ist eine **Auflistung der obersten** Ebene, die allen anderen Auflistungen der obersten Ebene übergeordnet ist. Es ist jedoch nicht erforderlich, **auf die Stamm** Auflistung zuzugreifen, bevor Sie auf andere Auflistungen der obersten Ebene zugreifen.

## <a name="comadmin-library"></a>COMAdmin-Bibliothek

Die folgenden Sammlungen werden von der COMAdmin-Bibliothek unterstützt.



| Sammlung                                                             | BESCHREIBUNG                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | Enthält eine Liste der Server im Anwendungs Cluster.                                                                                            |
| [**ApplicationInstance**](applicationinstances.md)                   | Enthält ein-Objekt für jede Instanz einer laufenden com+-Anwendung.                                                                                   |
| [**Anwendungen**](applications.md)                                   | Enthält ein-Objekt für jede com+-Anwendung, die auf dem lokalen Computer installiert ist.                                                                         |
| [**Komponenten**](components.md)                                       | Enthält ein-Objekt für jede Komponente in der Anwendung, mit der es verknüpft ist.                                                                      |
| [**Computer Liste**](computerlist.md)                                   | Enthält eine Liste der Computer, die sich im Ordner **Computer** des Verwaltungs Tools Komponenten Dienste befinden.                                     |
| [**Dcomprotokolle**](dcomprotocols.md)                                 | Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen. Sie enthält ein Objekt für jedes Protokoll.                                                         |
| [**ErrorInfo**](errorinfo.md)                                         | Ruft erweiterte Fehlerinformationen zu Methoden ab, die mehrere-Objekte betreffen.                                                               |
| [**Eventclassesforiid**](eventclassesforiid.md)                       | Ruft Informationen zu Ereignis Klassen ab.                                                                                                        |
| [**Filesforimport**](filesforimport.md)                               | Ruft Informationen zu einer Anwendung, die importiert werden kann, aus der zugehörigen MSI-Datei ab.                                                                    |
| [**Inprocservers**](inprocservers.md)                                 | Enthält eine Liste der in-Process-Server, die beim System registriert sind. Sie enthält ein-Objekt für jede Komponente.                                       |
| [**Interfakesforcomponent**](interfacesforcomponent.md)               | Enthält ein-Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.                                                    |
| [**Legacycomponents**](legacycomponents.md)                           | Enthält ein-Objekt für jede nicht konfigurierte Komponente in der Anwendung, mit der es verknüpft ist.                                                         |
| [**Legacyserver**](legacyservers.md)                                 | Identisch mit der [**inprocservers**](inprocservers.md) -Auflistung, mit der Ausnahme, dass diese Sammlung auch lokale Server enthält.                           |
| [**LocalComputer**](localcomputer.md)                                 | Enthält ein einzelnes Objekt, das Einstellungs Informationen auf Computer Ebene für den Computer enthält, auf den Sie zugreifen.                             |
| [**Methodsforinterface**](methodsforinterface.md)                     | Enthält ein-Objekt für jede Methode in der Schnittstelle, mit der die Auflistung verknüpft ist.                                                               |
| [**Partitionen**](partitions.md)                                       | Dient zum Angeben der Anwendungen, die in den einzelnen Partitionen enthalten sind.                                                                                         |
| [**Partitionusers**](partitionusers.md)                               | Wird verwendet, um die in jeder Partition enthaltenen Benutzer anzugeben.                                                                                                |
| [**PropertyInfo**](propertyinfo.md)                                   | Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden.                                                                      |
| [**Publisherproperties**](publisherproperties.md)                     | Enthält ein-Objekt für jede Herausgeber Eigenschaft für die [**übergeordnete Index**](subscriptionsforcomponent.md) Index Auflistung.              |
| [**Relatedcollectioninfo**](relatedcollectioninfo.md)                 | Ruft Informationen zu anderen Auflistungen ab, die sich auf die Auflistung beziehen, von der Sie aufgerufen wird.                                                      |
| [**Rollen**](roles.md)                                                 | Enthält ein-Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der es verknüpft ist.                                                                  |
| [**Rolesforcomponent**](rolesforcomponent.md)                         | Enthält ein-Objekt für jede Rolle, die der Komponente zugeordnet ist, mit der die Auflistung verknüpft ist.                                                        |
| [**Rolesforinterface**](rolesforinterface.md)                         | Enthält ein-Objekt für jede Rolle, die der-Schnittstelle zugewiesen ist, mit der die Auflistung verknüpft ist.                                                        |
| [**Rolesformethod**](rolesformethod.md)                               | Enthält ein-Objekt für jede Rolle, die der Methode zugewiesen ist, mit der die Auflistung verknüpft ist.                                                           |
| [**Rolesforpartition**](rolesforpartition.md)                         | Enthält ein-Objekt für jede Rolle, die der Partition zugewiesen ist, mit der die Auflistung verknüpft ist.                                                        |
| [**Fasst**](root.md)                                                   | Enthält die Auflistungen der obersten Ebene im Katalog.                                                                                                    |
| [**Abonnement Eigenschaften**](subscriberproperties.md)                   | Enthält ein-Objekt für jede Abonnenten Eigenschaft für die [**übergeordnete Index**](subscriptionsforcomponent.md) Index Auflistung.             |
| [**Abonnement forcomponent**](subscriptionsforcomponent.md)         | Enthält ein-Objekt für jedes Abonnement für die Auflistung der übergeordneten [**Komponenten**](components.md) .                                                  |
| [**Transientpublisherproperties**](transientpublisherproperties.md)   | Enthält ein-Objekt für jede Verleger Eigenschaft für die übergeordnete [**transientabonnements**](transientsubscriptions.md) -Auflistung.                    |
| [**Transientabonberproperties**](transientsubscriberproperties.md) | Enthält ein-Objekt für jede Abonnenten Eigenschaft für die übergeordnete [**transientabonnements**](transientsubscriptions.md) -Auflistung.                   |
| [**Transientabonnements**](transientsubscriptions.md)               | Enthält ein-Objekt für jedes vorübergehende Abonnement.                                                                                                   |
| [**Usersinpartitionrole**](usersinpartitionrole.md)                   | Enthält ein-Objekt für jeden Benutzer in der Partitions Rolle, mit der die Auflistung verknüpft ist.                                                            |
| [**Usersinrole**](usersinrole.md)                                     | Enthält ein-Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.                                                                      |
| [**Wowinprocservers**](wowinprocservers.md)                           | Enthält eine Liste der in-Process-Server, die für 32-Bit-Komponenten auf 64-Bit-Computern beim System registriert sind.                                       |
| [**Wowlegacyservers**](wowlegacyservers.md)                           | Identisch mit der [**Legacyservers**](legacyservers.md) -Auflistung, mit der Ausnahme, dass diese Auflistung aus der 32-Bit-Registrierung auf 64-Bit-Computern gezeichnet wird. |



 

 

 



