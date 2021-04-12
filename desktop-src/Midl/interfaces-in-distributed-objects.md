---
title: Schnittstellen in verteilten Objekten
description: Bei der verteilten Verarbeitung ist eine Schnittstelle eine Auflistung von Definitionen und Remote Funktionen, die zwei oder mehr Programmen die Interaktion zwischen verschiedenen Kontexten ermöglicht.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- Schnittstellen-Mittell, in verteilten Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314991"
---
# <a name="interfaces-in-distributed-objects"></a><span data-ttu-id="bb403-104">Schnittstellen in verteilten Objekten</span><span class="sxs-lookup"><span data-stu-id="bb403-104">Interfaces in Distributed Objects</span></span>

<span data-ttu-id="bb403-105">Bei der verteilten Verarbeitung ist eine Schnittstelle eine Auflistung von Definitionen und Remote Funktionen, die zwei oder mehr Programmen die Interaktion zwischen verschiedenen Kontexten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="bb403-105">In distributed computing, an interface is a collection of definitions and remote functions that enables two or more programs to interoperate between different contexts.</span></span> <span data-ttu-id="bb403-106">In einer RPC-Anwendung gibt eine Schnittstelle Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="bb403-106">In an RPC application, an interface specifies:</span></span>

-   <span data-ttu-id="bb403-107">Die Art und Weise, wie sich Client-und Server Anwendungen untereinander identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bb403-107">How client and server applications identify themselves to each other.</span></span>
-   <span data-ttu-id="bb403-108">Wie Daten zwischen Client und Server übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="bb403-108">How data is transmitted between client and server.</span></span>
-   <span data-ttu-id="bb403-109">Remote Prozeduren, die von der Client Anwendung aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="bb403-109">Remote procedures that the client application can call.</span></span>
-   <span data-ttu-id="bb403-110">Datentypen für die Parameter und Rückgabewerte der Remote Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="bb403-110">Data types for the parameters and return values of the remote procedures.</span></span>

<span data-ttu-id="bb403-111">Der Microsoft Interface Definition Language (Mittelwert) dient zum Implementieren von Schnittstellen, die in verteilten Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb403-111">The Microsoft Interface Definition Language (MIDL) is for implementing interfaces used in distributed applications.</span></span> <span data-ttu-id="bb403-112">Mit mittlerer l kann eine Anwendung über eine oder mehrere Schnittstellen verfügen.</span><span class="sxs-lookup"><span data-stu-id="bb403-112">With MIDL, an application can have one interface or many.</span></span> <span data-ttu-id="bb403-113">Jede Schnittstelle gibt einen eindeutigen verteilten Vertrag zwischen den Client-und Serverprogrammen an.</span><span class="sxs-lookup"><span data-stu-id="bb403-113">Each interface specifies a unique distributed contract between the client and server programs.</span></span> <span data-ttu-id="bb403-114">Anwendungen, die auf Remote Prozedur aufrufen (RPC), Component Object Model (com) und verteiltem Component Object Model (DCOM) basieren, geben ihre Schnittstellen mithilfe von "Mittel l" an.</span><span class="sxs-lookup"><span data-stu-id="bb403-114">Applications based on remote procedure calls (RPC), Component Object Model (COM), and Distributed Component Object Model (DCOM) specify their interfaces using MIDL.</span></span>

<span data-ttu-id="bb403-115">"Mittel l" ähnelt C und C++ in vielerlei Hinsicht.</span><span class="sxs-lookup"><span data-stu-id="bb403-115">MIDL resembles C and C++ in many ways.</span></span> <span data-ttu-id="bb403-116">Eine Übersicht über das Schreiben von Mittel l-Schnittstellen finden Sie unter [entwickeln der-Schnittstelle](/windows/desktop/Rpc/developing-the-interface).</span><span class="sxs-lookup"><span data-stu-id="bb403-116">For an overview of writing MIDL interfaces, see [Developing the Interface](/windows/desktop/Rpc/developing-the-interface).</span></span>

 

 