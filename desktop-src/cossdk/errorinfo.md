---
description: Ruft erweiterte Fehlerinformationen zu Methoden ab, die mehrere Objekte behandeln, z. b. auffüllen und SaveChanges des comadmincatalogcollection-Objekts, und Methoden zum Installieren, importieren oder Exportieren von Anwendungen oder Komponenten für das comadmincatalog-Objekt.
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
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483606"
---
# <a name="errorinfo-collection"></a>ErrorInfo-Sammlung

Ruft erweiterte Fehlerinformationen zu [**Methoden ab,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) die mehrere Objekte behandeln, z. b. auffüllen und [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts, und Methoden zum Installieren, importieren oder Exportieren von Anwendungen oder Komponenten für das [**comadmincatalog**](comadmincatalog.md) -Objekt.

Verwenden Sie die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) -Methode für eine [**comadmincatalogcollection**](comadmincatalogcollection.md) , um auf die **errorInfo** -Auflistung zuzugreifen, die der ursprünglichen Auflistung mit einem Fehler zugeordnet ist.

Sie müssen [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) direkt nach einem Fehler auf **errorInfo** aufrufen. Andernfalls gehen die Fehlerinformationen verloren.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **errorInfo** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von jeder Sammlung mit Ausnahme von **errorInfo**, [**inprocservers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**relatedcollectioninfo**](relatedcollectioninfo.md), [**root**](root.md)und [**wowinprocservers**](wowinprocservers.md)zu dieser Sammlung navigieren.

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [ErrorCode](#errorcode)
-   [Majorref](#majorref)
-   [MinorRef](#minorref)
-   [Name](#name)

### <a name="errorcode"></a>ErrorCode



| Eingabe | Wert |
|----------------|----------------------------------------|
| BESCHREIBUNG    | Der Fehlercode für das Objekt oder die Datei. |
| Access         | ReadOnly                               |
| type           | String                                 |
| Standard        | Keine                                   |
| Minimalsystem | Windows 2000                           |



 

### <a name="majorref"></a>Majorref



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschafts Wert für das Objekt, das einen Fehler aufweist. Wenn beispielsweise ein [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Vorgang für eine Auflistung für ein bestimmtes Objekt in der Auflistung fehlschlägt, wird der **Schlüssel** Eigenschafts Wert für dieses Objekt als majorref-Wert gemeldet. Verwenden Sie diese Eigenschaft, um das Element zu überprüfen, das nicht aktualisiert werden kann, oder um die Komponente oder dll zu finden, die nicht installiert werden kann. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| type           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Standard        | Keine                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine genaue Angabe des Elements, das einen Fehler aufweist, z. b. einen Eigenschaftsnamen. Wenn mehrere Fehler auftreten oder in Kontexten, in denen dies nicht zutrifft, ist MinorRef gleich <Invalid> . |
| Access         | ReadOnly                                                                                                                                                                          |
| type           | String                                                                                                                                                                            |
| Standard        | Keine                                                                                                                                                                              |
| Minimalsystem | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name des Objekts oder der Datei, die einen Fehler aufweist. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| type           | String                                                                                                                                                                                                                   |
| Standard        | Keine                                                                                                                                                                                                                     |
| Minimalsystem | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
