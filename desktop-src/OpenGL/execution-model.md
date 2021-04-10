---
title: Ausführungs Modell
description: Ausführungs Modell
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, Ausführungs Modell
- Ausführungs Modell OpenGL
- OpenGL, Client/Server-Modell
- Client/Server-Modell OpenGL
- OpenGL, netzwerktransparent
- Framebuffers, Ausführungs Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947977"
---
# <a name="execution-model"></a><span data-ttu-id="1212d-109">Ausführungs Modell</span><span class="sxs-lookup"><span data-stu-id="1212d-109">Execution Model</span></span>

<span data-ttu-id="1212d-110">Das Modell für die Interpretation von OpenGL-Befehlen ist Client/Server.</span><span class="sxs-lookup"><span data-stu-id="1212d-110">The model for interpretation of OpenGL commands is client/server.</span></span> <span data-ttu-id="1212d-111">Der Anwendungscode (der Client) gibt Befehle aus, die von OpenGL (dem Server) interpretiert und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1212d-111">Application code (the client) issues commands, which are interpreted and processed by OpenGL (the server).</span></span> <span data-ttu-id="1212d-112">Der Server kann auf demselben Computer wie der Client ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1212d-112">The server may or may not operate on the same computer as the client.</span></span> <span data-ttu-id="1212d-113">In diesem Sinne ist OpenGL netzwerktransparent.</span><span class="sxs-lookup"><span data-stu-id="1212d-113">In this sense, OpenGL is network-transparent.</span></span> <span data-ttu-id="1212d-114">Ein Server kann mehrere OpenGL-Kontexte verwalten, von denen jeder ein gekapselter OpenGL-Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="1212d-114">A server can maintain several OpenGL contexts, each of which is an encapsulated OpenGL state.</span></span> <span data-ttu-id="1212d-115">Ein Client kann eine Verbindung mit einem dieser Kontexte herstellen.</span><span class="sxs-lookup"><span data-stu-id="1212d-115">A client can connect to any one of these contexts.</span></span> <span data-ttu-id="1212d-116">Das erforderliche Netzwerkprotokoll kann implementiert werden, indem ein bereits vorhandenes Protokoll (z. b. das des X-Fenstersystems) erweitert oder ein unabhängiges Protokoll verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1212d-116">The required network protocol can be implemented by augmenting an already existing protocol (such as that of the X Window System) or by using an independent protocol.</span></span> <span data-ttu-id="1212d-117">Zum Abrufen von Benutzereingaben werden keine OpenGL-Befehle bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1212d-117">No OpenGL commands are provided for obtaining user input.</span></span>

<span data-ttu-id="1212d-118">Das Fenstersystem, das Frame Puffer-Ressourcen ordnet, steuert letztendlich die Auswirkungen von OpenGL-Befehlen auf den Frame Puffer.</span><span class="sxs-lookup"><span data-stu-id="1212d-118">The window system that allocates framebuffer resources ultimately controls the effects of OpenGL commands on the framebuffer.</span></span> <span data-ttu-id="1212d-119">Das Fenstersystem:</span><span class="sxs-lookup"><span data-stu-id="1212d-119">The window system:</span></span>

-   <span data-ttu-id="1212d-120">Bestimmt, auf welche Teile des Frame Puffer OpenGL zu einem beliebigen Zeitpunkt zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="1212d-120">Determines which portions of the framebuffer OpenGL may access at any given time.</span></span>
-   <span data-ttu-id="1212d-121">Kommuniziert mit OpenGL, wie diese Teile strukturiert sind.</span><span class="sxs-lookup"><span data-stu-id="1212d-121">Communicates to OpenGL how those portions are structured.</span></span>

<span data-ttu-id="1212d-122">Daher sind keine OpenGL-Befehle zum Konfigurieren von Frame Puffer oder zum Initialisieren von OpenGL vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1212d-122">Therefore, there are no OpenGL commands to configure the framebuffer or initialize OpenGL.</span></span> <span data-ttu-id="1212d-123">Die Frame Puffer Konfiguration erfolgt außerhalb von OpenGL in Verbindung mit dem Fenstersystem. Die OpenGL-Initialisierung findet statt, wenn das Fenstersystem ein Fenster für das OpenGL-Rendering bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1212d-123">Frame buffer configuration is done outside of OpenGL in conjunction with the window system; OpenGL initialization takes place when the window system allocates a window for OpenGL rendering.</span></span>

 

 




