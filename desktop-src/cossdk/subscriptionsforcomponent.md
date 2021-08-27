---
description: Enthält ein -Objekt für jedes Abonnement für die übergeordnete Components-Auflistung.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: SubscriptionsForComponent-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8c07162fc20788545b38b8fae4be245b9a1ebbff
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886199"
---
# <a name="subscriptionsforcomponent-collection"></a>SubscriptionsForComponent-Sammlung

Enthält ein -Objekt für jedes Abonnement für die übergeordnete [**Components-Auflistung.**](components.md)

Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **SubscriptionsForComponent-Auflistung erbt** von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**PublisherProperties**](publisherproperties.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**SubscriberProperties**](subscriberproperties.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Komponenten**](components.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Beschreibung](#description)
-   [Aktiviert](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [ID](#subscriptionsforcomponent-collection)
-   [Interfaceid](#interfaceid)
-   [MachineName](#machinename)
-   [MethodName](#methodname)
-   [Name](#machinename)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [In Warteschlange](#queued)
-   [SubscriberMoniker](#subscribermoniker)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|-------------------------------------|
| Beschreibung    | Eine Beschreibung für das Abonnement. |
| Access         | ReadWrite                           |
| type           | String                              |
| Standard        | ""                                  |
| Mindestsystem | Windows 2000                        |



 

### <a name="enabled"></a>Aktiviert



| Eingabe | Wert |
|----------------|----------------------------------------------------------|
| Beschreibung    | Gibt an, ob das Abonnement derzeit aktiviert ist. |
| Access         | ReadWrite                                                |
| Typ           | Bool                                                     |
| Standard        | True                                                     |
| Mindestsystem | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Beim Abonnieren einer Ereignisklasse wird verwendet, um die GUID der Partitions-ID darzustellen, die die Ereignisklasse enthält. Beim Abonnieren von Ereignisklassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder einer anderen Partition zu abonnieren. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| type           | String                                                                                                                                                                                                                                             |
| Standard        | NULL                                                                                                                                                                                                                                               |
| Mindestsystem | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------|
| Beschreibung    | Die CLSID für die Ereignisklasse. Sie können eine EventCLSID oder eine PublisherID angeben, aber nicht beides. |
| Access         | WriteOnce                                                                                    |
| type           | String                                                                                       |
| Standard        | –                                                                                          |
| Mindestsystem | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine Zeichenfolge, die die Filterkriterien angibt. Kann eine CLSID für eine [**PublisherFilter-Klasse**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) sein. |
| Access         | ReadWrite                                                                                                        |
| type           | String                                                                                                           |
| Standard        | –                                                                                                              |
| Mindestsystem | Windows 2000                                                                                                     |



 

### <a name="id"></a>ID



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bezeichner für das Abonnement. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                        |
| type           | String                                                                                                                                                           |
| Standard        | &lt;Generiert&gt;                                                                                                                                                |
| Mindestsystem | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>Interfaceid



| Eingabe | Wert |
|----------------|------------------------------------------|
| Beschreibung    | Die IID für die abonnierte Schnittstelle. |
| Access         | ReadWrite                                |
| type           | String                                   |
| Standard        | –                                      |
| Mindestsystem | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------|
| Beschreibung    | Ein Remotecomputername für Abonnements von Ereignisklassen auf einem Remotecomputer. |
| Access         | ReadWrite                                                                       |
| type           | String                                                                          |
| Standard        | ""                                                                              |
| Mindestsystem | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| Eingabe | Wert |
|----------------|----------------------------------------------|
| Beschreibung    | Methode für die Schnittstelle, die abonniert wird. |
| Access         | ReadWrite                                    |
| type           | String                                       |
| Standard        | –                                          |
| Mindestsystem | Windows 2000                                 |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Name für das Abonnement. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| type           | String                                                                                                                                                                                                                             |
| Standard        | "Neues Abonnement"                                                                                                                                                                                                                 |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>PerUser



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob das Abonnement nur für einen bestimmten Benutzer gilt: UserName. |
| Access         | ReadWrite                                                                   |
| Typ           | Bool                                                                        |
| Standard        | Falsch                                                                       |
| Mindestsystem | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| Beschreibung    | Die ID für den Herausgeber. Sie können eine EventCLSID oder eine PublisherID angeben, aber nicht beides. |
| Access         | WriteOnce                                                                               |
| type           | String                                                                                  |
| Standard        | ""                                                                                      |
| Mindestsystem | Windows 2000                                                                            |



 

### <a name="queued"></a>In Warteschlange



| Eingabe | Wert |
|----------------|-----------------------------------------------|
| Beschreibung    | Gibt an, ob das Abonnement in die Warteschlange gestellt wird. |
| Access         | ReadWrite                                     |
| Typ           | Bool                                          |
| Standard        | Falsch                                         |
| Mindestsystem | Windows 2000                                  |



 

### <a name="subscribermoniker"></a>SubscriberMoniker



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Ein Moniker für einen Abonnenten, der als In Warteschlange gekennzeichnet ist. Ein Standardwert wird generiert, wenn Queued anfänglich auf True festgelegt ist. |
| Access         | ReadWrite                                                                                                       |
| type           | String                                                                                                          |
| Standard        | –                                                                                                             |
| Mindestsystem | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Beim Abonnieren einer Ereignisklasse in derselben Partition wird verwendet, um die GUID der Partitions-ID des Abonnenten zu darstellen. Beim Abonnieren von Ereignisklassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder einer anderen Partition zu abonnieren. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| type           | String                                                                                                                                                                                                                                                          |
| Standard        | &lt;Generiert&gt;                                                                                                                                                                                                                                               |
| Mindestsystem | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------|
| Beschreibung    | Der Name des Benutzers, für den das Abonnement gilt, wenn PerUser true ist. |
| Access         | ReadWrite                                                                |
| type           | String                                                                   |
| Standard        | –                                                                      |
| Mindestsystem | Windows 2000                                                             |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
