---
description: Ein Parser ist die Netzwerkmonitor Komponente, die Daten in einer verzögerten Erfassung überprüft und bestimmte Protokollinformationen an die Anwendung übergibt, die den Parser aufruft. Ein Parser ist passiv, da er nur funktioniert, wenn Netzwerkmonitor oder ein Experte ihn aufruft.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861991"
---
# <a name="parser"></a><span data-ttu-id="15a54-104">Parser</span><span class="sxs-lookup"><span data-stu-id="15a54-104">Parser</span></span>

<span data-ttu-id="15a54-105">Ein Parser ist die Netzwerkmonitor Komponente, die Daten in einer [*verzögerten Erfassung*](d.md)überprüft und bestimmte Protokollinformationen an die Anwendung übergibt, die den Parser aufruft.</span><span class="sxs-lookup"><span data-stu-id="15a54-105">A parser is the Network Monitor component that inspects data in a [*delayed capture*](d.md), and passes specific protocol information to the application that calls the parser.</span></span> <span data-ttu-id="15a54-106">Ein Parser ist passiv, da er nur funktioniert, wenn Netzwerkmonitor oder ein [*Experte*](e.md) ihn aufruft.</span><span class="sxs-lookup"><span data-stu-id="15a54-106">A parser is passive because it works only when Network Monitor or an [*expert*](e.md) call it.</span></span>

<span data-ttu-id="15a54-107">Jeder Parser identifiziert ein Protokoll, und in der Regel wird ein Parser in seiner eigenen Parser-DLL implementiert.</span><span class="sxs-lookup"><span data-stu-id="15a54-107">Each parser identifies one protocol, and typically, a parser is implemented within its own parser DLL.</span></span> <span data-ttu-id="15a54-108">Eine Parser-DLL kann jedoch mehrere Parser enthalten. Dies bedeutet, dass eine DLL verwendet werden kann, um mehr als ein Protokoll zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="15a54-108">However, a parser DLL can contain multiple parsers which means that one DLL can be used to detect more than one protocol.</span></span>

<span data-ttu-id="15a54-109">Die an einen Parser weiter gegebenen Daten werden aus einer [*verzögerten Erfassung*](d.md)entnommen und auf Frame-für-Frame-Basis an den Parser übergeben.</span><span class="sxs-lookup"><span data-stu-id="15a54-109">The data passed to a parser is taken from a [*delayed capture*](d.md), and passed to the parser on a frame-by-frame basis.</span></span> <span data-ttu-id="15a54-110">Sie können eine echt Zeiterfassung nicht analysieren.</span><span class="sxs-lookup"><span data-stu-id="15a54-110">You cannot parse a real-time capture.</span></span>

<span data-ttu-id="15a54-111">Um die Daten in einem Frame zu analysieren, muss der Parser die Protokoll Instanz erkennen, die Eigenschaften identifizieren, die in der Protokoll Instanz vorhanden sind, und jede Eigenschaft eine Eigenschafts Definition anfügen.</span><span class="sxs-lookup"><span data-stu-id="15a54-111">To parse the data in a frame, the parser must recognize the protocol instance, identify the properties that exist in the protocol instance, and attach a property definition to each property.</span></span> <span data-ttu-id="15a54-112">Beachten Sie, dass der Frame nur einen Datenstrom enthält.</span><span class="sxs-lookup"><span data-stu-id="15a54-112">Be aware that the frame contains only a stream of data.</span></span> <span data-ttu-id="15a54-113">Der Frame enthält keine Daten, die angeben, welche Protokolle oder Protokoll Eigenschaften die Daten darstellen.</span><span class="sxs-lookup"><span data-stu-id="15a54-113">The frame does not contain data that indicates which protocols or protocol properties the data represents.</span></span>

<span data-ttu-id="15a54-114">Die folgende Abbildung zeigt einen Frame, der eine Instanz eines Protokolls enthält.</span><span class="sxs-lookup"><span data-stu-id="15a54-114">The following illustration shows a frame that contains an instance of a protocol.</span></span>

![ein Frame, der eine Protokoll Instanz enthält.](images/parser1.png)

<span data-ttu-id="15a54-116">Wenn Netzwerkmonitor Analysierte Daten in der Benutzeroberfläche anzeigt, muss der Parser die Daten formatieren.</span><span class="sxs-lookup"><span data-stu-id="15a54-116">If Network Monitor is going to display parsed data in the UI, the parser must format the data.</span></span> <span data-ttu-id="15a54-117">Einige Experten verwenden die parserausgabe jedoch Programm gesteuert und zeigen die Ausgabe nicht in der Netzwerkmonitor-Benutzeroberfläche an.</span><span class="sxs-lookup"><span data-stu-id="15a54-117">However, some experts use the parser output programmatically, and do not display the output in the Network Monitor UI.</span></span> <span data-ttu-id="15a54-118">Die angezeigten Daten umfassen sowohl Parser-definierte Daten als auch die Daten in der Erfassung.</span><span class="sxs-lookup"><span data-stu-id="15a54-118">Displayed data includes both parser-defined data, and the data in the capture.</span></span> <span data-ttu-id="15a54-119">Der Parser stellt z. b. in der Regel einen Namen für eine angezeigte Eigenschaft und die Daten in der Erfassung bereit, die der-Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15a54-119">For example, the parser typically provides both a name for a property that is displayed, and the data in the capture that is associated with the property.</span></span>



| <span data-ttu-id="15a54-120">Informationen über</span><span class="sxs-lookup"><span data-stu-id="15a54-120">For information about</span></span>                                         | <span data-ttu-id="15a54-121">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="15a54-121">See</span></span>                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="15a54-122">Welche Einstiegspunkte in der Parser-DLL implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="15a54-122">Which entry points must be implemented within the parser DLL.</span></span> | [<span data-ttu-id="15a54-123">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="15a54-123">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                 |
| <span data-ttu-id="15a54-124">Gewusst wie: Implementieren von parserdll-Exportfunktionen</span><span class="sxs-lookup"><span data-stu-id="15a54-124">How to implement parser DLL export functions.</span></span>                 | [<span data-ttu-id="15a54-125">Schreiben eines Protokoll Parsers</span><span class="sxs-lookup"><span data-stu-id="15a54-125">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="15a54-126">Welche Funktionen und Struktur Parser verwenden.</span><span class="sxs-lookup"><span data-stu-id="15a54-126">Which functions and structures parsers use.</span></span>                   | [<span data-ttu-id="15a54-127">Parser-Funktionen und-Strukturen</span><span class="sxs-lookup"><span data-stu-id="15a54-127">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



