---
title: Das Programmiermodell
description: In den ersten Tagen der Computerprogrammierung wurde jedes Programm als großer monolithischer Block geschrieben, der mit goto-Anweisungen gefüllt wurde.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710895"
---
# <a name="the-programming-model"></a><span data-ttu-id="34e25-103">Das Programmiermodell</span><span class="sxs-lookup"><span data-stu-id="34e25-103">The Programming Model</span></span>

<span data-ttu-id="34e25-104">In den ersten Tagen der Computerprogrammierung wurde jedes Programm als großer monolithischer Block geschrieben, der mit **goto** -Anweisungen gefüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="34e25-104">In the early days of computer programming, each program was written as a large monolithic chunk, filled with **goto** statements.</span></span> <span data-ttu-id="34e25-105">Jedes Programm musste seine eigene Eingabe und Ausgabe auf verschiedenen Hardware Geräten verwalten.</span><span class="sxs-lookup"><span data-stu-id="34e25-105">Each program had to manage its own input and output to different hardware devices.</span></span> <span data-ttu-id="34e25-106">Als die Programmier Disziplin gereift ist, war dieser monolithische Code in Prozeduren organisiert, wobei die am häufigsten verwendeten Prozeduren in Bibliotheken für Freigabe und Wiederverwendung gepackt wurden.</span><span class="sxs-lookup"><span data-stu-id="34e25-106">As the programming discipline matured, this monolithic code was organized into procedures, with the most commonly used procedures packed in libraries for sharing and reuse.</span></span>

![monolithische goto-Anweisungen und Prozeduren in freigegebenen Bibliotheken verpackt](images/prog-a06.png)

<span data-ttu-id="34e25-108">Die Programmiersprache C unterstützt die Prozedur orientierte Programmierung.</span><span class="sxs-lookup"><span data-stu-id="34e25-108">The C programming language supports procedure-oriented programming.</span></span> <span data-ttu-id="34e25-109">In C bezieht sich die Haupt Prozedur auf alle anderen Prozeduren als schwarze Felder.</span><span class="sxs-lookup"><span data-stu-id="34e25-109">In C, the main procedure relates to all other procedures as black boxes.</span></span> <span data-ttu-id="34e25-110">Die Main-Prozedur kann z. B. nicht ermitteln, wie die Prozeduren A, B und X ihre Arbeit erledigen.</span><span class="sxs-lookup"><span data-stu-id="34e25-110">For example, the main procedure cannot find out how procedures A, B, and X do their work.</span></span> <span data-ttu-id="34e25-111">In der Main-Prozedur wird nur eine andere Prozedur aufgerufen. Sie enthält keine Informationen zur Implementierung dieser Prozedur.</span><span class="sxs-lookup"><span data-stu-id="34e25-111">The main procedure only calls another procedure; it has no information about how that procedure is implemented.</span></span>

![Isolation von Aktivitäten, die in externen Prozeduren ausgeführt werden](images/prog-a08.png)

<span data-ttu-id="34e25-113">Prozedur orientierte Programmiersprachen bieten einfache Mechanismen zum angeben und Schreiben von Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="34e25-113">Procedure-oriented programming languages provide simple mechanisms for specifying and writing procedures.</span></span> <span data-ttu-id="34e25-114">Beispielsweise ist der ANSI-Standard-C-Funktionsprototyp ein Konstrukt, mit dem der Name einer Prozedur, der Typ des Ergebnisses, das zurückgegeben wird (sofern vorhanden) und die Anzahl, Sequenz und der Typ der Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="34e25-114">For example, the ANSI-standard C-function prototype is a construct used to specify the name of a procedure, the type of the result it returns (if any) and the number, sequence, and type of its parameters.</span></span> <span data-ttu-id="34e25-115">Die Verwendung des Funktions Prototyps ist eine formale Methode zum Angeben einer Schnittstelle zwischen Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="34e25-115">Using the function prototype is a formal way to specify an interface between procedures.</span></span>

<span data-ttu-id="34e25-116">Microsoft RPC baut auf diesem Programmiermodell auf, indem es in Schnittstellen gruppierte Prozeduren zulässt, die sich in verschiedenen Prozessen befinden als der Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="34e25-116">Microsoft RPC builds on that programming model by allowing procedures, grouped together in interfaces, to reside in different processes than the caller.</span></span> <span data-ttu-id="34e25-117">Microsoft RPC fügt auch einen formelleren Ansatz für die Prozedur Definition hinzu, der es dem Aufrufer und der aufgerufenen Routine ermöglicht, einen Vertrag zum Remote austauschen von Daten und Aufrufen von Funktionen zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="34e25-117">Microsoft RPC also adds a more formal approach to procedure definition that allows the caller and the called routine to adopt a contract for remotely exchanging data and invoking functionality.</span></span> <span data-ttu-id="34e25-118">Im Microsoft RPC-Programmiermodell werden herkömmliche Funktionsaufrufe mit zwei zusätzlichen Elementen ergänzt.</span><span class="sxs-lookup"><span data-stu-id="34e25-118">In the Microsoft RPC programming model, traditional function calls are supplemented with two additional elements.</span></span>

-   <span data-ttu-id="34e25-119">Das erste Element ist eine IDL-/ACF-Datei, die den Datenaustausch und den Parameter Übergabe Mechanismus zwischen dem Aufrufer und der aufgerufenen Prozedur genau beschreibt.</span><span class="sxs-lookup"><span data-stu-id="34e25-119">The first element is an .idl/.acf file that precisely describes the data exchange and parameter-passing mechanism between the caller and called procedure.</span></span>
-   <span data-ttu-id="34e25-120">Das zweite Element ist ein Satz von Lauf Zeit-APIs, die Entwicklern eine genaue Kontrolle über den Remote Prozedur Aufruf bieten, einschließlich Sicherheitsaspekten, der Verwaltung des Zustands auf dem Server, der Angabe, welche Clients mit dem Server kommunizieren können usw.</span><span class="sxs-lookup"><span data-stu-id="34e25-120">The second element is a set of run-time APIs that provide developers with granular control of the remote procedure call, including security aspects, managing state on the server, specifying which clients can talk to the server, and so on.</span></span>

 

 




