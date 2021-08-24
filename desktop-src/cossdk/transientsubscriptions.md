---
description: Enthält ein -Objekt für jedes vorübergehende Abonnement. Vorübergehende Abonnements können während der Ausführung von Objektinstanzen erstellt werden und verschwinden, wenn das Objekt zerstört wird.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: TransientSubscriptions-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5053a4fd488ed38a637b4296f94caf20887f3ed924ae6d11b8f6a242669eccad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853930"
---
# <a name="transientsubscriptions-collection"></a>TransientSubscriptions-Auflistung

Enthält ein -Objekt für jedes vorübergehende Abonnement. Vorübergehende Abonnements können während der Ausführung von Objektinstanzen erstellt werden und verschwinden, wenn das Objekt zerstört wird.

Diese Sammlung unterstützt die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **TransientSubscriptions-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientPublisherProperties**](transientpublisherproperties.md)
-   [**TransientSubscriberProperties**](transientsubscriberproperties.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Beschreibung](#description)
-   [Aktiviert](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [ID](#transientsubscriptions-collection)
-   [Interfaceid](#interfaceid)
-   [MethodName](#methodname)
-   [Name](#methodname)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [SubscriberInterface](#subscriberinterface)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|-------------------------------------|
| Beschreibung    | Eine Beschreibung für das Abonnement. |
| Zugriff         | ReadWrite                           |
| type           | String                              |
| Standard        | ""                                  |
| Mindestsystem | Windows 2000                        |



 

### <a name="enabled"></a>Aktiviert



| Eingabe | Wert |
|----------------|----------------------------------------------------------|
| Beschreibung    | Gibt an, ob das Abonnement derzeit aktiviert ist. |
| Zugriff         | ReadWrite                                                |
| Typ           | Bool                                                     |
| Standard        | Richtig                                                     |
| Mindestsystem | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Beim Abonnieren einer Ereignisklasse wird verwendet, um die GUID der Partitions-ID mit der Ereignisklasse zu darstellen. Beim Abonnieren von Ereignisklassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder einer anderen Partition zu abonnieren. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                          |
| type           | String                                                                                                                                                                                                                                             |
| Standard        | NULL                                                                                                                                                                                                                                               |
| Mindestsystem | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------|
| Beschreibung    | Die CLSID für die Ereignisklasse. Sie können eine EventCLSID oder eine PublisherID angeben, aber nicht beides. |
| Zugriff         | WriteOnce                                                                                    |
| type           | String                                                                                       |
| Standard        | Nicht zutreffend                                                                                          |
| Mindestsystem | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine Zeichenfolge, die die Filterkriterien angibt. Kann eine CLSID für eine [**PublisherFilter-Klasse**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) sein. |
| Zugriff         | ReadWrite                                                                                                            |
| type           | String                                                                                                               |
| Standard        | Nicht zutreffend                                                                                                                  |
| Mindestsystem | Windows 2000                                                                                                         |



 

### <a name="id"></a>ID



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bezeichner für das Abonnement. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                        |
| type           | String                                                                                                                                                           |
| Standard        | <Generated>                                                                                                                                                |
| Mindestsystem | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>Interfaceid



| Eingabe | Wert |
|----------------|----------------------------------|
| Beschreibung    | IID für die abonnierte Schnittstelle. |
| Zugriff         | WriteOnce                        |
| type           | String                           |
| Standard        | Nicht zutreffend                              |
| Mindestsystem | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Eingabe | Wert |
|----------------|----------------------------------------------|
| Beschreibung    | Methode für die Schnittstelle, die abonniert wird. |
| Zugriff         | ReadWrite                                    |
| type           | String                                       |
| Standard        | Nicht zutreffend                                          |
| Mindestsystem | Windows 2000                                 |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name für das Abonnement. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                 |
| Standard        | "Neues Abonnement"                                                                                                                                                                                                                     |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>PerUser



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob das Abonnement nur für einen bestimmten Benutzer gilt, der durch die UserName-Eigenschaft dargestellt wird. |
| Zugriff         | ReadWrite                                                                                               |
| Typ           | Bool                                                                                                    |
| Standard        | Falsch                                                                                                   |
| Mindestsystem | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------|
| Beschreibung    | ID für den Herausgeber. Sie können eine EventCLSID oder eine PublisherID angeben, aber nicht beides. |
| Zugriff         | WriteOnce                                                                           |
| type           | String                                                                              |
| Standard        | ""                                                                                  |
| Mindestsystem | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>SubscriberInterface



| Eingabe | Wert |
|----------------|------------------------------------------|
| Beschreibung    | Ein Zeiger auf die Schnittstelle des Abonnenten. |
| Zugriff         | ReadWrite                                |
| Typ           | Variant                                  |
| Standard        | Nicht zutreffend                                      |
| Mindestsystem | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Beim Abonnieren einer Ereignisklasse in derselben Partition wird verwendet, um die GUID der Partitions-ID des Abonnenten darzustellen. Beim Abonnieren von Ereignisklassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder einer anderen Partition zu abonnieren. |
| Zugriff         | WriteOnce                                                                                                                                                                                                                                                       |
| type           | String                                                                                                                                                                                                                                                          |
| Standard        | <Generated>                                                                                                                                                                                                                                               |
| Mindestsystem | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------|
| Beschreibung    | Der Name des Benutzers, für den das Abonnement gilt, wenn PerUser true ist. |
| Zugriff         | ReadWrite                                                               |
| type           | String                                                                  |
| Standard        | Nicht zutreffend                                                                     |
| Mindestsystem | Windows 2000                                                            |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
