---
title: Das RPC-Modell
description: Der Remote Prozedur Aufruf (RPC) für die Programmiersprachen C und C++ wurde entwickelt, um die Anforderungen von Entwicklern zu erfüllen, die an der nächsten Generation von Software für Windows-Betriebssysteme arbeiten.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, das RPC-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729416"
---
# <a name="the-rpc-model"></a><span data-ttu-id="c1108-104">Das RPC-Modell</span><span class="sxs-lookup"><span data-stu-id="c1108-104">The RPC Model</span></span>

<span data-ttu-id="c1108-105">Der Remote Prozedur Aufruf (RPC) für die Programmiersprachen C und C++ wurde entwickelt, um die Anforderungen von Entwicklern zu erfüllen, die an der nächsten Generation von Software für Windows-Betriebssysteme arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c1108-105">Remote Procedure Call (RPC) for the C and C++ programming languages is designed to help meet the needs of developers working on the next generation of software for Windows operating systems.</span></span>

<span data-ttu-id="c1108-106">RPC ist ein leistungsfähiger, stabiler, effizienter und sicherer Prozess für die prozessübergreifende Kommunikation (prozessübergreifende Communication, IPC), der den Datenaustausch und den Aufruf von Funktionen in einem anderen Prozess ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c1108-106">RPC is a powerful, robust, efficient, and secure interprocess communication (IPC) mechanism that enables data exchange and invocation of functionality residing in a different process.</span></span> <span data-ttu-id="c1108-107">Der andere Prozess kann sich auf demselben Computer, im lokalen Netzwerk oder über das Internet befinden.</span><span class="sxs-lookup"><span data-stu-id="c1108-107">That different process can be on the same machine, on the local area network, or across the Internet.</span></span> <span data-ttu-id="c1108-108">In diesem Abschnitt werden das RPC-Programmiermodell und das Modell für verteilte Systeme erläutert, die mithilfe von RPC implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="c1108-108">This section explains the RPC programming model and the model for distributed systems that can be implemented using RPC.</span></span>

<span data-ttu-id="c1108-109">RPC unterstützt 64-Bit-Windows vollständig.</span><span class="sxs-lookup"><span data-stu-id="c1108-109">RPC fully supports 64-bit Windows.</span></span> <span data-ttu-id="c1108-110">Es gibt drei Arten von Prozessen: systemeigene 32-Bit-Prozesse, native 64-Bit-Prozesse und 32-Bit-Prozesse, die unter dem 32-Bit-Prozess Emulator auf einem 64-Bit-System ausgeführt werden (häufig als WOW64 Processes bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="c1108-110">There are three types of processes: native 32-bit processes, native 64-bit processes, and 32-bit processes running under the 32-bit process emulator on a 64-bit system (often referred to as WOW64 processes).</span></span> <span data-ttu-id="c1108-111">Weitere Informationen zu WOW64 finden Sie unter [Ausführen von 32-Bit-Anwendungen](/windows/desktop/WinProg64/running-32-bit-applications).</span><span class="sxs-lookup"><span data-stu-id="c1108-111">For more information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span> <span data-ttu-id="c1108-112">Mithilfe von RPC können Entwickler zwischen verschiedenen Prozess Typen transparent kommunizieren. RPC verwaltet Prozess Unterschiede automatisch im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="c1108-112">Using RPC, developers can transparently communicate between different types of process; RPC automatically manages process differences behind the scenes.</span></span>

<span data-ttu-id="c1108-113">RPC wurde anfänglich als Erweiterung für OSF RPC entwickelt.</span><span class="sxs-lookup"><span data-stu-id="c1108-113">RPC was initially developed as an extension to OSF RPC.</span></span> <span data-ttu-id="c1108-114">Mit Ausnahme einiger erweiterter Features ist RPC mit den Implementierungen von OSF RPC anderer Hersteller interoperabel.</span><span class="sxs-lookup"><span data-stu-id="c1108-114">With the exception of some of its advanced features, RPC is interoperable with other vendors' implementations of OSF RPC.</span></span>

<span data-ttu-id="c1108-115">Dieser Abschnitt bietet auch eine Übersicht über die RPC-Komponenten und deren Betrieb.</span><span class="sxs-lookup"><span data-stu-id="c1108-115">This section also provides an overview of RPC components and their operation.</span></span> <span data-ttu-id="c1108-116">Die Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c1108-116">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="c1108-117">Das Programmiermodell</span><span class="sxs-lookup"><span data-stu-id="c1108-117">The Programming Model</span></span>](the-programming-model.md)
-   [<span data-ttu-id="c1108-118">Das Modell für verteilte Systeme</span><span class="sxs-lookup"><span data-stu-id="c1108-118">The Model for Distributed Systems</span></span>](the-model-for-distributed-systems.md)
-   [<span data-ttu-id="c1108-119">Funktionsweise von RPC</span><span class="sxs-lookup"><span data-stu-id="c1108-119">How RPC Works</span></span>](how-rpc-works.md)
-   [<span data-ttu-id="c1108-120">Microsoft RPC-Komponenten</span><span class="sxs-lookup"><span data-stu-id="c1108-120">Microsoft RPC Components</span></span>](microsoft-rpc-components.md)

 

 