---
description: Enthält ein-Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Interfakesforcomponent-Auflistung
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
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127025"
---
# <a name="interfacesforcomponent-collection"></a>Interfakesforcomponent-Auflistung

Enthält ein-Objekt für jede Schnittstelle, die von der Komponente verfügbar gemacht wird, mit der die Auflistung verknüpft ist.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **interfakesforcomponent** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Methodsforinterface**](methodsforinterface.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Rolesforinterface**](rolesforinterface.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Komponenten**](components.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [CLSID](#clsid)
-   [Beschreibung](#description)
-   [IID](#iid)
-   [Name](#name)
-   [Queuingenabled](#queuingenabled)
-   [Queueingsupported](#queueingsupported)

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|---------------------------|
| BESCHREIBUNG    | Eine GUID für die Komponente. |
| Access         | ReadOnly                  |
| type           | String                    |
| Standard        | –                       |
| Minimalsystem | Windows 2000              |



 

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|----------------------------------|
| BESCHREIBUNG    | Eine Beschreibung für die-Schnittstelle. |
| Access         | ReadWrite                        |
| type           | String                           |
| Standard        | ""                               |
| Minimalsystem | Windows 2000                     |



 

### <a name="iid"></a>IID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID für die-Schnittstelle. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | –                                                                                                                                                       |
| Minimalsystem | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ein Name für die-Schnittstelle. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                    |
| type           | String                                                                                                                                                      |
| Standard        | –                                                                                                                                                         |
| Minimalsystem | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>Queuingenabled



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Markiert die Schnittstelle als Warteschlange und kann mithilfe des Verwaltungs Tools admin SDK oder Komponenten Dienste festgelegt werden. Allerdings kann für nur eine Schnittstelle, für die das in der **Warteschlange** stehende Flag festgelegt ist, das **queuingaktivierte** Flag festgelegt |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| type           | Bool                                                                                                                                                                                                                               |
| Standard        | Falsch                                                                                                                                                                                                                              |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>Queueingsupported



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Schnittstelle unterstützt Warteschlangen. Damit eine Schnittstelle Warteschlangen unterstützt, sollten alle Methoden nur in den Parametern enthalten. **Unterstützte Warteschlangen werden** als schreibgeschützte Eigenschaft verfügbar gemacht. |
| Access         | ReadOnly                                                                                                                                                               |
| type           | Bool                                                                                                                                                                   |
| Standard        | Falsch                                                                                                                                                                  |
| Minimalsystem | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
