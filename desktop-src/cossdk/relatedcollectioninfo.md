---
description: Ruft Informationen zu anderen Auflistungen ab, die mit der Auflistung verknüpft sind, aus der sie aufgerufen wird.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: RelatedCollectionInfo-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 45e9e0f0e251bc9b0772d5def40fec148d541964d34e4f1dda954825f456468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637090"
---
# <a name="relatedcollectioninfo-collection"></a>RelatedCollectionInfo-Sammlung

Ruft Informationen zu anderen Auflistungen ab, die mit der Auflistung verknüpft sind, aus der sie aufgerufen wird. Auf **die RelatedCollectionInfo-Auflistung** kann von jedem [**COMAdminCatalogCollection-Objekt aus zugegriffen**](comadmincatalogcollection.md) werden, indem die [**GetCollection-Methode verwendet**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) wird. Die **RelatedCollectionInfo-Auflistung** enthält ein -Objekt für jede Auflistung, auf die von der ursprünglichen Auflistung aus zugegriffen werden kann. Verwandte Sammlungen folgen der Sammlungshierarchie der Komponentendienste-Verwaltungstool.

Diese Sammlung unterstützt nicht die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **RelatedCollectionInfo-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**Propertyinfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

Sie können von jeder Sammlung zu dieser Sammlung navigieren.

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Name](#name)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name der verknüpften Auflistung. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | ReadOnly                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                     |
| Standard        | Keine                                                                                                                                                                                                       |
| Mindestsystem | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
