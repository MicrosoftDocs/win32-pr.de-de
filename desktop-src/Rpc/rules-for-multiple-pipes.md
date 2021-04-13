---
title: Regeln für mehrere Pipes
description: Regeln für mehrere Pipes in einem einzigen Aufruf in Remote Prozedur Aufruf (RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d804c132d7fc859906f065e4c9dc39dd3159519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473885"
---
# <a name="rules-for-multiple-pipes"></a><span data-ttu-id="d2965-103">Regeln für mehrere Pipes</span><span class="sxs-lookup"><span data-stu-id="d2965-103">Rules for Multiple Pipes</span></span>

<span data-ttu-id="d2965-104">Sie können in \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] einer beliebigen Kombination in einem einzelnen-Befehl eine Kombination aus in-, out-und in-und \[ **out** - \] Pipe-Parametern kombinieren, aber Sie müssen die Pipes in einer bestimmten Reihenfolge verarbeiten, wie im folgenden Pseudo Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d2965-104">You can combine \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], and \[**in, out**\] pipe parameters in any combination in a single call, but you must process the pipes in a specific order, as shown in the following pseudocode example:</span></span>

> [!Note]  
> <span data-ttu-id="d2965-105">Diese Funktion wird in Windows Vista und späteren Plattformen nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2965-105">This feature is no longer supported in Windows Vista and later platforms.</span></span>

 

-   <span data-ttu-id="d2965-106">Holen Sie die Daten aus jeder Eingabe Pipe, beginnend mit dem ersten (äußersten linken) \[ **in** \] -Parameter, und fahren Sie in der Reihenfolge fort, bevor Sie die Pipeline vor Beginn der nächsten Verarbeitung leeren.</span><span class="sxs-lookup"><span data-stu-id="d2965-106">Get the data from every input pipe, starting with the first (leftmost) \[**in**\] parameter, and continuing in order, draining each pipe before beginning to process the next.</span></span>
-   <span data-ttu-id="d2965-107">Nachdem jede Eingabe Pipe vollständig verarbeitet wurde, senden Sie die Daten für die ausgabepipes, beginnend mit dem ersten \[ **out** \] -Parameter, und setzen Sie in der Reihenfolge fort, dass Sie jede Pipe ausfüllen, bevor Sie mit der Verarbeitung der nächsten beginnen.</span><span class="sxs-lookup"><span data-stu-id="d2965-107">After every input pipe has been completely processed, send the data for the output pipes, again starting with the first \[**out**\] parameter, and continuing in order, filling each pipe before beginning to process the next.</span></span>

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 