---
description: Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: PropertyInfo-Auflistung
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
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127020"
---
# <a name="propertyinfo-collection"></a>PropertyInfo-Auflistung

Ruft Informationen zu den Eigenschaften ab, die von einer angegebenen Auflistung unterstützt werden. Der Zugriff auf die **PropertyInfo** -Auflistung ist von jedem [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aus möglich, indem die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) -Methode verwendet wird. Die **PropertyInfo** -Auflistung enthält ein-Objekt für jede Eigenschaft, die von der ursprünglichen Auflistung unterstützt wird.

## <a name="members"></a>Member

Die **PropertyInfo** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   **PropertyInfo**
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von jeder Sammlung aus zu dieser Sammlung navigieren.

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Name](#name)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Den Namen der Eigenschaft. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                                         |
| type           | String                                                                                                                                                                                           |
| Standard        | Keine                                                                                                                                                                                             |
| Minimalsystem | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
