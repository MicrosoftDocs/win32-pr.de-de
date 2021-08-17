---
description: Ruft Informationen zum Ausführen von Anwendungen ab.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: ApplicationInstances-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 957fe3fa556a3e41e2484116ff2c9242fd63efa1469a4a6040f31aa04a3627e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129382"
---
# <a name="applicationinstances-collection"></a>ApplicationInstances-Sammlung

Ruft Informationen zum Ausführen von Anwendungen ab.

Diese Sammlung unterstützt die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **ApplicationInstances-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Anwendungen**](applications.md)
-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Anwendung](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Anwendung



| Eingabe | Wert |
|----------------|-------------------------------------|
| Beschreibung    | Die ID für die ausgeführte Anwendung. |
| Zugriff         | ReadOnly                            |
| type           | String                              |
| Standard        | Nicht zutreffend                                 |
| Mindestsystem | Windows XP                          |



 

### <a name="hasrecycled"></a>HasRecycled



| Eingabe | Wert |
|----------------|---------------------------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendungsinstanz wiederverwendet wurde. |
| Zugriff         | ReadOnly                                                      |
| type           | Bool                                                          |
| Standard        | Falsch                                                         |
| Mindestsystem | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der global eindeutige Bezeichner für die Anwendungsinstanz. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                                                                                            |
| type           | String                                                                                                                                                                                                                              |
| Standard        | Nicht zutreffend                                                                                                                                                                                                                                 |
| Mindestsystem | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendungsinstanz derzeit angehalten ist. |
| Zugriff         | ReadOnly                                                        |
| type           | Bool                                                            |
| Standard        | Falsch                                                           |
| Mindestsystem | Windows XP                                                      |



 

### <a name="partitionid"></a>Partitionid



| Eingabe | Wert |
|----------------|-------------------------------------------------|
| Beschreibung    | Die Partitions-ID, die von der Anwendung verwendet wird. |
| Zugriff         | ReadOnly                                        |
| type           | String                                          |
| Standard        | Nicht zutreffend                                             |
| Mindestsystem | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Eingabe | Wert |
|----------------|---------------------------------------------|
| Beschreibung    | Die Prozess-ID der Anwendungsinstanz. |
| Zugriff         | ReadOnly                                    |
| type           | String                                      |
| Standard        | Nicht zutreffend                                         |
| Mindestsystem | Windows XP                                  |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
