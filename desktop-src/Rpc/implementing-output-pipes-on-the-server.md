---
title: Implementieren von ausgabepipes auf dem Server
description: Um mit dem Empfang von Daten von einem Server zu beginnen, Ruft ein Client eine der Remote Prozeduren des Servers auf.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3eb1362736207f9cc79d82ab6c981431d0bfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039492"
---
# <a name="implementing-output-pipes-on-the-server"></a>Implementieren von ausgabepipes auf dem Server

Um mit dem Empfang von Daten von einem Server zu beginnen, Ruft ein Client eine der Remote Prozeduren des Servers auf. Diese Prozedur muss das Push-Verfahren wiederholt im Stub des Servers aufzurufen. Der mittlerer l-Compiler verwendet die IDL-Datei der Anwendung, um die Push-Prozedur des Servers automatisch zu generieren.

Die Remote Server Routine muss den Puffer der ausgabepipe mit Daten füllen, bevor die pushprozedur aufgerufen wird. Jedes Mal, wenn das Serverprogramm das Push-Verfahren im Stub aufruft, werden die Daten von der Push-Prozedur an den Client übertragen und an den Client übermittelt. Die Schleife wird fortgesetzt, bis der Server einen Puffer der Länge 0 (null) sendet.

Das folgende Beispiel stammt aus dem pipedemo-Programm, das in den Beispielen für die Windows SDK enthalten ist. Es wird eine Remote Server Prozedur veranschaulicht, die eine Pipe verwendet, um Daten vom Server an den Client zu übersetzen.


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

[Kanal](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 