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
# <a name="server-guidelines"></a><span data-ttu-id="d65e4-103">Server Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d65e4-103">Server Guidelines</span></span>

<span data-ttu-id="d65e4-104">Damit Microsoft Active Accessibility wie entworfen funktioniert, müssen die Server Barrierefreiheits Informationen für Clients bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d65e4-104">For Microsoft Active Accessibility to work as designed, servers must provide accessibility information to clients.</span></span>

<span data-ttu-id="d65e4-105">Zum Implementieren von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)müssen Server Entwickler diesem grundlegenden Prozess folgen.</span><span class="sxs-lookup"><span data-stu-id="d65e4-105">To implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), server developers must follow this basic process.</span></span>

1.  <span data-ttu-id="d65e4-106">Erstellen Sie barrierefreie Objekte, indem Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften und-Methoden für Ihre benutzerdefinierten Benutzeroberflächen Elemente und für den Client der Anwendung implementieren.</span><span class="sxs-lookup"><span data-stu-id="d65e4-106">Create accessible objects by implementing the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods for your custom user interface elements and for your application's client.</span></span> <span data-ttu-id="d65e4-107">Stellen Sie sicher, dass Sie eine duale Schnittstelle bereitstellen, die sowohl **IAccessible** als auch [**IDispatch**](idispatch-interface.md) unterstützt, damit Clients, die in Microsoft Visual Basic und verschiedenen Skriptsprachen geschrieben sind, Informationen zu den Objekten erhalten.</span><span class="sxs-lookup"><span data-stu-id="d65e4-107">Be sure to provide a dual interface that supports both **IAccessible** and [**IDispatch**](idispatch-interface.md) so that clients written in Microsoft Visual Basic and various scripting languages can get information about the objects.</span></span>
2.  <span data-ttu-id="d65e4-108">Wenden Sie [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) an, um Clients über Änderungen an den benutzerdefinierten Benutzeroberflächen Elementen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="d65e4-108">Call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to notify clients of changes to your custom user interface elements.</span></span>
3.  <span data-ttu-id="d65e4-109">Behandeln Sie [**WM \_ GetObject**](wm-getobject.md) , um Zugriff auf die barrierefreien Objekte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d65e4-109">Handle [**WM\_GETOBJECT**](wm-getobject.md) to provide access to your accessible objects.</span></span>

<span data-ttu-id="d65e4-110">Vorschläge und Richtlinien zum Entwerfen von zugänglichen Objekten finden Sie [im Entwicklerhandbuch für Active Accessibility-Server](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="d65e4-110">For suggestions and guidelines for designing accessible objects, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d65e4-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d65e4-111">In this section</span></span>

-   [<span data-ttu-id="d65e4-112">Implementierung von untergeordneten IDs durch Server</span><span class="sxs-lookup"><span data-stu-id="d65e4-112">How Servers Implement Child IDs</span></span>](how-servers-implement-child-ids.md)

 

 




