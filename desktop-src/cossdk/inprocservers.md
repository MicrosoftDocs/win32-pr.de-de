---
description: Enthält eine Liste der Prozessserver, die beim System registriert sind. Sie enthält ein -Objekt für jede Komponente, die als Prozessserver registriert ist.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: InprocServers-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: b751f007082454832fe31172e35b834b66c36d13dbaf6a6687ba0036879b60c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047458"
---
# <a name="inprocservers-collection"></a>InprocServers-Sammlung

Enthält eine Liste der Prozessserver, die beim System registriert sind. Sie enthält ein -Objekt für jede Komponente, die als Prozessserver registriert ist.

Diese Auflistung unterstützt die [**Remove-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts,**](comadmincatalogcollection.md) jedoch nicht die [**Add-Methode.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) Verwenden Sie zum Installieren oder Importieren von Komponenten in eine Anwendung Methoden für das [**COMAdminCatalog-Objekt.**](comadmincatalog.md)

## <a name="members"></a>Member

Die **InprocServers-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Clsid](#clsid)
-   [Inprocserver32](#inprocserver32)
-   [ProgID](#progid)

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine GUID für die Komponente. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                  |
| type           | String                                                                                                                                                    |
| Standard        | Nicht zutreffend                                                                                                                                                       |
| Mindestsystem | Windows 2000                                                                                                                                              |



 

### <a name="inprocserver32"></a>Inprocserver32



| Eingabe | Wert |
|----------------|----------------------------------|
| Beschreibung    | Der Dateipfad für die Komponente. |
| Zugriff         | ReadOnly                         |
| type           | String                           |
| Standard        | Nicht zutreffend                              |
| Mindestsystem | Windows 2000                     |



 

### <a name="progid"></a>ProgID



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Ein Name, der die Komponente identifiziert. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                            |
| type           | String                                                                                                                                                              |
| Standard        | Nicht zutreffend                                                                                                                                                                 |
| Mindestsystem | Windows 2000                                                                                                                                                        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
