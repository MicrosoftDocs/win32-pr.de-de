---
title: Implementieren von Eingabe Pipes auf dem Client
description: Wenn Sie eine Eingabe Pipe zum Übertragen von Daten vom Client auf den-Server verwenden, müssen Sie eine Pull-Prozedur implementieren.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810caa31c4932294797a5ed502c6f93d8613ea0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858382"
---
# <a name="implementing-input-pipes-on-the-client"></a>Implementieren von Eingabe Pipes auf dem Client

Wenn Sie eine Eingabe Pipe zum Übertragen von Daten vom Client auf den-Server verwenden, müssen Sie eine Pull-Prozedur implementieren. Die Pull-Prozedur muss die zu übertragenden Daten finden, die Daten in den Puffer einlesen und die Anzahl der zu sendenden Elemente festlegen. Nicht alle Daten müssen sich im Puffer befinden, wenn der Server mit dem Abrufen von Daten an sich selbst beginnt. Mit der Pull-Prozedur kann der Puffer inkrementell aufgefüllt werden.

Wenn keine weiteren Daten zum Senden vorhanden sind, legt die Prozedur das letzte Argument auf NULL fest. Wenn alle Daten gesendet werden, sollte die Pull-Prozedur vor der Rückgabe alle benötigten Bereinigungs Vorgänge ausführen. Bei einem Parameter, bei dem es sich um eine \[ in-, out- \] Pipe handelt, muss die Pull-Prozedur die Zustands Variable des Clients zurücksetzen, nachdem alle Daten übertragen wurden, sodass Sie von der Push-Prozedur zum Empfangen von Daten verwendet werden kann.

Das folgende Beispiel wird aus dem pipedemo-Programm extrahiert, das im Platform Software Development Kit (SDK) enthalten ist.


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



Dieses Beispiel enthält die Header Datei, die vom-Mittell-Compiler generiert wurde. Weitere Informationen finden Sie [unter Definieren von Pipes in IDL-Dateien](defining-pipes-in-idl-files.md). Außerdem wird eine Variable deklariert, die Sie als Datenquelle namens globalpipedata verwendet. Die Variable globalbuffer ist ein Puffer, den die Pull-Prozedur verwendet, um die Datenblöcke zu senden, die Sie von globalpipedata abruft.

Die sendlongs-Funktion deklariert die Eingabe Pipe und ordnet Speicher für die Datenquellen Variable globalpipedata zu. In Ihrem Client/Server-Programm kann es sich bei der Datenquelle um eine Datei oder Struktur handeln, die vom Client erstellt wird. Sie können das Client Programm auch zum Abrufen von Daten vom Server, zum Verarbeiten und zum Zurückgeben des Servers mithilfe einer Eingabe Pipe verwenden. In diesem einfachen Beispiel ist die Datenquelle ein dynamisch zugewiesener Puffer mit langen ganzen Zahlen.

Bevor die Übertragung beginnen kann, muss der Client Zeiger auf die Zustands Variable, die Pull-Prozedur und die zuordnungsprozedur festlegen. Diese Zeiger werden in der Pipe-Variablen aufbewahrt, die der Client deklariert. In diesem Fall deklariert sendlongs inpipe. Sie können einen beliebigen entsprechenden Datentyp für die Zustands Variable verwenden.

Clients initiieren Datenübertragungen über eine Pipe, indem Sie eine Remote Prozedur auf dem Server aufrufen. Durch den Aufruf der Remote Prozedur wird dem Serverprogramm mitgeteilt, dass der Client zur Übertragung bereit ist. Der Server kann die Daten dann in sich selbst abrufen. In diesem Beispiel wird eine Remote Prozedur mit dem Namen inpipe aufgerufen. Nachdem die Daten an den Server übertragen wurden, gibt die sendlongs-Funktion den dynamisch zugewiesenen Puffer frei.

Anstatt Arbeitsspeicher jedes Mal zuzuweisen, wenn ein Puffer benötigt wird. die "Zuweisung"-Prozedur in diesem Beispiel legt einfach einen Zeiger auf die Variable "globalbuffer" fest. Der Puffer wird von der Pull-Prozedur jedes Mal wieder verwendet, wenn Daten übertragen werden. Komplexere Client Programme müssen möglicherweise jedes Mal einen neuen Puffer zuordnen, wenn der Serverdaten vom Client abruft.

Der Clientstub Ruft die Pull-Prozedur auf. Die Pull-Prozedur in diesem Beispiel verwendet die State-Variable, um die nächste Position im globalen Datenquellen Puffer zu verfolgen, aus dem gelesen werden soll. Er liest Daten aus dem Quell Puffer in den Pipepuffer. Der Client-Stub überträgt die Daten an den Server. Wenn alle Daten gesendet wurden, wird die Puffergröße von der Pull-Prozedur auf 0 (null) festgelegt. Dies weist den Server an, das Abrufen von Daten zu verhindern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 