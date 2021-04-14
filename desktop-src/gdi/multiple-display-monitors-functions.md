---
description: Die folgenden Funktionen bieten Unterstützung für mehrere Monitore.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funktionen mit mehreren Anzeige Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978536"
---
# <a name="multiple-display-monitors-functions"></a><span data-ttu-id="2e955-103">Funktionen mit mehreren Anzeige Monitoren</span><span class="sxs-lookup"><span data-stu-id="2e955-103">Multiple Display Monitors Functions</span></span>

<span data-ttu-id="2e955-104">Die folgenden Funktionen bieten Unterstützung für mehrere Monitore.</span><span class="sxs-lookup"><span data-stu-id="2e955-104">The following functions provide support for multiple monitors.</span></span>



| <span data-ttu-id="2e955-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="2e955-105">Function</span></span>                                           | <span data-ttu-id="2e955-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e955-106">Description</span></span>                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e955-107">**Enumdisplaymonitors**</span><span class="sxs-lookup"><span data-stu-id="2e955-107">**EnumDisplayMonitors**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | <span data-ttu-id="2e955-108">Listet Anzeige Monitore auf, die einen Bereich überschneiden, der durch die Schnittmenge eines angegebenen clippingrechtecks und den sichtbaren Bereich eines Geräte Kontexts gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="2e955-108">Enumerates display monitors that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context.</span></span> |
| [<span data-ttu-id="2e955-109">**Getmonitorinfo**</span><span class="sxs-lookup"><span data-stu-id="2e955-109">**GetMonitorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | <span data-ttu-id="2e955-110">Ruft Informationen zu einem Anzeige Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="2e955-110">Retrieves information about a display monitor.</span></span>                                                                                                               |
| [<span data-ttu-id="2e955-111">**Monitorenumschlag**</span><span class="sxs-lookup"><span data-stu-id="2e955-111">**MonitorEnumProc**</span></span>](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | <span data-ttu-id="2e955-112">Eine von der Funktion [**enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) aufgerufene Anwendungs definierte Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="2e955-112">An application-defined callback function that is called by the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span>                                  |
| [<span data-ttu-id="2e955-113">**MonitorFromPoint**</span><span class="sxs-lookup"><span data-stu-id="2e955-113">**MonitorFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | <span data-ttu-id="2e955-114">Ruft ein Handle für den Anzeige Monitor ab, der einen angegebenen Punkt enthält.</span><span class="sxs-lookup"><span data-stu-id="2e955-114">Retrieves a handle to the display monitor that contains a specified point.</span></span>                                                                                   |
| [<span data-ttu-id="2e955-115">**Monitorfromrect**</span><span class="sxs-lookup"><span data-stu-id="2e955-115">**MonitorFromRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | <span data-ttu-id="2e955-116">Ruft ein Handle für den Anzeige Monitor mit dem größten Bereich der Schnittmenge mit einem angegebenen Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="2e955-116">Retrieves a handle to the display monitor that has the largest area of intersection with a specified rectangle.</span></span>                                              |
| [<span data-ttu-id="2e955-117">**Monitorfromwindow**</span><span class="sxs-lookup"><span data-stu-id="2e955-117">**MonitorFromWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | <span data-ttu-id="2e955-118">Ruft ein Handle für den Anzeige Monitor mit dem größten Bereich der Schnittmenge mit dem umgebenden Rechteck eines angegebenen Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="2e955-118">Retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.</span></span>                       |



 

 

 



