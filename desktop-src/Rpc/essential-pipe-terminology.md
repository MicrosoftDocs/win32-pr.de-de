---
title: Wichtige Pipe-Terminologie
description: Wie bei anderen Typen von Parametern für Remote Prozedur Aufrufe können Pipes in den Parametern \ oder \ out \ Parameter lauten.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517018"
---
# <a name="essential-pipe-terminology"></a><span data-ttu-id="ede43-103">Wichtige Pipe-Terminologie</span><span class="sxs-lookup"><span data-stu-id="ede43-103">Essential Pipe Terminology</span></span>

<span data-ttu-id="ede43-104">Wie bei anderen Typen von Parametern für Remote Prozedur Aufrufe können Pipes \[ [**in**](/windows/desktop/Midl/in) - \] oder \[ [**out**](/windows/desktop/Midl/out-idl) - \] Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="ede43-104">Like other types of parameters to remote procedure calls, pipes can be \[ [**in**](/windows/desktop/Midl/in)\] or \[ [**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="ede43-105">Da der Server die Übertragung von Daten über eine Pipe steuert, werden Pipes mit dem \[ **in** - \] Attribut zum *Abrufen* von Daten an den Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="ede43-105">Since the server controls the transfer of data through a pipe, pipes with the \[**in**\] attribute are said to *pull* data to the server.</span></span> <span data-ttu-id="ede43-106">Auf ähnliche Weise überträgt *Output Pipes Daten* vom Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="ede43-106">Similarly, output pipes *push* data from the server to the client.</span></span> <span data-ttu-id="ede43-107">Die Prozeduren, die die Datenübertragung ausführen, werden als *Pull-Prozedur* bzw. als *pushprozedur* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ede43-107">The procedures that do the data transfer are called the *pull procedure* and the *push procedure*, respectively.</span></span>

<span data-ttu-id="ede43-108">Der mittlerer l-Compiler generiert die Push-und Pull-Prozeduren für den Server.</span><span class="sxs-lookup"><span data-stu-id="ede43-108">The MIDL compiler generates the push and pull procedures for the server.</span></span> <span data-ttu-id="ede43-109">Außerdem wird die Zuordnung von Daten Puffern im Arbeitsspeicher verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ede43-109">In addition, it manages the allocation of data buffers in memory.</span></span> <span data-ttu-id="ede43-110">Der Client muss jedoch eigene Push-und Pull-Prozeduren bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ede43-110">However, the client must provide its own push and pull procedures.</span></span> <span data-ttu-id="ede43-111">Außerdem muss Sie eine Prozedur zum Zuordnen der von der Pipe verwendeten Speicherpuffer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ede43-111">It must also provide a procedure for allocating the memory buffers used by the pipe.</span></span> <span data-ttu-id="ede43-112">Diese werden automatisch vom Clientstub zum richtigen Zeitpunkt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ede43-112">These are automatically called at the appropriate time by the client stub.</span></span> <span data-ttu-id="ede43-113">Die Zuordnungs Prozedur wird häufig als Zuordnungseinheits-Prozedur oder Zuordnungseinheits-Funktion bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ede43-113">The allocation procedure is often called the alloc procedure or the alloc function.</span></span>

 

 