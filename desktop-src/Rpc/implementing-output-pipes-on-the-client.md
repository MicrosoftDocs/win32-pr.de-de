---
title: Implementieren von Ausgabe Pipes auf dem Client
description: Wenn Sie zum Übertragen von Daten vom Server an den Client eine ausgabepipe verwenden, müssen Sie eine pushprozedur in Ihrem Client implementieren.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff274491e2b665d86b550853d07c3ff6a4b2a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727792"
---
# <a name="implementing-output-pipes-on-the-client"></a>Implementieren von Ausgabe Pipes auf dem Client

Wenn Sie zum Übertragen von Daten vom Server an den Client eine ausgabepipe verwenden, müssen Sie eine pushprozedur in Ihrem Client implementieren. Die Push-Prozedur nimmt einen Zeiger auf einen Puffer und eine Element Anzahl aus dem Stub des Clients auf. wenn die Element Anzahl größer als 0 ist, werden die Daten von verarbeitet. Beispielsweise können die Daten aus dem Puffer des Stubs in ihren eigenen Arbeitsspeicher kopiert werden. Alternativ können die Daten im Puffer des Stubs verarbeitet und in einer Datei gespeichert werden. Wenn die Element Anzahl gleich 0 (null) ist, werden alle erforderlichen Cleanuptasks von der Push-Prozedur vor der Rückgabe abgeschlossen.

Im folgenden Beispiel ordnet die Client Funktion receivelongs eine Pipe-Struktur und einen globalen Speicherpuffer zu. Sie initialisiert die-Struktur, führt den Remote Prozedur Rückruf durch und gibt dann den Arbeitsspeicher frei.

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



Dieses Beispiel enthält die Header Datei, die vom-Mittell-Compiler generiert wurde. Weitere Informationen finden Sie [unter Definieren von Pipes in der IDL-Datei](defining-pipes-in-idl-files.md). Außerdem wird eine Variable, globalpipedata, deklariert, die als Daten Senke verwendet wird. Die Variable globalbuffer ist ein Puffer, den die pushprozedur zum Empfangen von Datenblöcken verwendet, die in globalpipedata gespeichert werden.

Die receivelongs-Funktion deklariert eine Pipe und ordnet Speicherplatz für die Variable der globalen Daten Senke zu. In Ihrem Client/Server-Programm kann die Daten Senke eine vom Client erstellte Datei-oder Datenstruktur sein. In diesem einfachen Beispiel ist die Datenquelle ein dynamisch zugewiesener Puffer mit langen ganzen Zahlen.

Bevor die Datenübertragung beginnen kann, muss das Client Programm die ausgabepipestruktur initialisieren. Sie muss Zeiger auf die Zustands Variable, die pushprozedur und die zuordnungsprozedur festlegen. In diesem Beispiel heißt die ausgabepipe-Variable outputpipe.

Clients signalisieren Servern, dass Sie bereit sind, Daten zu empfangen, indem Sie eine Remote Prozedur auf dem Server aufrufen. In diesem Beispiel wird die Remote Prozedur als outpipe bezeichnet. Wenn der Client die Remote Prozedur aufruft, beginnt der Server mit der Datenübertragung. Jedes Mal, wenn Daten eintreffen, ruft der Clientstub die Zustellungs-und pushprozeduren des Clients nach Bedarf auf.

Anstatt Arbeitsspeicher jedes Mal zuzuweisen, wenn ein Puffer benötigt wird, legt die Zuordnungs Prozedur in diesem Beispiel einfach einen Zeiger auf die Variable globalbuffer fest. Der Pull-Vorgang wird dann bei jedem Datentransfer erneut verwendet. Komplexere Client Programme müssen möglicherweise jedes Mal einen neuen Puffer zuordnen, wenn der Serverdaten vom Client abruft.

Das Push-Verfahren in diesem Beispiel verwendet die State-Variable, um die nächste Position zu verfolgen, an der die Daten im globalen Daten Senke-Puffer gespeichert werden. Er schreibt Daten aus dem Pipe-Puffer in den Senke Puffer. Der Client-Stub empfängt dann den nächsten Datenblock vom Server und speichert ihn im Pipepuffer. Wenn alle Daten gesendet wurden, überträgt der Server einen Puffer der Größe 0 (null). Dies gibt die pushprozedur an, um den Empfang von Daten zu verhindern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 