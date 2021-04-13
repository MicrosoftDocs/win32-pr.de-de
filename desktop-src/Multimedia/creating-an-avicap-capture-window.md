---
title: Erstellen eines avicap-Erfassungs Fensters
description: Erstellen eines avicap-Erfassungs Fensters
ms.assetid: a1418e98-f16d-401a-94a7-64fb272a39e2
keywords:
- capkreatecapturewindow-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d035d44b8d0b46df31afa5c3235e59286121c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309683"
---
# <a name="creating-an-avicap-capture-window"></a><span data-ttu-id="5ea02-104">Erstellen eines avicap-Erfassungs Fensters</span><span class="sxs-lookup"><span data-stu-id="5ea02-104">Creating an AVICap Capture Window</span></span>

<span data-ttu-id="5ea02-105">Sie können ein Aufzeichnungs Fenster der avicap-Fenster Klasse erstellen, indem Sie die [**capanatecapturewindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ea02-105">You can create a capture window of the AVICap window class by using the [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) function.</span></span> <span data-ttu-id="5ea02-106">Diese Funktion gibt ein Fenster Handle zurück, das das Aufzeichnungs Fenster identifiziert und von einer Anwendung verwendet wird, um nachfolgende Nachrichten an das Fenster zu senden.</span><span class="sxs-lookup"><span data-stu-id="5ea02-106">This function returns a window handle that identifies the capture window and is used by an application to send subsequent messages to the window.</span></span>

<span data-ttu-id="5ea02-107">Sie können ein oder mehrere Erfassungsfenster in einer Anwendung erstellen und jedes Aufzeichnungs Fenster mit einem anderen Erfassungsgerät verbinden.</span><span class="sxs-lookup"><span data-stu-id="5ea02-107">You can create one or more capture windows in an application and connect each capture window to a different capture device.</span></span>

 

 




