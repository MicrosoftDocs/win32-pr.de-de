---
title: Implementieren von Eingabepipes auf dem Client
description: Wenn Sie eine Eingabepipe verwenden, um Daten vom Client auf den Server zu übertragen, müssen Sie eine Pullprozedur implementieren.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0301fc7324a982db81b6c728131762361cfce185f3d432f238ca2cf8d715546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929119"
---
# <a name="implementing-input-pipes-on-the-client"></a>Implementieren von Eingabepipes auf dem Client

Wenn Sie eine Eingabepipe verwenden, um Daten vom Client auf den Server zu übertragen, müssen Sie eine Pullprozedur implementieren. Die Pullprozedur muss die zu übertragenden Daten finden, die Daten in den Puffer einlesen und die Anzahl der zu sendenden Elemente festlegen. Nicht alle Daten müssen sich im Puffer befinden, wenn der Server beginnt, Daten an sich selbst zu pullen. Die Pullprozedur kann den Puffer inkrementell füllen.

Wenn keine daten mehr gesendet werden müssen, legt die Prozedur ihr letztes Argument auf 0 (null) fest. Wenn alle Daten gesendet werden, sollte der Pullvorgang alle erforderlichen Bereinigungen durchführen, bevor zurückgegeben wird. Bei einem Parameter, der ein \[ In-Out-Pipe \] ist, muss die Pullprozedur die Zustandsvariable des Clients zurücksetzen, nachdem alle Daten übertragen wurden, damit die Pushprozedur sie zum Empfangen von Daten verwenden kann.

Das folgende Beispiel wird aus dem Pipedemo-Programm extrahiert, das im Platform Software Development Kit (SDK) enthalten ist.


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void SendLongs()
{
    LONG_PIPE inPipe;
    int i;
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
 
    for (i=0; i<PIPE_SIZE; i++)
        globalPipeData[i] = IN_VALUE;
 
    pipeDataIndex = 0;
    inPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    inPipe.pull  = PipePull;
    inPipe.alloc = PipeAlloc;
 
    InPipe( inPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );

}//end SendLongs
 
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
 
void PipePull( rpc_ss_pipe_state_t stateInfo,
               long *inputBuffer,
               ulong maxBufSize,
               ulong *sizeToSend )
{
    ulong currentIndex;
    ulong i;
    ulong elementsToRead;
    ulong *state = (ulong *)stateInfo;

    currentIndex = *state;
    if (*state >=  PIPE_SIZE )
    {
        *sizeToSend = 0; /* end of pipe data */
        *state = 0; /* Reset the state = global index */
    }
    else 
    {
        if ( currentIndex + maxBufSize > PIPE_SIZE )
            elementsToRead = PIPE_SIZE - currentIndex;
        else
            elementsToRead = maxBufSize;
 
        for (i=0; i < elementsToRead; i++)
        {
            /*client sends data */
            inputBuffer[i] = globalPipeData[i + currentIndex];
        }
 
        *state +=   elementsToRead;
        *sizeToSend = elementsToRead;
    } 
}//end PipePull
```



Dieses Beispiel enthält die vom MIDL-Compiler generierte Headerdatei. Weitere Informationen finden Sie unter [Definieren von Pipes in IDL-Dateien.](defining-pipes-in-idl-files.md) Außerdem wird eine Variable deklariert, die als Datenquelle namens globalPipeData verwendet wird. Die Variable globalBuffer ist ein Puffer, den die Pullprozedur verwendet, um die Datenblöcke zu senden, die sie aus globalPipeData abruft.

Die SendLongs-Funktion deklariert die Eingabepipe und belegt Speicher für die Datenquellenvariable globalPipeData. In Ihrem Client-/Serverprogramm kann die Datenquelle eine Datei oder Struktur sein, die der Client erstellt. Sie können das Clientprogramm auch dazu bringen, Daten vom Server abzurufen, zu verarbeiten und mithilfe einer Eingabepipe an den Server zurückzugeben. In diesem einfachen Beispiel ist die Datenquelle ein dynamisch zugeordneter Puffer langer ganzzahliger Zahlen.

Bevor die Übertragung beginnen kann, muss der Client Zeiger auf die Zustandsvariable, die Pullprozedur und die Alloc-Prozedur festlegen. Diese Zeiger werden in der vom Client deklarierten Pipevariablen beibehalten. In diesem Fall deklariert SendLongs inPipe. Sie können einen beliebigen geeigneten Datentyp für Ihre Zustandsvariable verwenden.

Clients initiieren Datenübertragungen über eine Pipe, indem sie eine Remoteprozedur auf dem Server aufrufen. Durch Aufrufen der Remoteprozedur wird dem Serverprogramm mitgeteilt, dass der Client für die Übertragung bereit ist. Der Server kann dann die Daten an sich selbst übertragen. In diesem Beispiel wird eine Remoteprozedur namens InPipe aufgerufen. Nachdem die Daten an den Server übertragen wurden, gibt die SendLongs-Funktion den dynamisch zugeordneten Puffer frei.

Anstatt jedes Mal Arbeitsspeicher zu belegen, wenn ein Puffer benötigt wird. Die Alloc-Prozedur in diesem Beispiel legt einfach einen Zeiger auf die Variable globalBuffer fest. Der Pullprozedur verwendet diesen Puffer bei jeder Übertragung von Daten wieder. Komplexere Clientprogramme müssen möglicherweise jedes Mal, wenn der Server Daten vom Client abruft, einen neuen Puffer zuordnen.

Der Clientstub ruft die Pullprozedur auf. Die Pullprozedur in diesem Beispiel verwendet die Zustandsvariable, um die nächste Position im globalen Datenquellenpuffer nachzuverfolgen, aus der gelesen werden soll. Sie liest Daten aus dem Quellpuffer in den Pipepuffer. Der Clientstub überträgt die Daten an den Server. Wenn alle Daten gesendet wurden, legt die Pullprozedur die Puffergröße auf 0 (null) fest. Dadurch wird der Server angewiesen, das Abrufen von Daten zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rohr](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 