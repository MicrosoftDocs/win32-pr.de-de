---
title: Erstellen von Proxyobjekten
description: Zusätzlich zum Entwerfen von Klassen, die IAccessible-Eigenschaften und -Methoden implementieren, müssen Serverentwickler möglicherweise auch Proxyobjekte entwerfen, die die Lebensdauer von barrierefreien Objekten überwachen.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49abceb3b38b4495d871605634c8f95353c35b4b6bcd0c54dda374c75572fbea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133893"
---
# <a name="creating-proxy-objects"></a>Erstellen von Proxyobjekten

Zusätzlich zum Entwerfen von Klassen, die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden implementieren, müssen Serverentwickler möglicherweise auch Proxyobjekte entwerfen, die die Lebensdauer von barrierefreien Objekten überwachen.  Wenn ein barrierefreies Objekt in einer Anwendung während der gesamten Ausführung der Anwendung verfügbar ist, müssen Sie kein Proxyobjekt erstellen. Wenn es möglich ist, das barrierefreie Objekt zu zerstören, während die Anwendung ausgeführt wird, müssen Sie ein Proxyobjekt erstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Was sind Proxyobjekte?](what-are-proxy-objects.md)
-   [Gründe für die Verwendung von Proxyobjekten](why-proxy-objects-are-needed.md)
-   [Entwurfsüberlegungen für Proxyobjekte](design-considerations-for-proxy-objects.md)

 

 




