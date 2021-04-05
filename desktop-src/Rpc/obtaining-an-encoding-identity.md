---
title: Abrufen einer Codierungs Identität
description: Eine Anwendung, die codierte Daten decodiert, kann die Identität der Routine abrufen, die zum Codieren der Daten verwendet wird, bevor eine Routine zum Decodieren aufgerufen wird. Diese Identität wird von der mesinqprocencodingid-Routine bereitstellt.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Abrufen der Codierungs Identität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713073"
---
# <a name="obtaining-an-encoding-identity"></a><span data-ttu-id="320ff-105">Abrufen einer Codierungs Identität</span><span class="sxs-lookup"><span data-stu-id="320ff-105">Obtaining an Encoding Identity</span></span>

<span data-ttu-id="320ff-106">Eine Anwendung, die codierte Daten decodiert, kann die Identität der Routine abrufen, die zum Codieren der Daten verwendet wird, bevor eine Routine zum Decodieren aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="320ff-106">An application that is decoding encoded data can obtain the identity of the routine used to encode the data, prior to calling a routine to decode it.</span></span> <span data-ttu-id="320ff-107">Diese Identität wird von der [**mesinqprocencodingid**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) -Routine bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="320ff-107">The [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) routine provides this identity.</span></span>

<span data-ttu-id="320ff-108">Jeder Prozedur in einer Schnittstelle wird vom Mittelwert Compiler eine ganzzahlige Identifikationsnummer, die als *Prozedur Bezeichner* oder eine *proc ID* bezeichnet wird, zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="320ff-108">Each procedure in an interface is assigned an integer identification number, called a *procedure identifier* or a *proc ID*, by the MIDL compiler.</span></span> <span data-ttu-id="320ff-109">Die Nummerierung beginnt mit 0.</span><span class="sxs-lookup"><span data-stu-id="320ff-109">Numbering begins with zero.</span></span> <span data-ttu-id="320ff-110">Die RPC-Laufzeitbibliotheken sind nicht an der Übersetzung der Prozedur-ID in einen tatsächlichen Prozedur Aufruf beteiligt.</span><span class="sxs-lookup"><span data-stu-id="320ff-110">The RPC run-time libraries are not involved in translating the procedure ID into an actual procedure call.</span></span> <span data-ttu-id="320ff-111">Wenn eine proc ID angegeben ist, muss Ihre Anwendung eine Möglichkeit zum Aufrufen der richtigen Prozedur bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="320ff-111">Given a proc ID, your application must provide a means of calling the correct procedure.</span></span> <span data-ttu-id="320ff-112">In der Regel verwenden Anwendungsentwickler eine Reihe von **if** -Anweisungen oder (bei Verwendung von C/C++) eine **Switch** -Anweisung zu diesem Zweck.</span><span class="sxs-lookup"><span data-stu-id="320ff-112">Typically, application developers use a series of **if** statements, or (when using C/C++) a **switch** statement for this purpose.</span></span>

 

 




