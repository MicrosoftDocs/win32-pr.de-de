---
title: Implementieren von Eingabepipes auf dem Server
description: Um mit dem Senden von Daten an einen Server zu beginnen, ruft ein Client eine der Remoteverfahren des Servers auf.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf133fce019328b9fa7d6b2a03e47d516de5ca74310d611ecea1686c0b9a3a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020520"
---
# <a name="implementing-input-pipes-on-the-server"></a>Implementieren von Eingabepipes auf dem Server

Um mit dem Senden von Daten an einen Server zu beginnen, ruft ein Client eine der Remoteverfahren des Servers auf. Diese Prozedur muss die Pullprozedur wiederholt im Stub des Servers aufrufen. Der MIDL-Compiler verwendet die IDL-Datei der Anwendung, um die Pullprozedur des Servers automatisch zu generieren.

Jedes Mal, wenn das Serverprogramm die Pullprozedur in seinem Stub aufruft, empfängt die Pullprozedur Datenblöcke vom Client. Die Daten werden in den Puffer des Servers entmarshalt. Die Remoteprozedur des Servers kann diese Daten dann auf jede erforderliche Weise verarbeiten. Die Schleife wird fortgesetzt, bis der Server einen Puffer der Länge 0 empfängt.

Das folgende Beispiel stammen aus dem Pipedemo-Programm, das in den Beispielen enthalten ist, die im Platform Software Development Kit (SDK) enthalten sind. Es veranschaulicht eine Remoteserverprozedur, die eine Pipe verwendet, um Daten vom Client an den Server zu pullen.

``` syntax
//file: server.c (fragment)
#include uc_server.c
#define PIPE_TRANSFER_SIZE 100 /* Transfer 100 pipe elements at one time */
 
void InPipe(LONG_PIPE     long_pipe )
{
    long local_pipe_buf[PIPE_TRANSFER_SIZE];
    ulong actual_transfer_count = PIPE_TRANSFER_SIZE;
 
    while(actual_transfer_count > 0) /* Loop to get all 
                                        the pipe data elements */
    {
        long_pipe.pull( long_pipe.state,
                        local_pipe_buf,
                        PIPE_TRANSFER_SIZE,
                        &actual_transfer_count);
        /* process the elements */
    } // end while
} //end InPipe
```

 

 




