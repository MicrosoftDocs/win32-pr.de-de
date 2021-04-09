---
description: Enthält ein-Objekt für jedes vorübergehende Abonnement. Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Transientabonnements-Auflistung
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
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861284"
---
# <a name="transientsubscriptions-collection"></a>Transientabonnements-Auflistung

Enthält ein-Objekt für jedes vorübergehende Abonnement. Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **transientabonnements** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Transientpublisherproperties**](transientpublisherproperties.md)
-   [**Transientabonberproperties**](transientsubscriberproperties.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Beschreibung](#description)
-   [Aktiviert](#enabled)
-   [Eventclasspartitionid](#eventclasspartitionid)
-   [Eventclsid](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [ID](#transientsubscriptions-collection)
-   [InterfaceID](#interfaceid)
-   [MethodName](#methodname)
-   [Name](#methodname)
-   [Peruser](#peruser)
-   [PublisherID](#publisherid)
-   [Abonnement Schnittstelle](#subscriberinterface)
-   [Abonnement-ID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|-------------------------------------|
| BESCHREIBUNG    | Eine Beschreibung für das Abonnement. |
| Access         | ReadWrite                           |
| type           | String                              |
| Standard        | ""                                  |
| Minimalsystem | Windows 2000                        |



 

### <a name="enabled"></a>Aktiviert



| Eingabe | Wert |
|----------------|----------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob das Abonnement derzeit aktiviert ist. |
| Access         | ReadWrite                                                |
| type           | Bool                                                     |
| Standard        | Richtig                                                     |
| Minimalsystem | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>Eventclasspartitionid



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Beim Abonnieren einer Ereignisklasse wird verwendet, um die GUID der Partitions-ID darzustellen, die die Ereignisklasse enthält. Beim Abonnieren von Ereignis Klassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder in einer anderen Partition zu abonnieren. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| type           | String                                                                                                                                                                                                                                             |
| Standard        | NULL                                                                                                                                                                                                                                               |
| Minimalsystem | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>Eventclsid



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Die CLSID für die Ereignisklasse. Sie können angeben, dass es sich um eine eventclsid oder eine PublisherID handelt, aber nicht beides. |
| Access         | WriteOnce                                                                                    |
| type           | String                                                                                       |
| Standard        | –                                                                                          |
| Minimalsystem | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine Zeichenfolge, die die Filterkriterien angibt. Kann eine CLSID für eine [**publisherfilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) -Klasse sein. |
| Access         | ReadWrite                                                                                                            |
| type           | String                                                                                                               |
| Standard        | –                                                                                                                  |
| Minimalsystem | Windows 2000                                                                                                         |



 

### <a name="id"></a>id



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Bezeichner für das Abonnement. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                        |
| type           | String                                                                                                                                                           |
| Standard        | <Generated>                                                                                                                                                |
| Minimalsystem | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Eingabe | Wert |
|----------------|----------------------------------|
| BESCHREIBUNG    | IID für die Schnittstelle, die abonniert hat. |
| Access         | WriteOnce                        |
| type           | String                           |
| Standard        | –                              |
| Minimalsystem | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Eingabe | Wert |
|----------------|----------------------------------------------|
| BESCHREIBUNG    | Methode für die Schnittstelle, die abonniert wird. |
| Access         | ReadWrite                                    |
| type           | String                                       |
| Standard        | –                                          |
| Minimalsystem | Windows 2000                                 |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name des Abonnements. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                 |
| Standard        | "Neues Abonnement"                                                                                                                                                                                                                     |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>Peruser



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob das Abonnement nur für einen bestimmten Benutzer gilt, der durch die UserName-Eigenschaft dargestellt wird. |
| Access         | ReadWrite                                                                                               |
| type           | Bool                                                                                                    |
| Standard        | Falsch                                                                                                   |
| Minimalsystem | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------|
| BESCHREIBUNG    | ID für den Verleger. Sie können angeben, dass es sich um eine eventclsid oder eine PublisherID handelt, aber nicht beides. |
| Access         | WriteOnce                                                                           |
| type           | String                                                                              |
| Standard        | ""                                                                                  |
| Minimalsystem | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>Abonnement Schnittstelle



| Eingabe | Wert |
|----------------|------------------------------------------|
| BESCHREIBUNG    | Ein Zeiger auf die-Schnittstelle des Abonnenten. |
| Access         | ReadWrite                                |
| type           | Variant                                  |
| Standard        | –                                      |
| Minimalsystem | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>Abonnement-ID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Beim Abonnieren einer Ereignisklasse in derselben Partition wird zur Darstellung der GUID der Partitions-ID des Abonnenten verwendet. Beim Abonnieren von Ereignis Klassen hat der Abonnent die Möglichkeit, eine Ereignisklasse in derselben oder in einer anderen Partition zu abonnieren. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| type           | String                                                                                                                                                                                                                                                          |
| Standard        | <Generated>                                                                                                                                                                                                                                               |
| Minimalsystem | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name des Benutzers, für den das Abonnement gilt, wenn peruser den Wert true hat. |
| Access         | ReadWrite                                                               |
| type           | String                                                                  |
| Standard        | –                                                                     |
| Minimalsystem | Windows 2000                                                            |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
