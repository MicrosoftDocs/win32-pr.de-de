---
description: Die RolesForPartition-Auflistung bezieht sich immer auf ein Objekt in der Partitionsauflistung. Sie enthält ein -Objekt für jede Rolle, die der Partition zugewiesen ist, mit der sie verknüpft ist.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: RolesForPartition-Sammlung
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
ms.openlocfilehash: 6c1e64e314478793a5b421d1f0a6a76c2eb028708410a14ea426f52fbd41dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637040"
---
# <a name="rolesforpartition-collection"></a>RolesForPartition-Sammlung

Die **RolesForPartition-Auflistung** bezieht sich immer auf ein Objekt in der [**Partitionsauflistung.**](partitions.md) Sie enthält ein -Objekt für jede Rolle, die der Partition zugewiesen ist, mit der sie verknüpft ist.

Diese Auflistung unterstützt nicht die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **RolesForPartition-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInPartitionRole**](usersinpartitionrole.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Partitionen**](partitions.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Beschreibung](#description)
-   [Name](#name)

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|----------------------------|
| Beschreibung    | Eine Beschreibung der Rolle. |
| Zugriff         | ReadOnly                   |
| type           | String                     |
| Standard        | ""                         |
| Mindestsystem | Windows Server 2003        |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name der Rolle. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                                                                                                                    |
| type           | String                                                                                                                                                                                                                                                      |
| Standard        | ""                                                                                                                                                                                                                                                          |
| Mindestsystem | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
