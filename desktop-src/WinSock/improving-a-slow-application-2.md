---
description: In diesem Abschnitt wird ein Teil einer Beispielanwendung untersucht, die sehr langsam über das Netzwerk ausgeführt wird. In diesem Abschnitt werden Änderungen am ursprünglichen Code vorgenommen, um die Leistung zu verbessern.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Verbessern einer langsamen Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360036"
---
# <a name="improving-a-slow-application"></a><span data-ttu-id="7f117-104">Verbessern einer langsamen Anwendung</span><span class="sxs-lookup"><span data-stu-id="7f117-104">Improving a Slow Application</span></span>

<span data-ttu-id="7f117-105">In diesem Abschnitt wird ein Teil einer Beispielanwendung untersucht, die sehr langsam über das Netzwerk ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f117-105">This section examines a portion of a sample application that operates over the network very slowly.</span></span> <span data-ttu-id="7f117-106">In diesem Abschnitt werden Änderungen am ursprünglichen Code vorgenommen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7f117-106">Throughout this section, modifications are made to the initial code to improve its performance.</span></span>

<span data-ttu-id="7f117-107">Das Mock-Beispiel ist der aktualisierte Teil für ein Spiel namens "Life".</span><span class="sxs-lookup"><span data-stu-id="7f117-107">The mock sample is the updated portion for a game called Life.</span></span> <span data-ttu-id="7f117-108">Die Anwendung wird so geschrieben, dass der Client die Berechnungen für die Updates ausführt und Sie an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="7f117-108">The application is written such that the client performs the calculations for the updates and sends them to the server.</span></span> <span data-ttu-id="7f117-109">Der Server zeigt dann das resultierende Lebensfeld an.</span><span class="sxs-lookup"><span data-stu-id="7f117-109">The server then displays the resulting Life field.</span></span> <span data-ttu-id="7f117-110">Bei der Ausgabe des Clients handelt es sich um einen Bytestream, der in dreies (dreiplets) gruppiert ist, wobei jedes einzelne Paar ein einzelnes Zellen Update darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f117-110">The output from the client is a stream of bytes, grouped in threes (triplets), each triplet representing one cell update.</span></span> <span data-ttu-id="7f117-111">Die Bytes im Dreieck stellen die Zeile, Spalte und den Wert für die Zelle dar.</span><span class="sxs-lookup"><span data-stu-id="7f117-111">The bytes in the triplet represent the row, column, and value, respectively, for the cell.</span></span>

<span data-ttu-id="7f117-112">Dieses Beispiel beginnt als absichtlich schlechte Anwendung, die die Baseline bietet, von der Leistungsverbesserungen veranschaulicht werden können.</span><span class="sxs-lookup"><span data-stu-id="7f117-112">This sample begins as an intentionally poor performing application, which provides the baseline from which performance improvements can be illustrated.</span></span> <span data-ttu-id="7f117-113">Von dort wird der Code dreimal verbessert, um verschiedene Probleme zu beheben, die sich auf die Leistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="7f117-113">From there, the code is improved three times to address various issues that affect performance.</span></span> <span data-ttu-id="7f117-114">Diese Beispiele sollten in der richtigen Reihenfolge gelesen werden, da sich jede Iterations Zeit auf der vorherigen Version verbessert.</span><span class="sxs-lookup"><span data-stu-id="7f117-114">These samples should be read in order, as each iteration improves on the previous version.</span></span>

<span data-ttu-id="7f117-115">Der grundlegende Code und die Revisionen, die diesen Code verbessern, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7f117-115">The baseline code, and the revisions that improve that code, are the following:</span></span>

-   [<span data-ttu-id="7f117-116">Baselineversion: eine sehr schlechte leistungsfähige Anwendung</span><span class="sxs-lookup"><span data-stu-id="7f117-116">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
-   [<span data-ttu-id="7f117-117">Revision 1: Bereinigen der offensichtlichen</span><span class="sxs-lookup"><span data-stu-id="7f117-117">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
-   [<span data-ttu-id="7f117-118">Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="7f117-118">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
-   [<span data-ttu-id="7f117-119">Revision 3: komprimierte Block-Sendevorgang</span><span class="sxs-lookup"><span data-stu-id="7f117-119">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
-   [<span data-ttu-id="7f117-120">Zukünftige Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7f117-120">Future Improvements</span></span>](future-improvements-2.md)

> [!WARNING]
> <span data-ttu-id="7f117-121">Die ersten Beispiele der Anwendung sorgen für eine absichtlich schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="7f117-121">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="7f117-122">Verwenden Sie diese Codebeispiele nicht in Ihrer Anwendung. Sie dienen nur zur Veranschaulichung.</span><span class="sxs-lookup"><span data-stu-id="7f117-122">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7f117-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f117-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f117-124">Hochleistungsfähige Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7f117-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



