---
title: Behandeln von WM_GETOBJECT
description: Wenn eine WM- \_ GetObject-Nachricht empfangen wird, die den objID- \_ Client enthält, muss der Server einen Zeiger auf das Objekt zurückgeben, das IAccessible implementiert.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711717"
---
# <a name="how-to-handle-wm_getobject"></a>Behandeln von WM- \_ GetObject

Wenn eine WM- [**\_ GetObject**](wm-getobject.md) -Nachricht empfangen wird, die den [**objID- \_ Client**](object-identifiers.md)enthält, muss der Server einen Zeiger auf das Objekt zurückgeben, das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert. Dieser Zeiger ist ein LRESULT, das durch den Aufruf von [**lresultfro"bject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)" abgerufen wird. Microsoft Active Accessibility führt in Verbindung mit der Component Object Model (com)-Bibliothek das entsprechende Marshalling durch und übergibt den **IAccessible** -Schnittstellen Zeiger vom Server an den Client.

Server müssen die Verweis Zählung für das barrierefreie Objekt ordnungsgemäß behandeln. Beachten Sie, dass beim Erstellen eines COM-Objekts der Verweis Zähler 1 ist. [**Lresultfromuject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) erhöht den Verweis Zähler dann mehrmals. Alle von **lresultfropbject** erstellten Verweise werden automatisch freigegeben, wenn das Objekt nicht mehr benötigt wird. der Server ist jedoch für die Freigabe des ersten Verweises verantwortlich. sofern dies nicht der Fall ist, wird das Objekt nie zerstört. In den Beispielen in den folgenden Abschnitten wird gezeigt, wie Verweise auf barrierefreie Objekte freigegeben werden.

Server behandeln die [**WM- \_ GetObject**](wm-getobject.md) -Server in der Regel mit einer der folgenden Methoden:

-   [Neue barrierefreie Objekte erstellen](create-new-accessible-objects.md)
-   [Wieder verwenden vorhandener Zeiger auf Objekte](reuse-existing-pointers-to-objects.md)
-   [Erstellen neuer Schnittstellen für dasselbe Objekt](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> Wenn in diesem Abschnitt in der restlichen Dokumentation ein Zeiger auf eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle erläutert wird, ist dieser Zeiger möglicherweise ein Zeiger auf ein Proxy Objekt, das die **IAccessible** -Schnittstelle umschließt. Weitere Informationen zu Proxy Objekten finden Sie unter [Erstellen von Proxy Objekten](creating-proxy-objects.md).

 

Eine Übersicht über [**WM \_ GetObject**](wm-getobject.md)finden Sie unter [Funktionsweise von "WM \_ GetObject](how-wm-getobject-works.md)".

 

 




