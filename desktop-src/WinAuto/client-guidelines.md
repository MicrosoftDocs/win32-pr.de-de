---
title: Client Richtlinien
description: Client Entwickler sollten die folgenden Funktionen verwenden, um Informationen zu den Elementen der Benutzeroberfläche zu erhalten.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103948383"
---
# <a name="client-guidelines"></a><span data-ttu-id="883a9-103">Client Richtlinien</span><span class="sxs-lookup"><span data-stu-id="883a9-103">Client Guidelines</span></span>

<span data-ttu-id="883a9-104">Client Entwickler sollten die folgenden Funktionen verwenden, um Informationen zu den Elementen der Benutzeroberfläche zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="883a9-104">Client developers should use the following functionality to get information about the user interface elements:</span></span>

-   <span data-ttu-id="883a9-105">Zum Abrufen einer [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle zu Objekten müssen Sie [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="883a9-105">To get an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface to objects, call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>
-   <span data-ttu-id="883a9-106">Verwenden Sie die Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , um barrierefreie Objekte zu überprüfen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="883a9-106">To examine and manipulate accessible objects, use the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods.</span></span>
-   <span data-ttu-id="883a9-107">Um [WinEvents](winevents-overview.md)zu empfangen, rufen Sie [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) auf, um eine WinEvent-Rückruffunktion für die Ereignisse zu registrieren, die für die Client Anwendung relevant sind.</span><span class="sxs-lookup"><span data-stu-id="883a9-107">To receive [WinEvents](winevents-overview.md), call [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) to register a WinEvent callback function for those events that are relevant to the client application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="883a9-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="883a9-108">In this section</span></span>

-   [<span data-ttu-id="883a9-109">Abrufen von untergeordneten IDs durch Clients</span><span class="sxs-lookup"><span data-stu-id="883a9-109">How Clients Obtain Child IDs</span></span>](how-clients-obtain-child-ids.md)

 

 




