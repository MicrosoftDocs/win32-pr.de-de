---
description: Ruft Informationen zu anderen Auflistungen ab, die sich auf die Auflistung beziehen, von der Sie aufgerufen wird.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Relatedcollectioninfo-Auflistung
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
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214141"
---
# <a name="relatedcollectioninfo-collection"></a>Relatedcollectioninfo-Auflistung

Ruft Informationen zu anderen Auflistungen ab, die sich auf die Auflistung beziehen, von der Sie aufgerufen wird. Auf die **relatedcollectioninfo** -Auflistung kann von jedem [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aus zugegriffen werden, indem die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) -Methode verwendet wird. Die **relatedcollectioninfo** -Auflistung enthält ein-Objekt für jede Auflistung, auf die von der ursprünglichen Auflistung aus zugegriffen werden kann. Verwandte Sammlungen Folgen der Hierarchie der Komponenten Dienste-Verwaltungs Tools.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **relatedcollectioninfo** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**PropertyInfo**](propertyinfo.md)
-   **Relatedcollectioninfo**

Sie können von jeder Sammlung aus zu dieser Sammlung navigieren.

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Name](#name)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der verknüpften Auflistung. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                     |
| Standard        | Keine                                                                                                                                                                                                       |
| Minimalsystem | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
