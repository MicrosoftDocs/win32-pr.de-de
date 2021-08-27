---
description: Ruft erweiterte Fehlerinformationen zu Methoden ab, die mehrere Objekte behandeln, z. B. Populate und SaveChanges für das COMAdminCatalogCollection-Objekt und Methoden zum Installieren, Importieren oder Exportieren von Anwendungen oder Komponenten im COMAdminCatalog-Objekt.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: ErrorInfo-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9953bc1119d7e203936ca7e78048a4083a996ec2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881043"
---
# <a name="errorinfo-collection"></a>ErrorInfo-Sammlung

Ruft erweiterte Fehlerinformationen zu Methoden ab, die mehrere Objekte behandeln, z. [**B. Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) und [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für das [**COMAdminCatalogCollection-Objekt**](comadmincatalogcollection.md) und Methoden zum Installieren, Importieren oder Exportieren von Anwendungen oder Komponenten im [**COMAdminCatalog-Objekt.**](comadmincatalog.md)

Verwenden Sie die [**GetCollection-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) für eine [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) um auf die **ErrorInfo-Auflistung** zuzugreifen, die der ursprünglichen Sammlung zugeordnet ist, die einen Fehler aufweist.

Sie müssen [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) für **ErrorInfo** sofort aufrufen, nachdem ein Fehler aufgetreten ist. Andernfalls geht die Fehlerinformation verloren.

Diese Auflistung unterstützt nicht die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **ErrorInfo-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können aus jeder Sammlung zu dieser Sammlung navigieren, mit Ausnahme von **ErrorInfo,** [**InprocServers,**](inprocservers.md) [**PropertyInfo,**](propertyinfo.md) [**RelatedCollectionInfo,**](relatedcollectioninfo.md) [**Root**](root.md)und [**WOWInprocServers.**](wowinprocservers.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   [Name](#name)

### <a name="errorcode"></a>ErrorCode



| Eingabe | Wert |
|----------------|----------------------------------------|
| Beschreibung    | Der Fehlercode für das Objekt oder die Datei. |
| Access         | ReadOnly                               |
| type           | String                                 |
| Standard        | Keine                                   |
| Mindestsystem | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der [**Key-Eigenschaftswert**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) für das Objekt, das einen Fehler aufweist. Wenn beispielsweise ein [**SaveChanges-Aufruf**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für eine Auflistung für ein bestimmtes Objekt in der Auflistung fehlschlägt, wird der **Key-Eigenschaftswert** für dieses Objekt als MajorRef-Wert gemeldet. Verwenden Sie diese Eigenschaft, um das Element zu untersuchen, das nicht aktualisiert werden kann, oder um die Komponente oder DLL zu suchen, die nicht installiert werden kann. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Standard        | Keine                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine genaue Angabe des Elements, das einen Fehler aufweist, z. B. ein Eigenschaftenname. Wenn mehrere Fehler auftreten oder in Kontexten, in denen dies nicht zutrifft, ist MinorRef &lt; &gt; ungültig. |
| Access         | ReadOnly                                                                                                                                                                          |
| type           | String                                                                                                                                                                            |
| Standard        | Keine                                                                                                                                                                              |
| Mindestsystem | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name des Objekts oder der Datei, das bzw. die einen Fehler aufweist. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| type           | String                                                                                                                                                                                                                   |
| Standard        | Keine                                                                                                                                                                                                                     |
| Mindestsystem | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
