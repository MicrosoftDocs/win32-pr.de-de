---
description: Gibt die Anwendungen an, die in jeder Partition enthalten sind.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Partitions Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749080"
---
# <a name="partitions-collection"></a>Partitions Sammlung

Gibt die Anwendungen an, die in jeder Partition enthalten sind.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **Partitions** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**Anwendungen**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Rolesforpartition**](rolesforpartition.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Austauschbar](#changeable)
-   [Gelöscht werden](#deleteable)
-   [Beschreibung](#description)
-   [ID](#partitions-collection)
-   [Name](#name)

### <a name="changeable"></a>Austauschbar



| Eingabe | Wert |
|----------------|--------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob diese Partition änderbar ist. |
| Access         | ReadWrite                                        |
| type           | Bool                                             |
| Standard        | Richtig                                             |
| Minimalsystem | Windows Server 2003                              |



 

### <a name="deleteable"></a>Gelöscht werden



| Eingabe | Wert |
|----------------|---------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob diese Partition gelöscht werden kann. |
| Access         | ReadWrite                                         |
| type           | Bool                                              |
| Standard        | Richtig                                              |
| Minimalsystem | Windows Server 2003                               |



 

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------|
| BESCHREIBUNG    | Diese Eigenschaft stellt die Beschreibung dar, die die Partition identifiziert. |
| Access         | ReadWrite                                                           |
| type           | String                                                              |
| Standard        | ""                                                                  |
| Minimalsystem | Windows Server 2003                                                 |



 

### <a name="id"></a>id



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID, die die Partition darstellt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                          |
| type           | String                                                                                                                                                             |
| Standard        | <Generated>                                                                                                                                                  |
| Minimalsystem | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Stellt den Partitionsnamen dar. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                 |
| Standard        | "Neue Partition"                                                                                                                                                                                                                        |
| Minimalsystem | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
