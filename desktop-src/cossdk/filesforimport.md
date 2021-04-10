---
description: Ruft Informationen für importierte Anwendungen ab.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Sammlung "filesforimport"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127144"
---
# <a name="filesforimport-collection"></a>Sammlung "filesforimport"

Ruft Informationen für importierte Anwendungen ab.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die Sammlung " **filesforimport** " erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Applicationfilename](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [Beschreibung](#partitiondescription)
-   [FileName](#applicationfilename)
-   [Hasusers](#hasusers)
-   [IsProxy](#isproxy)
-   [IsService](#isservice)
-   [PartitionDescription](#partitiondescription)
-   [PartitionID](#partitionid)
-   [PartitionName](#partitionname)

### <a name="applicationfilename"></a>Applicationfilename



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der MSI-Datei, die die Anwendung enthält, die importiert werden kann. |
| Access         | ReadOnly                                                                     |
| type           | String                                                                       |
| Standard        | –                                                                          |
| Minimalsystem | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Eingabe | Wert |
|----------------|------------------------------|
| BESCHREIBUNG    | Der Namen der Anwendung. |
| Access         | ReadOnly                     |
| type           | String                       |
| Standard        | ""                           |
| Minimalsystem | Windows XP                   |



 

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|-----------------------------------|
| BESCHREIBUNG    | Eine Beschreibung der Anwendung. |
| Access         | ReadOnly                          |
| type           | String                            |
| Standard        | ""                                |
| Minimalsystem | Windows XP                        |



 

### <a name="filename"></a>FileName



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der DLL-oder exe-Datei, die die Anwendung enthält. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                |
| Standard        | ""                                                                                                                                                                                                                                    |
| Minimalsystem | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>Hasusers



| Eingabe | Wert |
|----------------|--------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendung über Benutzer verfügt. |
| Access         | ReadOnly                                         |
| type           | Bool                                             |
| Standard        | Falsch                                            |
| Minimalsystem | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| Eingabe | Wert |
|----------------|-----------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendung ein Proxy ist. |
| Access         | ReadOnly                                      |
| type           | Bool                                          |
| Standard        | Falsch                                         |
| Minimalsystem | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| Eingabe | Wert |
|----------------|-------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Anwendung ein Dienst ist. |
| Access         | ReadOnly                                        |
| type           | Bool                                            |
| Standard        | Falsch                                           |
| Minimalsystem | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| Eingabe | Wert |
|----------------|-----------------------------------------------|
| BESCHREIBUNG    | Eine Beschreibung der Anwendungs Partition. |
| Access         | ReadOnly                                      |
| type           | String                                        |
| Standard        | ""                                            |
| Minimalsystem | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| Eingabe | Wert |
|----------------|------------------------------------------|
| BESCHREIBUNG    | Die GUID der Anwendungs Partition. |
| Access         | ReadOnly                                 |
| type           | String                                   |
| Standard        | ""                                       |
| Minimalsystem | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| Eingabe | Wert |
|----------------|------------------------------------------|
| BESCHREIBUNG    | Der Name der Partition der Anwendung. |
| Access         | ReadOnly                                 |
| type           | String                                   |
| Standard        | ""                                       |
| Minimalsystem | Windows Server 2003                      |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
