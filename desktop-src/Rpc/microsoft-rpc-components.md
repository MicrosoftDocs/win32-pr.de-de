---
title: RPC-Komponenten
description: Remote Prozedur Aufruf-Komponenten (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947770"
---
# <a name="rpc-components"></a><span data-ttu-id="2836d-104">RPC-Komponenten</span><span class="sxs-lookup"><span data-stu-id="2836d-104">RPC Components</span></span>

<span data-ttu-id="2836d-105">RPC umfasst die folgenden Hauptkomponenten:</span><span class="sxs-lookup"><span data-stu-id="2836d-105">RPC includes the following major components:</span></span>

-   <span data-ttu-id="2836d-106">Mittlerer l-Compiler</span><span class="sxs-lookup"><span data-stu-id="2836d-106">MIDL compiler</span></span>
-   <span data-ttu-id="2836d-107">Laufzeitbibliotheken und Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2836d-107">Run-time libraries and header files</span></span>
-   <span data-ttu-id="2836d-108">Name Service Provider (manchmal auch als Locator bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="2836d-108">Name service provider (sometimes referred to as the Locator)</span></span>
-   <span data-ttu-id="2836d-109">Endpunkt Zuordnung (manchmal auch als Port-Mapper bezeichnet)</span><span class="sxs-lookup"><span data-stu-id="2836d-109">Endpoint mapper (sometimes referred to as the port mapper)</span></span>

<span data-ttu-id="2836d-110">Im RPC-Modell können Sie eine Schnittstelle für die Remote Prozeduren formal mithilfe einer für diesen Zweck entworfenen Sprache angeben.</span><span class="sxs-lookup"><span data-stu-id="2836d-110">In the RPC model, you can formally specify an interface to the remote procedures using a language designed for this purpose.</span></span> <span data-ttu-id="2836d-111">Diese Sprache wird als Schnittstellen Definitions Sprache oder IDL bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2836d-111">This language is called the Interface Definition Language, or IDL.</span></span> <span data-ttu-id="2836d-112">Die Microsoft-Implementierung dieser Sprache wird als Microsoft Interface Definition Language oder als Mittelwert bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2836d-112">The Microsoft implementation of this language is called the Microsoft Interface Definition Language, or MIDL.</span></span>

<span data-ttu-id="2836d-113">Nachdem Sie eine Schnittstelle erstellt haben, müssen Sie Sie über den Mittelwert Compiler übergeben.</span><span class="sxs-lookup"><span data-stu-id="2836d-113">After you create an interface, you must pass it through the MIDL compiler.</span></span> <span data-ttu-id="2836d-114">Dieser Compiler generiert die stubweise, die Aufrufe von lokalen Prozeduren in Remote Prozedur Aufrufe übersetzen.</span><span class="sxs-lookup"><span data-stu-id="2836d-114">This compiler generates the stubs that translate local procedure calls into remote procedure calls.</span></span> <span data-ttu-id="2836d-115">Stubel sind Platzhalter Funktionen, die Aufrufe an die Lauf Zeit Bibliotheksfunktionen durchführen, die den Remote Prozedur Aufruf verwalten.</span><span class="sxs-lookup"><span data-stu-id="2836d-115">Stubs are placeholder functions that make the calls to the run-time library functions, which manage the remote procedure call.</span></span> <span data-ttu-id="2836d-116">Der Vorteil dieses Ansatzes besteht darin, dass das Netzwerk für Ihre verteilte Anwendung fast vollständig transparent wird.</span><span class="sxs-lookup"><span data-stu-id="2836d-116">The advantage of this approach is that the network becomes almost completely transparent to your distributed application.</span></span> <span data-ttu-id="2836d-117">Ihr Client Programm ruft auf, was als lokale Prozeduren erscheinen soll. die Arbeit, Sie in Remote aufrufen umzuwandeln, erfolgt automatisch.</span><span class="sxs-lookup"><span data-stu-id="2836d-117">Your client program calls what appear to be local procedures; the work of turning them into remote calls is done for you automatically.</span></span> <span data-ttu-id="2836d-118">Der gesamte Code, der Daten übersetzt, auf das Netzwerk zugreift und Ergebnisse abruft, wird vom Mittelwert Compiler generiert und ist für Ihre Anwendung nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="2836d-118">All the code that translates data, accesses the network, and retrieves results is generated for you by the MIDL compiler and is invisible to your application.</span></span>

 

 




