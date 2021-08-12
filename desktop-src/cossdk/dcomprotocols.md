---
description: Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen. Sie enthält ein -Objekt für jedes Protokoll.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: DCOMProtocols-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: f387c9ba1d46b99c44a3d6616df95f7b6f9cece959a943b63ed12ce6fe8af900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548019"
---
# <a name="dcomprotocols-collection"></a>DCOMProtocols-Sammlung

Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen. Sie enthält ein -Objekt für jedes Protokoll.

Diese Sammlung unterstützt die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **DCOMProtocols-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Name](#name)
-   [Order](#order)
-   [ProtocolCode](#protocolcode)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name des Protokolls. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) zurückgegeben, wenn die Name-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadWrite                                                                                                                                                   |
| type           | String                                                                                                                                                      |
| Standard        | "Neues Protokoll"                                                                                                                                              |
| Mindestsystem | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>Auftrag



| Eingabe | Wert |
|----------------|-----------------------------------------|
| Beschreibung    | Die Reihenfolge, in der das Protokoll versucht werden soll. |
| Zugriff         | ReadWrite                               |
| Typ           | Long (0-65000)                          |
| Standard        | 0                                       |
| Mindestsystem | Windows 2000                            |



 

### <a name="protocolcode"></a>ProtocolCode



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Code, der die RPC-Protokollsequenz an gibt. Folgende Protokollcodes werden unterstützt: ncacn \_ ip \_ tcp, ncacn \_ http, ncacn \_ spx. Diese Eigenschaft wird [](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) zurückgegeben, wenn die Key-Eigenschaftsmethode für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                                                                                      |
| Standard        | ""                                                                                                                                                                                                                                                                          |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
