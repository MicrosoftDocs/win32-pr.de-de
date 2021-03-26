---
description: Jedes Mal, wenn eine Anwendung einen Domänen Controller erstellt und sofort mit dem Aufrufen von GDI-Zeichnungs-oder-Ausgabefunktionen beginnt, nutzt Sie den standardmäßigen Seiten Raum für den Geräteraum und die Transformationen für den Geräte Speicherplatz auf dem Client Bereich.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Standard Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978688"
---
# <a name="default-transformations"></a><span data-ttu-id="a6729-103">Standard Transformationen</span><span class="sxs-lookup"><span data-stu-id="a6729-103">Default Transformations</span></span>

<span data-ttu-id="a6729-104">Jedes Mal, wenn eine Anwendung einen Domänen Controller erstellt und sofort mit dem Aufrufen von GDI-Zeichnungs-oder-Ausgabefunktionen beginnt, nutzt Sie den standardmäßigen Seiten Raum für den Geräteraum und die Transformationen für den Geräte Speicherplatz auf dem Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="a6729-104">Whenever an application creates a DC and immediately begins calling GDI drawing or output functions, it takes advantage of the default page-space to device-space, and device-space to client-area transformations.</span></span> <span data-ttu-id="a6729-105">Eine Transformation für Welt-zu-Seite-Speicherplatz kann erst auftreten, wenn die Anwendung die [**setgraphicsmode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) -Funktion aufruft, um den Modus auf "GM Advanced" festzulegen, \_ und dann die Funktion " [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="a6729-105">A world-to-page space transformation cannot happen until the application first calls the [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) function to set the mode to GM\_ADVANCED and then calls the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function.</span></span>

<span data-ttu-id="a6729-106">Die Verwendung von mm \_ -Text (die standardmäßige Transformation für den Seiten Raum für den Geräteraum) führt zu einer eins-zu-Eins-Zuordnung, d. h. ein angegebener Punkt im Seiten Raum wird dem gleichen Punkt im Geräteraum zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a6729-106">Use of MM\_TEXT (the default page-space to device-space transformation) results in a one-to-one mapping; that is, a given point in page space maps to the same point in device space.</span></span> <span data-ttu-id="a6729-107">Wie bereits erwähnt, wird diese Transformation nicht durch eine Matrix angegeben.</span><span class="sxs-lookup"><span data-stu-id="a6729-107">As previously mentioned, this transformation is not specified by a matrix.</span></span> <span data-ttu-id="a6729-108">Stattdessen wird Sie durch Aufteilen der Breite des Viewports durch die Breite des Fensters und durch die Höhe des Viewports um die Höhe des Fensters erreicht.</span><span class="sxs-lookup"><span data-stu-id="a6729-108">Instead, it is obtained by dividing the width of the viewport by the width of the window and the height of the viewport by the height of the window.</span></span> <span data-ttu-id="a6729-109">Im Standardfall sind die Viewport-Dimensionen 1 Pixel und 1 Pixel, und die Fenster Dimensionen sind 1-Seiten-Einheit um 1-Seiteneinheit.</span><span class="sxs-lookup"><span data-stu-id="a6729-109">In the default case, the viewport dimensions are 1-pixel by 1-pixel and the window dimensions are 1-page unit by 1-page unit.</span></span>

<span data-ttu-id="a6729-110">Die Transformation für den Geräte Speicherplatz zu physischem Gerät (Client Bereich, Desktop oder Drucker) führt immer zu einer eins-zu-Eins-Zuordnung. Das heißt, eine Einheit im Gerätebereich entspricht immer einer Einheit im Client Bereich, auf dem Desktop oder auf einer Seite.</span><span class="sxs-lookup"><span data-stu-id="a6729-110">The device-space to physical-device (client area, desktop, or printer paper) transformation always results in a one-to-one mapping; that is, one unit in device space is always equivalent to one unit in the client area, on the desktop, or on a page.</span></span> <span data-ttu-id="a6729-111">Der einzige Zweck dieser Transformation ist die Übersetzung. Dadurch wird sichergestellt, dass die Ausgabe ordnungsgemäß im Fenster einer Anwendung angezeigt wird, unabhängig davon, wo das Fenster auf dem Desktop verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a6729-111">The sole purpose of this transformation is translation; it ensures that output appears correctly in an application's window no matter where that window is moved on the desktop.</span></span>

<span data-ttu-id="a6729-112">Der einzige eindeutige Aspekt von mm \_ -Text ist die Ausrichtung der y-Achse im Seitenbereich.</span><span class="sxs-lookup"><span data-stu-id="a6729-112">The one unique aspect of MM\_TEXT is the orientation of the y-axis in page space.</span></span> <span data-ttu-id="a6729-113">In mm \_ -Text wird die positive y-Achse nach unten erweitert, und die negative y-Achse wird aufwärts erweitert.</span><span class="sxs-lookup"><span data-stu-id="a6729-113">In MM\_TEXT, the positive y-axis extends downward and the negative y-axis extends upward.</span></span>

 

 



