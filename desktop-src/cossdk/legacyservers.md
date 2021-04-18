---
description: Identisch mit der inprocservers-Auflistung, mit der Ausnahme, dass diese Sammlung auch lokale Server enthält.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Legacyservers-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344199"
---
# <a name="legacyservers-collection"></a>Legacyservers-Sammlung

Identisch mit der [**inprocservers**](inprocservers.md) -Auflistung, mit der Ausnahme, dass diese Sammlung auch lokale Server enthält.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **Legacyservers** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| Eingabe | Wert |
|----------------|------------------------|
| BESCHREIBUNG    | Der Name der Klasse. |
| Access         | ReadOnly               |
| type           | String                 |
| Standard        | –                    |
| Minimalsystem | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID für die Komponente. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | –                                                                                                                                                       |
| Minimalsystem | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Eingabe | Wert |
|----------------|----------------------------------|
| BESCHREIBUNG    | Der Dateipfad für die Komponente. |
| Access         | ReadOnly                         |
| type           | String                           |
| Standard        | –                              |
| Minimalsystem | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Eingabe | Wert |
|----------------|---------------------------------------------------------------|
| BESCHREIBUNG    | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an. |
| Access         | ReadOnly                                                      |
| type           | String                                                        |
| Standard        | –                                                           |
| Minimalsystem | Windows XP                                                    |



 

### <a name="progid"></a>ProgID



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ein Name, der die Komponente identifiziert. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                            |
| type           | String                                                                                                                                                              |
| Standard        | –                                                                                                                                                                 |
| Minimalsystem | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
