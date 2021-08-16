---
description: Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: PropertyInfo-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf5c354711ec9ca34af1809707a7a869d39a3026ca5cb7ca11d2245c02be049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547581"
---
# <a name="propertyinfo-collection"></a>PropertyInfo-Sammlung

Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden. Auf **die PropertyInfo-Auflistung** kann von jedem [**COMAdminCatalogCollection-Objekt aus zugegriffen**](comadmincatalogcollection.md) werden, indem die [**GetCollection-Methode verwendet**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) wird. Die **PropertyInfo-Auflistung** enthält ein -Objekt für jede Eigenschaft, die von der ursprünglichen Auflistung unterstützt wird.

## <a name="members"></a>Member

Die **PropertyInfo-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   **Propertyinfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können von jeder Sammlung zu dieser Sammlung navigieren.

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Name](#name)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name der Eigenschaft. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                                                         |
| type           | String                                                                                                                                                                                           |
| Standard        | Keine                                                                                                                                                                                             |
| Mindestsystem | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
