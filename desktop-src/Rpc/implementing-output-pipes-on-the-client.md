---
title: Implementieren von Ausgabepipes auf dem Client
description: Wenn Sie eine Ausgabepipe verwenden, um Daten vom Server an den Client zu übertragen, müssen Sie eine Pushprozedur in Ihrem Client implementieren.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e959db9e505bb7dfe570552fe0385251485591fecb1f818ab4d5de402c2297b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929129"
---
# <a name="implementing-output-pipes-on-the-client"></a>Implementieren von Ausgabepipes auf dem Client

Wenn Sie eine Ausgabepipe verwenden, um Daten vom Server an den Client zu übertragen, müssen Sie eine Pushprozedur in Ihrem Client implementieren. Die Pushprozedur verwendet einen Zeiger auf einen Puffer und eine Elementanzahl aus dem Clientstub und verarbeitet die Daten, wenn die Elementanzahl größer als 0 ist. Beispielsweise könnten die Daten aus dem Puffer des Stubs in den eigenen Arbeitsspeicher kopiert werden. Alternativ kann er die Daten im Puffer des Stubs verarbeiten und in einer Datei speichern. Wenn die Elementanzahl gleich 0 (null) ist, schließt die Pushprozedur alle erforderlichen Bereinigungsaufgaben vor der Rückgabe ab.

Im folgenden Beispiel ordnet die Clientfunktion ReceiveLongs eine Pipestruktur und einen globalen Speicherpuffer zu. Sie initialisiert die -Struktur, macht den Remoteprozeduraufruf und gibt dann den Arbeitsspeicher frei.

## <a name="example"></a>Beispiel


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *  globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void ReceiveLongs()
{
    LONG_PIPE *outputPipe;
    idl_long_int i;
 
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    pipeDataIndex = 0;
    outputPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    outputPipe.push  = PipePush;
    outputPipe.alloc = PipeAlloc;
 
    OutPipe( &outputPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );
 
}//end ReceiveLongs()

void PipeAlloc( rpc_ss_pipe_state_t stateInfo,
                ulong requestedSize,
                long **allocatedBuffer,
                ulong *allocatedSize )
{ 
    ulong *state = (ulong *)stateInfo;
    if ( requestedSize > (BUF_SIZE*sizeof(long)) )
    {
       *allocatedSize = BUF_SIZE * sizeof(long);
    }
    else
    {
       *allocatedSize = requestedSize;
    }
    *allocatedBuffer = globalBuffer; 
} //end PipeAlloc
 
void PipePush( rpc_ss_pipe_state_t stateInfo,
               long *buffer,
               ulong numberOfElements )
{
    ulong elementsToCopy, i;
    ulong *state = (ulong *)stateInfo;

    if (numberOfElements == 0)/* end of data */
    {
        *state = 0; /* Reset the state = global index */
    }
    else
    {
        if (*state + numberOfElements > PIPE_SIZE)
            elementsToCopy = PIPE_SIZE - *state;
        else
            elementsToCopy = numberOfElements;
 
        for (i=0; i <elementsToCopy; i++)
        { 
            /*client receives data */
            globalPipeData[*state] = buffer[i];
            (*state)++;
        }
    }
}//end PipePush
```



Dieses Beispiel enthält die vom MIDL-Compiler generierte Headerdatei. Weitere Informationen finden Sie [unter Definieren von Pipes in der IDL-Datei](defining-pipes-in-idl-files.md). Außerdem wird die Variable globalPipeData deklariert, die als Datensenke verwendet wird. Die Variable globalBuffer ist ein Puffer, der von der Pushprozedur zum Empfangen von Datenblöcken verwendet wird, die in globalPipeData gespeichert werden.

Die ReceiveLongs-Funktion deklariert eine Pipe und weist Speicherplatz für die globale Datensenkenvariable zu. In Ihrem Client-/Serverprogramm kann die Datensenke eine Datei oder Datenstruktur sein, die der Client erstellt. In diesem einfachen Beispiel ist die Datenquelle ein dynamisch zugeordneter Puffer mit langen ganzen Zahlen.

Bevor die Datenübertragung beginnen kann, muss ihr Clientprogramm die Ausgabepipestruktur initialisieren. Sie muss Zeiger auf die Zustandsvariable, die Pushprozedur und die Alloc-Prozedur festlegen. In diesem Beispiel wird die Ausgabepipevariable als outputPipe bezeichnet.

Clients signalisieren Servern, dass sie zum Empfangen von Daten bereit sind, indem sie eine Remoteprozedur auf dem Server aufrufen. In diesem Beispiel heißt die Remoteprozedur OutPipe. Wenn der Client die Remoteprozedur aufruft, beginnt der Server mit der Datenübertragung. Jedes Mal, wenn Daten eintreffen, ruft der Clientstub die Prozeduren "alloc" und "push" des Clients nach Bedarf auf.

Anstatt jedes Mal, wenn ein Puffer benötigt wird, Speicher zu reservieren, legt die Zuordnungsprozedur in diesem Beispiel einfach einen Zeiger auf die Variable globalBuffer fest. Der Pullprozedur verwendet diesen Puffer dann bei jeder Übertragung von Daten erneut. Komplexere Clientprogramme müssen möglicherweise jedes Mal, wenn der Server Daten vom Client pullt, einen neuen Puffer zuordnen.

Die Pushprozedur in diesem Beispiel verwendet die Zustandsvariable, um die nächste Position zu verfolgen, an der Daten im globalen Datensenkenpuffer gespeichert werden. Es schreibt Daten aus dem Pipepuffer in den Senkenpuffer. Der Clientstub empfängt dann den nächsten Datenblock vom Server und speichert ihn im Pipepuffer. Wenn alle Daten gesendet wurden, überträgt der Server einen Puffer der Größe 0 (null). Dadurch wird die Pushprozedur zum Beenden des Daten empfangenden Vorgangs angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rohr](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 