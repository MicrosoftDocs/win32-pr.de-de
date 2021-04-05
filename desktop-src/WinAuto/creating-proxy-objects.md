---
title: Erstellen von Proxy Objekten
description: Zusätzlich zum Entwerfen von Klassen, die Eigenschaften und Methoden von IAccessible implementieren, müssen Server Entwickler möglicherweise auch Proxy Objekte entwerfen, die die Lebensdauer von zugänglichen Objekten überwachen.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708555"
---
# <a name="creating-proxy-objects"></a>Erstellen von Proxy Objekten

Zusätzlich zum Entwerfen von Klassen, die Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren, müssen Server Entwickler möglicherweise auch *Proxy* Objekte entwerfen, die die Lebensdauer von zugänglichen Objekten überwachen. Wenn ein Barrierefreies Objekt in einer Anwendung für den gesamten Zeitpunkt verfügbar ist, an dem die Anwendung ausgeführt wird, müssen Sie kein Proxy Objekt erstellen. Wenn es möglich ist, das barrierefreie Objekt zu zerstören, während die Anwendung ausgeführt wird, müssen Sie ein Proxy Objekt erstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Was sind Proxy Objekte?](what-are-proxy-objects.md)
-   [Warum Proxy Objekte erforderlich sind](why-proxy-objects-are-needed.md)
-   [Entwurfs Überlegungen für Proxy Objekte](design-considerations-for-proxy-objects.md)

 

 




