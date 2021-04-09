---
title: Nur Attribute suchen
description: Manchmal führen Sie eine Suche durch, um zu ermitteln, welche Art von Daten für ein Objekt verfügbar ist.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Nur Attribute suchen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947331"
---
# <a name="search-attributes-only"></a>Nur Attribute suchen

Manchmal führen Sie eine Suche durch, um zu ermitteln, welche Art von Daten für ein Objekt verfügbar ist. In diesem Fall interessieren Sie sich nur für die Attribute und nicht für die Werte des Objekts. Um dies zu erreichen, legen Sie die Option "nur Attribute suchen" fest. Wenn Sie diese Option angeben, werden die Attributnamen ohne ihre Werte zurückgegeben. Das Resultset enthält jedoch nur die Attribute, denen Werte zugewiesen sind. Nehmen Sie beispielsweise ein Objekt mit den folgenden Attributen:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Wenn die Option nur Such Attribute festgelegt ist, enthält das Resultset Folgendes:

``` syntax
First Name
Last Name
Phone Number
```

Weitere Informationen zum Verwenden der Option nur Such Attribute mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Zurückgeben von Attributnamen mit idirector ysearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




