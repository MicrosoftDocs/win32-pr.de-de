---
description: Identisch mit der InprocServers-Sammlung, mit der Ausnahme, dass diese Sammlung auch lokale Server enthält.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: LegacyServers-Sammlung
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
ms.openlocfilehash: 3968b3cb7068f994d3ff44e7182add2b1e3cb7a44c0d73019cf583a0e8c7f70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306358"
---
# <a name="legacyservers-collection"></a>LegacyServers-Sammlung

Identisch mit der [**InprocServers-Sammlung,**](inprocservers.md) mit der Ausnahme, dass diese Sammlung auch lokale Server enthält.

Diese Auflistung unterstützt nicht die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **LegacyServers-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Classname](#classname)
-   [Clsid](#clsid)
-   [Inprocserver32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| Eingabe | Wert |
|----------------|------------------------|
| BESCHREIBUNG    | Der Name der Klasse. |
| Zugriff         | ReadOnly               |
| type           | String                 |
| Standard        | Nicht zutreffend                    |
| Mindestsystem | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine GUID für die Komponente. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | Nicht zutreffend                                                                                                                                                       |
| Mindestsystem | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>Inprocserver32



| Eingabe | Wert |
|----------------|----------------------------------|
| BESCHREIBUNG    | Der Dateipfad für die Komponente. |
| Zugriff         | ReadOnly                         |
| type           | String                           |
| Standard        | Nicht zutreffend                              |
| Mindestsystem | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Eingabe | Wert |
|----------------|---------------------------------------------------------------|
| BESCHREIBUNG    | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an. |
| Zugriff         | ReadOnly                                                      |
| type           | String                                                        |
| Standard        | Nicht zutreffend                                                           |
| Mindestsystem | Windows XP                                                    |



 

### <a name="progid"></a>ProgID



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ein Name, der die Komponente identifiziert. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                            |
| type           | String                                                                                                                                                              |
| Standard        | Nicht zutreffend                                                                                                                                                                 |
| Mindestsystem | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
