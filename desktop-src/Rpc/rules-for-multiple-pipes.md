---
title: Regeln für mehrere Pipes
description: Regeln für mehrere Pipes in einem einzelnen Aufruf im Remoteprozeduraufruf (Remote Procedure Call, RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd2de7a44f63d5c943f1d6526ee328bbae3e63c99bac118ec843ad266d1f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925977"
---
# <a name="rules-for-multiple-pipes"></a>Regeln für mehrere Pipes

Sie können in den Parametern , out und out pipe in einer beliebigen Kombination in einem einzigen Aufruf kombinieren, aber Sie müssen die Pipes in einer bestimmten Reihenfolge verarbeiten, wie im folgenden \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] \[  \] Pseudocodebeispiel gezeigt:

> [!Note]  
> Dieses Feature wird nicht mehr auf den Plattformen Windows Vista und höher unterstützt.

 

-   Sie können die Daten aus jeder Eingabepipe erhalten, beginnend mit dem ersten (ganz links) im -Parameter und dem Fortfahren in der angegebenen Reihenfolge und dem Leeren der einzelnen Pipes, bevor Sie mit der Verarbeitung der \[  \] nächsten beginnen.
-   Nachdem jede Eingabepipe vollständig verarbeitet wurde, senden Sie die Daten für die Ausgabepipes. Beginnen Sie erneut mit dem ersten \[ **out-Parameter,** und setzen Sie die Reihenfolge fort, und füllen Sie jede Pipe aus, bevor Sie mit der Verarbeitung des nächsten \] beginnen.

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

 

 