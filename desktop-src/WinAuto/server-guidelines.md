---
title: Server Richtlinien
description: Damit Microsoft Active Accessibility wie entworfen funktioniert, müssen die Server Barrierefreiheits Informationen für Clients bereitstellen.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388072"
---
# <a name="server-guidelines"></a>Server Richtlinien

Damit Microsoft Active Accessibility wie entworfen funktioniert, müssen die Server Barrierefreiheits Informationen für Clients bereitstellen.

Zum Implementieren von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)müssen Server Entwickler diesem grundlegenden Prozess folgen.

1.  Erstellen Sie barrierefreie Objekte, indem Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften und-Methoden für Ihre benutzerdefinierten Benutzeroberflächen Elemente und für den Client der Anwendung implementieren. Stellen Sie sicher, dass Sie eine duale Schnittstelle bereitstellen, die sowohl **IAccessible** als auch [**IDispatch**](idispatch-interface.md) unterstützt, damit Clients, die in Microsoft Visual Basic und verschiedenen Skriptsprachen geschrieben sind, Informationen zu den Objekten erhalten.
2.  Wenden Sie [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) an, um Clients über Änderungen an den benutzerdefinierten Benutzeroberflächen Elementen zu benachrichtigen.
3.  Behandeln Sie [**WM \_ GetObject**](wm-getobject.md) , um Zugriff auf die barrierefreien Objekte bereitzustellen.

Vorschläge und Richtlinien zum Entwerfen von zugänglichen Objekten finden Sie [im Entwicklerhandbuch für Active Accessibility-Server](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Implementierung von untergeordneten IDs durch Server](how-servers-implement-child-ids.md)

 

 




