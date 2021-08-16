---
description: Gibt die in jeder Partition enthaltenen Anwendungen an.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Partitionssammlung
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
ms.openlocfilehash: 3badf52755a77557c200569c25610b5918cf8dd599d17a83bdebb5c4ddfa6801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305873"
---
# <a name="partitions-collection"></a>Partitionssammlung

Gibt die in jeder Partition enthaltenen Anwendungen an.

Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **Partitionsauflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**Anwendungen**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Änderbar](#changeable)
-   [Löschbar](#deleteable)
-   [Beschreibung](#description)
-   [ID](#partitions-collection)
-   [Name](#name)

### <a name="changeable"></a>Änderbar



| Eingabe | Wert |
|----------------|--------------------------------------------------|
| Beschreibung    | Bestimmt, ob diese Partition geändert werden kann. |
| Access         | ReadWrite                                        |
| type           | Bool                                             |
| Standard        | True                                             |
| Mindestsystem | Windows Server 2003                              |



 

### <a name="deleteable"></a>Löschbar



| Eingabe | Wert |
|----------------|---------------------------------------------------|
| Beschreibung    | Bestimmt, ob diese Partition gelöscht werden kann. |
| Access         | ReadWrite                                         |
| type           | Bool                                              |
| Standard        | True                                              |
| Mindestsystem | Windows Server 2003                               |



 

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------|
| Beschreibung    | Diese Eigenschaft stellt die Beschreibung dar, die die Partition identifiziert. |
| Access         | ReadWrite                                                           |
| type           | String                                                              |
| Standard        | ""                                                                  |
| Mindestsystem | Windows Server 2003                                                 |



 

### <a name="id"></a>ID



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine GUID, die die Partition darstellt. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                          |
| type           | String                                                                                                                                                             |
| Standard        | <Generated>                                                                                                                                                  |
| Mindestsystem | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Stellt den Partitionsnamen dar. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                 |
| Standard        | "Neue Partition"                                                                                                                                                                                                                        |
| Mindestsystem | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
