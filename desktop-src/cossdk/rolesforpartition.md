---
description: Die rolesforpartition-Auflistung ist immer mit einem Objekt in der Partitions Sammlung verknüpft. Sie enthält ein-Objekt für jede Rolle, die der Partition zugewiesen ist, mit der Sie verknüpft ist.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Rolesforpartition-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126332"
---
# <a name="rolesforpartition-collection"></a>Rolesforpartition-Sammlung

Die **rolesforpartition** -Auflistung ist immer mit einem Objekt in der [**Partitions**](partitions.md) Sammlung verknüpft. Sie enthält ein-Objekt für jede Rolle, die der Partition zugewiesen ist, mit der Sie verknüpft ist.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **rolesforpartition** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Usersinpartitionrole**](usersinpartitionrole.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Partitionen**](partitions.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Beschreibung](#description)
-   [Name](#name)

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|----------------------------|
| BESCHREIBUNG    | Eine Beschreibung der Rolle. |
| Access         | ReadOnly                   |
| type           | String                     |
| Standard        | ""                         |
| Minimalsystem | Windows Server 2003        |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der Rolle. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                                                                                                    |
| type           | String                                                                                                                                                                                                                                                      |
| Standard        | ""                                                                                                                                                                                                                                                          |
| Minimalsystem | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
