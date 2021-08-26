---
title: Implementieren von Ausgabepipes auf dem Server
description: Um mit dem Empfangen von Daten von einem Server zu beginnen, ruft ein Client eine der Remoteprozeduren des Servers auf.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d93b2933499ca86ab49732d46cf2abe3c37247ed7bfa5e653e5aa0119b1e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020490"
---
# <a name="implementing-output-pipes-on-the-server"></a>Implementieren von Ausgabepipes auf dem Server

Um mit dem Empfangen von Daten von einem Server zu beginnen, ruft ein Client eine der Remoteprozeduren des Servers auf. Diese Prozedur muss die Pushprozedur wiederholt im Stub des Servers aufrufen. Der MIDL-Compiler verwendet die IDL-Datei der Anwendung, um die Pushprozedur des Servers automatisch zu generieren.

Die Remoteserverroutine muss den Puffer der Ausgabepipe mit Daten füllen, bevor sie die Pushprozedur aufruft. Jedes Mal, wenn das Serverprogramm die Pushprozedur in seinem Stub aufruft, marshallt die Pushprozedur die Daten und überträgt sie an den Client. Die Schleife wird fortgesetzt, bis der Server einen Puffer der Länge 0 (null) sendet.

Das folgende Beispiel stammt aus dem Pipedemo-Programm, das in den Beispielen enthalten ist, die im Windows SDK enthalten sind. Es veranschaulicht eine Remoteserverprozedur, die eine Pipe verwendet, um Daten vom Server an den Client zu pushen.


```C++
void OutPipe(LONG_PIPE *outputPipe )
{
    long *outputPipeData;
    ulong index = 0;
    ulong elementsToSend = PIPE_TRANSFER_SIZE;
 
    /* Allocate memory for the data to be passed back in the pipe */
    outputPipeData = (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    while(elementsToSend >0) /* Loop to send pipe data elements */
    {
        if (index >= PIPE_SIZE)
            elementsToSend = 0;
        else
        {
            if ( (index + PIPE_TRANSFER_SIZE) > PIPE_SIZE )
                elementsToSend = PIPE_SIZE - index;
            else
                elementsToSend = PIPE_TRANSFER_SIZE;
        }
                    
        outputPipe->push( outputPipe->state,
                          &(outputPipeData[index]),
                          elementsToSend ); 
        index += elementsToSend;
 
    } //end while
 
    free((void *)outputPipeData);
 
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rohr](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 