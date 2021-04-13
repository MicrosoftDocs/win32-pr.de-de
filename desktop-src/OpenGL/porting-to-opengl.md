---
title: Portieren auf OpenGL
description: Portieren auf OpenGL
ms.assetid: 6799e10b-2f7c-4516-92ea-43667784f8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8efd2a34ac5d7fb6fc52aef3f24a556712b2c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388477"
---
# <a name="porting-to-opengl"></a><span data-ttu-id="d6957-103">Portieren auf OpenGL</span><span class="sxs-lookup"><span data-stu-id="d6957-103">Porting to OpenGL</span></span>

<span data-ttu-id="d6957-104">OpenGL ist für die Kompatibilität von Hardware und Betriebssystemen hinweg konzipiert.</span><span class="sxs-lookup"><span data-stu-id="d6957-104">OpenGL is designed for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="d6957-105">Dieser Entwurf erleichtert Programmierern das Portieren von OpenGL-Programmen von einem System zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="d6957-105">This design makes it easier for programmers to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="d6957-106">Obwohl jedes Betriebssystem besondere Anforderungen erfüllt, kann ein Großteil des OpenGL-Codes in ihren aktuellen Programmen unverändert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6957-106">While each operating system has unique requirements, much of the OpenGL code in your current programs can be used as is.</span></span> <span data-ttu-id="d6957-107">Zum Portieren ihrer OpenGL-Anwendung auf Microsoft Windows müssen Sie Ihre Programme so ändern, dass Sie mit den Windows-windowingsystemen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d6957-107">To port your OpenGL application to Microsoft Windows, you'll have to modify your programs to work with the Windows windowing systems.</span></span>

<span data-ttu-id="d6957-108">In allgemeinen werden Anwendungen von einer von zwei Plattformen zu OpenGL für Windows portiert:</span><span class="sxs-lookup"><span data-stu-id="d6957-108">In general applications are ported to OpenGL for Windows from one of two platforms:</span></span>

-   <span data-ttu-id="d6957-109">Für das x-Fenster System entwickelte OpenGL-Anwendungen und die x-Bibliothek (Xlib)</span><span class="sxs-lookup"><span data-stu-id="d6957-109">OpenGL applications developed for the X Window System and the X library (Xlib)</span></span>
-   <span data-ttu-id="d6957-110">IRIS GL-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d6957-110">IRIS GL applications</span></span>

<span data-ttu-id="d6957-111">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="d6957-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d6957-112">Einführung in das Portieren in OpenGL für Windows</span><span class="sxs-lookup"><span data-stu-id="d6957-112">Introduction to Porting to OpenGL for Windows</span></span>](introduction-to-porting-to-opengl-for-windows-nt--windows-2000--and-windows-95-98.md)
-   [<span data-ttu-id="d6957-113">OpenGL-Funktionen und ihre IRIS GL-Entsprechungen</span><span class="sxs-lookup"><span data-stu-id="d6957-113">OpenGL Functions and Their IRIS GL Equivalents</span></span>](opengl-functions-and-their-iris-gl-equivalents.md)
-   [<span data-ttu-id="d6957-114">IRIS GL-und OpenGL-Unterschiede</span><span class="sxs-lookup"><span data-stu-id="d6957-114">IRIS GL and OpenGL Differences</span></span>](iris-gl-and-opengl-differences.md)

 

 




