---
description: Ruft Informationen zu laufenden Anwendungen ab.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: ApplicationInstance-Auflistung
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
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483163"
---
# <a name="applicationinstances-collection"></a>ApplicationInstance-Auflistung

Ruft Informationen zu laufenden Anwendungen ab.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **ApplicationInstance** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Anwendungen**](applications.md)
-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Anwendung](#applicationinstances-collection)
-   [Hasrecycelt](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Application



| Eingabe | Wert |
|----------------|-------------------------------------|
| BESCHREIBUNG    | Die ID für die laufende Anwendung. |
| Access         | ReadOnly                            |
| type           | String                              |
| Standard        | –                                 |
| Minimalsystem | Windows XP                          |



 

### <a name="hasrecycled"></a>Hasrecycelt



| Eingabe | Wert |
|----------------|---------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendungs Instanz wieder verwendet wurde. |
| Access         | ReadOnly                                                      |
| type           | Bool                                                          |
| Standard        | Falsch                                                         |
| Minimalsystem | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Globally Unique Identifier für die Anwendungs Instanz. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                                                                            |
| type           | String                                                                                                                                                                                                                              |
| Standard        | –                                                                                                                                                                                                                                 |
| Minimalsystem | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendungs Instanz zurzeit angehalten ist. |
| Access         | ReadOnly                                                        |
| type           | Bool                                                            |
| Standard        | Falsch                                                           |
| Minimalsystem | Windows XP                                                      |



 

### <a name="partitionid"></a>PartitionID



| Eingabe | Wert |
|----------------|-------------------------------------------------|
| BESCHREIBUNG    | Die Partitions-ID, die von der Anwendung verwendet wird. |
| Access         | ReadOnly                                        |
| type           | String                                          |
| Standard        | –                                             |
| Minimalsystem | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Eingabe | Wert |
|----------------|---------------------------------------------|
| BESCHREIBUNG    | Die Prozess-ID der Anwendungs Instanz. |
| Access         | ReadOnly                                    |
| type           | String                                      |
| Standard        | –                                         |
| Minimalsystem | Windows XP                                  |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
