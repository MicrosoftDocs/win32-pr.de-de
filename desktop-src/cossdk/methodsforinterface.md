---
description: Enthält ein-Objekt für jede Methode in der Schnittstelle, mit der die Auflistung verknüpft ist.
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: Methodsforinterface-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393226"
---
# <a name="methodsforinterface-collection"></a>Methodsforinterface-Auflistung

Enthält ein-Objekt für jede Methode in der Schnittstelle, mit der die Auflistung verknüpft ist.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **methodsforinterface** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Rolesformethod**](rolesformethod.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Interfakesforcomponent**](interfacesforcomponent.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Auto Vervollständigen](#autocomplete)
-   [CLSID](#clsid)
-   [Beschreibung](#description)
-   [IID](#iid)
-   [Index](#index)
-   [Name](#name)

### <a name="autocomplete"></a>AutoComplete



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob das Objekt automatisch deaktiviert wird, wenn die Methode abgeschlossen wird, ohne dass SetComplete oder SetAbort unbedingt aufgerufen wird. Dies wirkt sich nur auf die Standardeinstellung des Bits "Done" der JIT-Aktivierung beim Starten der Methode aus. Dieses Bit kann (wie bei SetComplete oder SetAbort) innerhalb der-Methode zurückgesetzt werden, um den Standardwert zu überschreiben. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                  |
| type           | Bool                                                                                                                                                                                                                                                                                                                                       |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                      |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                               |



 

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
|----------------|------------------------------|
| BESCHREIBUNG    | Eine Beschreibung der Methode. |
| Access         | ReadWrite                    |
| type           | String                       |
| Standard        | ""                           |
| Minimalsystem | Windows 2000                 |



 

### <a name="iid"></a>IID



| Eingabe | Wert |
|----------------|---------------------------|
| BESCHREIBUNG    | Eine GUID für die-Schnittstelle. |
| Access         | ReadOnly                  |
| type           | String                    |
| Standard        | –                       |
| Minimalsystem | Windows 2000              |



 

### <a name="index"></a>Index



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Methoden Dispatchbezeichner. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                        |
| type           | **DWORD**                                                                                                                                                       |
| Standard        | –                                                                                                                                                             |
| Minimalsystem | Windows 2000                                                                                                                                                    |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Methodenname. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                           |
| type           | String                                                                                                                                             |
| Standard        | –                                                                                                                                                |
| Minimalsystem | Windows 2000                                                                                                                                       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
