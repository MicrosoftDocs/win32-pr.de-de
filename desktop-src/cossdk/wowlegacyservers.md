---
description: Verfügbar gemachte Eigenschaften für die Sammlung "wowlegacyservers" sind identisch mit der "Legacyservers"-Sammlung, mit dem Unterschied, dass die Sammlung "wowlegacyservers" aus der 32-Bit-Registrierung auf 64-Bit-Computern gezeichnet wird.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Sammlung "wowlegacyservers"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346436"
---
# <a name="wowlegacyservers-collection"></a>Sammlung "wowlegacyservers"

Verfügbar gemachte Eigenschaften für die Sammlung " **wowlegacyservers** " sind identisch mit der " [**Legacyservers**](legacyservers.md) "-Sammlung, mit dem Unterschied, dass die Sammlung " **wowlegacyservers** " aus der 32-Bit-Registrierung auf 64-Bit-Computern gezeichnet wird.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **wowlegacyservers** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

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

 

 
