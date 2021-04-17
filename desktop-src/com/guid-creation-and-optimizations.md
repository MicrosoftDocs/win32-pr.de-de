---
title: GUID-Erstellung und-Optimierungen
description: GUID-Erstellung und-Optimierungen
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388706"
---
# <a name="guid-creation-and-optimizations"></a><span data-ttu-id="4b74b-103">GUID-Erstellung und-Optimierungen</span><span class="sxs-lookup"><span data-stu-id="4b74b-103">GUID Creation and Optimizations</span></span>

<span data-ttu-id="4b74b-104">Da eine CLSID, wie z. b. ein Schnittstellen Bezeichner (IID), eine GUID ist, hat keine andere Klasse, unabhängig von der Person, die Sie schreibt, eine doppelte CLSID.</span><span class="sxs-lookup"><span data-stu-id="4b74b-104">Because a CLSID, like an interface identifier (IID), is a GUID, no other class, no matter who writes it, has a duplicate CLSID.</span></span> <span data-ttu-id="4b74b-105">Server Implementierer erhalten CLSIDs in der Regel über die [**cokreateguid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4b74b-105">Server implementers generally obtain CLSIDs through the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span> <span data-ttu-id="4b74b-106">Mit dieser Funktion werden garantiert eindeutige CLSIDs erzeugt, sodass Server Implementierungen auf der ganzen Welt Ihre Software unabhängig entwickeln und bereitstellen können, ohne dass eine versehentliche Kollision mit von anderen geschriebenen Software besteht.</span><span class="sxs-lookup"><span data-stu-id="4b74b-106">This function is guaranteed to produce unique CLSIDs, so server implementers across the world can independently develop and deploy their software without fear of accidental collision with software written by others.</span></span>

<span data-ttu-id="4b74b-107">Durch die Verwendung eindeutiger CLSIDs wird die Möglichkeit von Namenskollisionen zwischen Klassen vermieden, weil CLSIDs in keiner Weise mit den in der zugrunde liegenden Implementierung verwendeten Namen verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="4b74b-107">Using unique CLSIDs avoids the possibility of name collisions among classes because CLSIDs are in no way connected to the names used in the underlying implementation.</span></span> <span data-ttu-id="4b74b-108">Beispielsweise können zwei verschiedene Lieferanten Klassen schreiben, die als "stackclass" bezeichnet werden, aber jede verfügt über eine eindeutige CLSID und kann daher nicht verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="4b74b-108">For example, two different vendors can write classes called "StackClass," but each would have a unique CLSID and therefore could not be confused.</span></span>

<span data-ttu-id="4b74b-109">COM muss häufig GUIDs (IIDs und CLSIDs) einem beliebig großen Satz an anderen Werten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="4b74b-109">COM frequently must map GUIDs (IIDs and CLSIDs) to some arbitrarily large set of other values.</span></span> <span data-ttu-id="4b74b-110">Als Anwendungsentwickler können Sie diese Suchvorgänge beschleunigen und dadurch die Systemleistung verbessern, indem Sie die GUIDs für Ihre Anwendung als Block von aufeinander folgenden Werten erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b74b-110">As an application developer, you can help speed up such searches, and thereby enhance system performance, by generating the GUIDs for your application as a block of consecutive values.</span></span>

<span data-ttu-id="4b74b-111">Die effizienteste Möglichkeit, einen Block von aufeinander folgenden GUIDs zu generieren, besteht darin, das Hilfsprogramm "" uuidgen "mithilfe der Schalter"-n "und"-x "auszuführen, die einen Block von UUIDs generieren, wobei jeder der ersten DWORD-Werte um eins erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="4b74b-111">The most efficient way to generate a block of consecutive GUIDs is to run the uuidgen utility using the -n and -x switches, which generates a block of UUIDs, each of whose first DWORD value is incremented by one.</span></span>

<span data-ttu-id="4b74b-112">Wenn Sie z. b. eingeben.</span><span class="sxs-lookup"><span data-stu-id="4b74b-112">For example, if you were to type</span></span>

<span data-ttu-id="4b74b-113">**"uuidgen-N5-x**</span><span class="sxs-lookup"><span data-stu-id="4b74b-113">**uuidgen -n5 -x**</span></span>

<span data-ttu-id="4b74b-114">Das Hilfsprogramm "uuidgen würde einen Block von UUIDs generieren, der etwa wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="4b74b-114">the uuidgen utility would generate a block of UUIDs similar to the following:</span></span>

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

<span data-ttu-id="4b74b-115">Eine Methode zum Erstellen und Nachverfolgen von GUIDs für ein gesamtes Projekt beginnt mit dem Erstellen eines Blocks einer beliebig großen Anzahl von UUIDs, z.b. 500.</span><span class="sxs-lookup"><span data-stu-id="4b74b-115">One method for generating and tracking GUIDs for an entire project begins with generating a block of some arbitrarily large number of UUIDs, say 500.</span></span> <span data-ttu-id="4b74b-116">Wenn Sie z. b. eingeben.</span><span class="sxs-lookup"><span data-stu-id="4b74b-116">For example, if you were to type</span></span>

<span data-ttu-id="4b74b-117">**"uuidgen-N500-x > guids.txt**</span><span class="sxs-lookup"><span data-stu-id="4b74b-117">**uuidgen -n500 -x > guids.txt**</span></span>

<span data-ttu-id="4b74b-118">Das Hilfsprogramm generiert 500 aufeinander folgende UUIDs und schreibt Sie in die angegebene Textdatei.</span><span class="sxs-lookup"><span data-stu-id="4b74b-118">the utility would generate 500 consecutive UUIDs and write them to the specified text file.</span></span> <span data-ttu-id="4b74b-119">Anschließend können Sie diese Datei in der Quell Struktur überprüfen und so ein einzelnes Repository für alle GUIDs bereitstellen, die in einem Projekt verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4b74b-119">You could then check this file into your source tree, providing a single repository for all GUIDs to be used in a project.</span></span> <span data-ttu-id="4b74b-120">Da Benutzer GUIDs für ihre Teile des Projekts benötigen, können Sie die Datei Auschecken, aber viele GUIDs, die Sie benötigen, markieren, Sie als angenommen markieren und eine Notiz über den Speicherort im Code oder "Spezifikation" hinterlassen.</span><span class="sxs-lookup"><span data-stu-id="4b74b-120">As people require GUIDs for their portions of the project, they can check out the file, take however many GUIDs they need, marking them as taken and leaving a note about where in the code or "spec" they are using them.</span></span>

<span data-ttu-id="4b74b-121">Zusätzlich zur Verbesserung der Systemleistung hat das Erstellen von Blöcken von aufeinander folgenden GUIDs auf diese Weise folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="4b74b-121">In addition to improving system performance, generating blocks of consecutive GUIDs in this way has the following benefits:</span></span>

-   <span data-ttu-id="4b74b-122">Eine zentrale Datei, in der alle GUIDs für eine Anwendung enthalten sind, macht es leicht nachzuverfolgen, welche GUIDs für was und welche Personen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b74b-122">A central file containing all GUIDs for an application makes it easy to keep track of which GUIDs are for what and which people are using them.</span></span>
-   <span data-ttu-id="4b74b-123">Ein Block von aufeinander folgenden GUIDs, die einer bestimmten Anwendung zugeordnet sind, hilft Entwicklern und Testern beim Debuggen beim Erkennen interner GUIDs und erleichtert die Suche in der Systemregistrierung, da Sie sequenziell gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4b74b-123">A block of consecutive GUIDs associated with a particular application helps developers and testers recognize internal GUIDs during debugging and makes it easier to find them in the system registry because they are stored sequentially.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b74b-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b74b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b74b-125">Zuständigkeiten von com-Servern</span><span class="sxs-lookup"><span data-stu-id="4b74b-125">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 




