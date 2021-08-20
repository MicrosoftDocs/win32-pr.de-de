---
description: Ruft Informationen für importierte Anwendungen ab.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: FilesForImport-Sammlung
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
ms.openlocfilehash: 3b6351edd58691db3a499a6c0512e76fe87167f888289b8a2d2a947fe1304cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307327"
---
# <a name="filesforimport-collection"></a>FilesForImport-Sammlung

Ruft Informationen für importierte Anwendungen ab.

Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

Die **FilesForImport-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [ApplicationFileName](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [Beschreibung](#partitiondescription)
-   [FileName](#applicationfilename)
-   [HasUsers](#hasusers)
-   [IsProxy](#isproxy)
-   [IsService](#isservice)
-   [PartitionDescription](#partitiondescription)
-   [PartitionID](#partitionid)
-   [PartitionName](#partitionname)

### <a name="applicationfilename"></a>ApplicationFileName



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------|
| Beschreibung    | Der Name der MSI-Datei, die die Anwendung enthält, die importiert werden kann. |
| Zugriff         | ReadOnly                                                                     |
| type           | String                                                                       |
| Standard        | –                                                                          |
| Mindestsystem | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Eingabe | Wert |
|----------------|------------------------------|
| Beschreibung    | Der Namen der Anwendung. |
| Zugriff         | ReadOnly                     |
| type           | String                       |
| Standard        | ""                           |
| Mindestsystem | Windows XP                   |



 

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|-----------------------------------|
| Beschreibung    | Eine Beschreibung der Anwendung. |
| Zugriff         | ReadOnly                          |
| type           | String                            |
| Standard        | ""                                |
| Mindestsystem | Windows XP                        |



 

### <a name="filename"></a>FileName



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name der DLL oder EXE-Datei, die die Anwendung enthält. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                |
| Standard        | ""                                                                                                                                                                                                                                    |
| Mindestsystem | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>HasUsers



| Eingabe | Wert |
|----------------|--------------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendung über Benutzer verfügt. |
| Zugriff         | ReadOnly                                         |
| type           | Bool                                             |
| Standard        | Falsch                                            |
| Mindestsystem | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| Eingabe | Wert |
|----------------|-----------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendung ein Proxy ist. |
| Zugriff         | ReadOnly                                      |
| type           | Bool                                          |
| Standard        | Falsch                                         |
| Mindestsystem | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| Eingabe | Wert |
|----------------|-------------------------------------------------|
| Beschreibung    | Gibt an, ob die Anwendung ein Dienst ist. |
| Zugriff         | ReadOnly                                        |
| type           | Bool                                            |
| Standard        | Falsch                                           |
| Mindestsystem | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| Eingabe | Wert |
|----------------|-----------------------------------------------|
| Beschreibung    | Eine Beschreibung der Partition der Anwendung. |
| Zugriff         | ReadOnly                                      |
| type           | String                                        |
| Standard        | ""                                            |
| Mindestsystem | Windows Server 2003                           |



 

### <a name="partitionid"></a>Partitionid



| Eingabe | Wert |
|----------------|------------------------------------------|
| Beschreibung    | Die GUID der Anwendungspartition. |
| Zugriff         | ReadOnly                                 |
| type           | String                                   |
| Standard        | ""                                       |
| Mindestsystem | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| Eingabe | Wert |
|----------------|------------------------------------------|
| Beschreibung    | Der Name der Partition der Anwendung. |
| Zugriff         | ReadOnly                                 |
| type           | String                                   |
| Standard        | ""                                       |
| Mindestsystem | Windows Server 2003                      |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
