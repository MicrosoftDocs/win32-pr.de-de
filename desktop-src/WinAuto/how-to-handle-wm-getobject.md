---
title: Behandeln von WM_GETOBJECT
description: Wenn eine WM \_ GETOBJECT-Nachricht empfangen wird, die OBJID \_ CLIENT enthält, muss der Server einen Zeiger auf das Objekt zurückgeben, das IAccessible implementiert.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f066ee42ffaeee2d585ac5480e5af31acf14c87ba9994d3d338b65e6cf427a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052725"
---
# <a name="how-to-handle-wm_getobject"></a>Behandeln von WM \_ GETOBJECT

Wenn eine [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) empfangen wird, die [**OBJID \_ CLIENT**](object-identifiers.md)enthält, muss der Server einen Zeiger auf das Objekt zurückgeben, das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)implementiert. Dieser Zeiger ist ein LRESULT, das durch Aufrufen von [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)abgerufen wird. Microsoft Active Accessibility führt in Verbindung mit der com-Bibliothek (Component Object Model) das entsprechende Marshalling durch und übergibt den **IAccessible-Schnittstellenzeiger** vom Server an den Client.

Server müssen die Verweiszählung für das barrierefreie Objekt ordnungsgemäß verarbeiten. Beachten Sie, dass beim Erstellen eines COM-Objekts der Verweiszähler 1 ist. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) erhöht dann den Verweiszähler mehrmals weiter. Alle von **LresultFromObject** erstellten Verweise werden automatisch freigegeben, wenn das Objekt nicht mehr benötigt wird, der Server jedoch für die Freigabe des ursprünglichen Verweises verantwortlich ist. Andernfalls wird das Objekt nie zerstört. Die Beispiele in den folgenden Abschnitten zeigen, wie Verweise auf barrierefreie Objekte veröffentlicht werden.

Server verarbeiten [**WM \_ GETOBJECT**](wm-getobject.md) in der Regel auf eine der folgenden Arten:

-   [Erstellen neuer barrierefreier Objekte](create-new-accessible-objects.md)
-   [Wiederverwenden vorhandener Zeiger auf Objekte](reuse-existing-pointers-to-objects.md)
-   [Erstellen neuer Schnittstellen für dasselbe Objekt](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> Wenn in diesem Abschnitt wie in der restlichen Dokumentation ein Zeiger auf eine [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) erläutert wird, kann dieser Zeiger tatsächlich ein Zeiger auf ein Proxyobjekt sein, das die **IAccessible-Schnittstelle** umschließt. Weitere Informationen zu Proxyobjekten finden Sie unter [Erstellen von Proxyobjekten.](creating-proxy-objects.md)

 

Eine Übersicht über [**WM \_ GETOBJECT**](wm-getobject.md)finden Sie unter Funktionsweise von [WM \_ GETOBJECT.](how-wm-getobject-works.md)

 

 




