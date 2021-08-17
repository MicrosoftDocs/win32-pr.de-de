---
title: Nur Suchattribute
description: Manchmal führen Sie eine Suche durch, um zu bestimmen, welcher Datentyp für ein Objekt verfügbar ist.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Search Attributes Only ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b1775c759975a508f5382ef2a30f290ac4a96b3b92120d4face6b1d0556426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443930"
---
# <a name="search-attributes-only"></a>Nur Suchattribute

Manchmal führen Sie eine Suche durch, um zu bestimmen, welcher Datentyp für ein Objekt verfügbar ist. In diesem Fall interessieren Sie sich nur für die Attribute und nicht für die Werte des Objekts. Um dies zu erreichen, legen Sie die Option "Nur Attribute durchsuchen" fest. Wenn Sie diese Option angeben, werden die Attributnamen ohne ihre Werte zurückgegeben. Das Resultset enthält jedoch nur die Attribute, denen Werte zugewiesen sind. Betrachten Sie beispielsweise ein Objekt mit den folgenden Attributen:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Wenn die Option Nur Suchattribute festgelegt ist, enthält das Resultset Folgendes:

``` syntax
First Name
Last Name
Phone Number
```

Weitere Informationen zur Verwendung der Option "Nur Suchattribute" mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Zurückgeben von nur Attributnamen mit IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




