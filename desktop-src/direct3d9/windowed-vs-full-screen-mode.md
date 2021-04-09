---
description: 'Direct3D-Anwendungen können in einem von zwei Modi ausgeführt werden: Vollbild oder Fenster.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Fenster-vs-Full-Screen Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123848"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a><span data-ttu-id="34f51-103">Fenster-vs-Full-Screen Modus (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="34f51-103">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>

<span data-ttu-id="34f51-104">Direct3D-Anwendungen können in einem von zwei Modi ausgeführt werden: Vollbild oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="34f51-104">Direct3D applications can run in either of two modes: full-screen or windowed.</span></span>

<span data-ttu-id="34f51-105">Der Vollbildmodus bedeutet, dass das Fenster, in dem die Anwendung ausgeführt wird, den gesamten Desktop abdeckt und alle ausgeführten Anwendungen (einschließlich Ihrer Entwicklungsumgebung) verbirgt.</span><span class="sxs-lookup"><span data-stu-id="34f51-105">Full-screen mode means the window that the application runs in covers the entire desktop, hiding all running applications (including your development environment).</span></span> <span data-ttu-id="34f51-106">Spiele werden in der Regel standardmäßig auf den Vollbildmodus festgestellt, um den Benutzer vollständig in das Spiel zu eintauchen</span><span class="sxs-lookup"><span data-stu-id="34f51-106">Games typically default to full-screen mode to fully immerse the user in the game by hiding all running applications.</span></span> <span data-ttu-id="34f51-107">Eine Anwendung, die im Fenstermodus ausgeführt wird, teilt den Desktop mit allen laufenden Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="34f51-107">An application running in windowed-mode shares the desktop with all running applications.</span></span> <span data-ttu-id="34f51-108">Code Unterschiede zwischen dem Vollbildmodus und dem Fenstermodus sind sehr gering.</span><span class="sxs-lookup"><span data-stu-id="34f51-108">Code differences between full-screen mode and windowed mode are very small.</span></span>

<span data-ttu-id="34f51-109">Da eine Anwendung, die im Vollbildmodus ausgeführt wird, den Bildschirm übernimmt, erfordert das Debuggen der Anwendung entweder einen separaten Monitor oder einen Remote Debugger.</span><span class="sxs-lookup"><span data-stu-id="34f51-109">Because an application running in full-screen mode takes over the screen, debugging the application requires either a separate monitor or the use of a remote debugger.</span></span> <span data-ttu-id="34f51-110">Verwenden Sie das [System Steuerungs Tool DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) , um das Debuggen mit mehreren Monitoren zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="34f51-110">Use the [DirectX Control Panel Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) to enable multiple-monitor debugging.</span></span> <span data-ttu-id="34f51-111">Ein Vorteil einer Anwendung im Windowed-Modus besteht darin, dass Sie den Code in einem Debugger ohne mehrere Monitore oder einen Remote Debugger schrittweise durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="34f51-111">One advantage of a windowed-mode application is that you can step through the code in a debugger without multiple monitors or a remote debugger.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34f51-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34f51-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34f51-113">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="34f51-113">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 



