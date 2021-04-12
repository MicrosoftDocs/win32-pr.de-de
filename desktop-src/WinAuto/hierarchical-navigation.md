---
title: Hierarchische Navigation
description: Häufig müssen Clients auf der Grundlage ihrer über-/Unterordnungsbeziehungen zwischen Objekten wechseln. Beispielsweise verfügt ein Client möglicherweise bereits über Informationen über ein ToolBar-Steuerelement, aber keine Informationen zu den darin enthaltenen Schaltflächen.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206738"
---
# <a name="hierarchical-navigation"></a>Hierarchische Navigation

Häufig müssen Clients auf der Grundlage ihrer über-/Unterordnungsbeziehungen zwischen Objekten wechseln. Beispielsweise verfügt ein Client möglicherweise bereits über Informationen über ein ToolBar-Steuerelement, aber keine Informationen zu den darin enthaltenen Schaltflächen.

Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle macht die hierarchischen Beziehungen zwischen Objekten verfügbar. Clients können von einem übergeordneten Objekt zu seinen untergeordneten Elementen oder von einem untergeordneten Objekt zu dessen übergeordnetem Element navigieren, indem Sie [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) oder [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)aufrufen.

 

 




