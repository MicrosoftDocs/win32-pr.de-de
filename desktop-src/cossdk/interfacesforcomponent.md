---
description: Enthält ein -Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: InterfacesForComponent-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 13c0ed22b6d4ee8ffb4a0d6c4d3f6475341192f656c48553ab901206be833b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047448"
---
# <a name="interfacesforcomponent-collection"></a>InterfacesForComponent-Auflistung

Enthält ein -Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.

Diese Sammlung unterstützt nicht die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **InterfacesForComponent-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**MethodsForInterface**](methodsforinterface.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForInterface**](rolesforinterface.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Komponenten**](components.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Clsid](#clsid)
-   [Beschreibung](#description)
-   [IID](#iid)
-   [Name](#name)
-   [QueuingEnabled](#queuingenabled)
-   [QueueingSupported](#queueingsupported)

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|---------------------------|
| Beschreibung    | Eine GUID für die Komponente. |
| Zugriff         | ReadOnly                  |
| type           | String                    |
| Standard        | Nicht zutreffend                       |
| Mindestsystem | Windows 2000              |



 

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|----------------------------------|
| Beschreibung    | Eine Beschreibung für die Schnittstelle. |
| Zugriff         | ReadWrite                        |
| type           | String                           |
| Standard        | ""                               |
| Mindestsystem | Windows 2000                     |



 

### <a name="iid"></a>IID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine GUID für die Schnittstelle. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | Nicht zutreffend                                                                                                                                                       |
| Mindestsystem | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Ein Name für die Schnittstelle. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                    |
| type           | String                                                                                                                                                      |
| Standard        | Nicht zutreffend                                                                                                                                                         |
| Mindestsystem | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Markiert die Schnittstelle als warteschlangenfähig und kann mit dem Admin SDK oder dem Verwaltungstool für Komponentendienste festgelegt werden. Allerdings kann nur für eine Schnittstelle, für die das **Flag Queuing Supported** festgelegt ist, das **Flag Queuing Enabled** festgelegt werden. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                          |
| Typ           | Bool                                                                                                                                                                                                                               |
| Standard        | Falsch                                                                                                                                                                                                                              |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>QueueingSupported



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Die Schnittstelle unterstützt Warteschlangen. Damit eine Schnittstelle Warteschlangen unterstützt, sollten alle Methoden nur in Parametern enthalten sein. **Unterstützte Warteschlangen** werden als schreibgeschützte Eigenschaft verfügbar gemacht. |
| Zugriff         | ReadOnly                                                                                                                                                               |
| Typ           | Bool                                                                                                                                                                   |
| Standard        | Falsch                                                                                                                                                                  |
| Mindestsystem | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
