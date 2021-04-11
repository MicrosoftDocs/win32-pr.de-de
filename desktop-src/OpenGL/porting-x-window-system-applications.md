---
title: Portieren von System Anwendungen für X-Fenster
description: Portieren von System Anwendungen für X-Fenster
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL unter Windows, portieren
- Portieren auf OpenGL, X Window System
- OpenGL-Portierung, X-Fenster System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206856"
---
# <a name="porting-x-window-system-applications"></a><span data-ttu-id="9a163-106">Portieren von System Anwendungen für X-Fenster</span><span class="sxs-lookup"><span data-stu-id="9a163-106">Porting X Window System Applications</span></span>

<span data-ttu-id="9a163-107">Wie bei Windows ist das X-Fenstersystem ein Nachrichten basiertes System, das Fenster Steuerelemente und Menüs verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a163-107">Like Windows, the X Window System is an event-handling, message-based system that uses window controls and menus.</span></span> <span data-ttu-id="9a163-108">Der OpenGL-Code in der X-Fenster System Anwendung befindet sich wahrscheinlich in Bereichen, die in etwa so aussehen, wo Sie angezeigt werden, wenn Sie Sie in Windows portieren.</span><span class="sxs-lookup"><span data-stu-id="9a163-108">The OpenGL code in your X Window System application is probably located in areas that roughly correspond to where it will appear when you port it to Windows.</span></span> <span data-ttu-id="9a163-109">Der größte Teil Ihres OpenGL-Codes ändert sich nicht, aber Sie müssen jeden Code neu schreiben, der für das X-Fenster System spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="9a163-109">Most of your OpenGL code will not change, but you must rewrite any code that is specific to the X Window System.</span></span>

<span data-ttu-id="9a163-110">**Verwenden Sie das folgende allgemeine Verfahren, um die OpenGL-Programme des X-Fensters auf Windows zu portieren.**</span><span class="sxs-lookup"><span data-stu-id="9a163-110">**Use the following general procedure to port your X Window System OpenGL programs to Windows**</span></span>

1.  <span data-ttu-id="9a163-111">Schreiben Sie den System spezifischen Code des X-Fensters mit dem entsprechenden Windows-Code um.</span><span class="sxs-lookup"><span data-stu-id="9a163-111">Rewrite the X Window System specific code using equivalent Windows code.</span></span> <span data-ttu-id="9a163-112">Suchen Sie den Code zum Erstellen von Fenstern und zur Ereignis Behandlung.</span><span class="sxs-lookup"><span data-stu-id="9a163-112">Locate window-creation and event-handling code.</span></span> <span data-ttu-id="9a163-113">Das X-Fenster System und Windows sind Ereignis Behandlung, Nachrichten basierte windowingsysteme, mit denen Sie leichter bestimmen können, wo die entsprechenden Änderungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="9a163-113">The X Window System and Windows are event-handling, message-based windowing systems, which makes it easier to determine where to make the appropriate changes.</span></span> <span data-ttu-id="9a163-114">(Insbesondere bei großen Anwendungen kann das Umschreiben einer Anwendung von einem Betriebssystem zu einem anderen eine komplexe und schwierige Aufgabe darstellen.)</span><span class="sxs-lookup"><span data-stu-id="9a163-114">(However, especially for large applications, rewriting an application from one operating system to another can be a complex and difficult undertaking.)</span></span>
2.  <span data-ttu-id="9a163-115">Suchen Sie nach Code, der glx-Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a163-115">Locate any code that uses GLX functions.</span></span> <span data-ttu-id="9a163-116">Dabei handelt es sich um die Funktionen, die Sie in die entsprechenden Windows-Funktionen übersetzen.</span><span class="sxs-lookup"><span data-stu-id="9a163-116">These are the functions you'll translate to their equivalent Windows functions.</span></span>
3.  <span data-ttu-id="9a163-117">Übersetzen Sie glx-Pixel Formatfunktionen und visuelle/drawable-Funktionen in entsprechende Windows/OpenGL-Pixel Formate und Gerätekontext Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9a163-117">Translate GLX pixel format functions and Visual/Drawable functions to appropriate Windows/OpenGL pixel format and device context functions.</span></span>
4.  <span data-ttu-id="9a163-118">Übersetzt die glx-renderingkontextfunktionen in Windows/OpenGL-Rendering-Kontextfunktionen</span><span class="sxs-lookup"><span data-stu-id="9a163-118">Translate GLX rendering context functions to Windows/OpenGL rendering context functions.</span></span>
5.  <span data-ttu-id="9a163-119">Übersetzt die glx-pixmap-Funktionen in äquivalente Windows-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9a163-119">Translate GLX Pixmap functions to equivalent Windows functions.</span></span>
6.  <span data-ttu-id="9a163-120">Übersetzen Sie glx Frame Puffer und andere glx-Funktionen in die entsprechenden Windows-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9a163-120">Translate GLX framebuffer and other GLX functions to the appropriate Windows functions.</span></span>

 

 




