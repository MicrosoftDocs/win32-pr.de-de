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
# <a name="implementing-input-pipes-on-the-client"></a><span data-ttu-id="38e55-103">Implementieren von Eingabe Pipes auf dem Client</span><span class="sxs-lookup"><span data-stu-id="38e55-103">Implementing Input Pipes on the Client</span></span>

<span data-ttu-id="38e55-104">Wenn Sie eine Eingabe Pipe zum Übertragen von Daten vom Client auf den-Server verwenden, müssen Sie eine Pull-Prozedur implementieren.</span><span class="sxs-lookup"><span data-stu-id="38e55-104">When using an input pipe to transfer data from the client to the server, you must implement a pull procedure.</span></span> <span data-ttu-id="38e55-105">Die Pull-Prozedur muss die zu übertragenden Daten finden, die Daten in den Puffer einlesen und die Anzahl der zu sendenden Elemente festlegen.</span><span class="sxs-lookup"><span data-stu-id="38e55-105">The pull procedure must find the data to be transferred, read the data into the buffer, and set the number of elements to send.</span></span> <span data-ttu-id="38e55-106">Nicht alle Daten müssen sich im Puffer befinden, wenn der Server mit dem Abrufen von Daten an sich selbst beginnt.</span><span class="sxs-lookup"><span data-stu-id="38e55-106">Not all of the data has to be in the buffer when the server begins to pull data to itself.</span></span> <span data-ttu-id="38e55-107">Mit der Pull-Prozedur kann der Puffer inkrementell aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="38e55-107">The pull procedure can fill the buffer incrementally.</span></span>

<span data-ttu-id="38e55-108">Wenn keine weiteren Daten zum Senden vorhanden sind, legt die Prozedur das letzte Argument auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="38e55-108">When there is no more data to send, the procedure sets its last argument to zero.</span></span> <span data-ttu-id="38e55-109">Wenn alle Daten gesendet werden, sollte die Pull-Prozedur vor der Rückgabe alle benötigten Bereinigungs Vorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="38e55-109">When all the data is sent, the pull procedure should do any needed cleanup before returning.</span></span> <span data-ttu-id="38e55-110">Bei einem Parameter, bei dem es sich um eine \[ in-, out- \] Pipe handelt, muss die Pull-Prozedur die Zustands Variable des Clients zurücksetzen, nachdem alle Daten übertragen wurden, sodass Sie von der Push-Prozedur zum Empfangen von Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="38e55-110">For a parameter that is an \[in, out\] pipe, the pull procedure must reset the client's state variable after all the data has been transmitted, so that the push procedure can use it to receive data.</span></span>

<span data-ttu-id="38e55-111">Das folgende Beispiel wird aus dem pipedemo-Programm extrahiert, das im Platform Software Development Kit (SDK) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="38e55-111">The following example is extracted from the Pipedemo program included with the Platform Software Development Kit (SDK).</span></span>


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



<span data-ttu-id="38e55-112">Dieses Beispiel enthält die Header Datei, die vom-Mittell-Compiler generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="38e55-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="38e55-113">Weitere Informationen finden Sie [unter Definieren von Pipes in IDL-Dateien](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="38e55-113">For details see [Defining Pipes in IDL Files](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="38e55-114">Außerdem wird eine Variable deklariert, die Sie als Datenquelle namens globalpipedata verwendet.</span><span class="sxs-lookup"><span data-stu-id="38e55-114">It also declares a variable it uses as the data source called globalPipeData.</span></span> <span data-ttu-id="38e55-115">Die Variable globalbuffer ist ein Puffer, den die Pull-Prozedur verwendet, um die Datenblöcke zu senden, die Sie von globalpipedata abruft.</span><span class="sxs-lookup"><span data-stu-id="38e55-115">The variable globalBuffer is a buffer that the pull procedure uses to send the blocks of data it obtains from globalPipeData.</span></span>

<span data-ttu-id="38e55-116">Die sendlongs-Funktion deklariert die Eingabe Pipe und ordnet Speicher für die Datenquellen Variable globalpipedata zu.</span><span class="sxs-lookup"><span data-stu-id="38e55-116">The SendLongs function declares the input pipe, and allocates memory for the data source variable globalPipeData.</span></span> <span data-ttu-id="38e55-117">In Ihrem Client/Server-Programm kann es sich bei der Datenquelle um eine Datei oder Struktur handeln, die vom Client erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="38e55-117">In your client/server program, the data source can be a file or structure that the client creates.</span></span> <span data-ttu-id="38e55-118">Sie können das Client Programm auch zum Abrufen von Daten vom Server, zum Verarbeiten und zum Zurückgeben des Servers mithilfe einer Eingabe Pipe verwenden.</span><span class="sxs-lookup"><span data-stu-id="38e55-118">You can also have your client program obtain data from the server, process it, and return it to the server using an input pipe.</span></span> <span data-ttu-id="38e55-119">In diesem einfachen Beispiel ist die Datenquelle ein dynamisch zugewiesener Puffer mit langen ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="38e55-119">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="38e55-120">Bevor die Übertragung beginnen kann, muss der Client Zeiger auf die Zustands Variable, die Pull-Prozedur und die zuordnungsprozedur festlegen.</span><span class="sxs-lookup"><span data-stu-id="38e55-120">Before the transfer can begin, the client must set pointers to the state variable, the pull procedure, and the alloc procedure.</span></span> <span data-ttu-id="38e55-121">Diese Zeiger werden in der Pipe-Variablen aufbewahrt, die der Client deklariert.</span><span class="sxs-lookup"><span data-stu-id="38e55-121">These pointers are kept in the pipe variable the client declares.</span></span> <span data-ttu-id="38e55-122">In diesem Fall deklariert sendlongs inpipe.</span><span class="sxs-lookup"><span data-stu-id="38e55-122">In this case, SendLongs declares inPipe.</span></span> <span data-ttu-id="38e55-123">Sie können einen beliebigen entsprechenden Datentyp für die Zustands Variable verwenden.</span><span class="sxs-lookup"><span data-stu-id="38e55-123">You can use any appropriate data type for your state variable.</span></span>

<span data-ttu-id="38e55-124">Clients initiieren Datenübertragungen über eine Pipe, indem Sie eine Remote Prozedur auf dem Server aufrufen.</span><span class="sxs-lookup"><span data-stu-id="38e55-124">Clients initiate data transfers across a pipe by invoking a remote procedure on the server.</span></span> <span data-ttu-id="38e55-125">Durch den Aufruf der Remote Prozedur wird dem Serverprogramm mitgeteilt, dass der Client zur Übertragung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="38e55-125">Calling the remote procedure tells the server program that the client is ready to transmit.</span></span> <span data-ttu-id="38e55-126">Der Server kann die Daten dann in sich selbst abrufen.</span><span class="sxs-lookup"><span data-stu-id="38e55-126">The server can then pull the data to itself.</span></span> <span data-ttu-id="38e55-127">In diesem Beispiel wird eine Remote Prozedur mit dem Namen inpipe aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="38e55-127">This example invokes a remote procedure called InPipe.</span></span> <span data-ttu-id="38e55-128">Nachdem die Daten an den Server übertragen wurden, gibt die sendlongs-Funktion den dynamisch zugewiesenen Puffer frei.</span><span class="sxs-lookup"><span data-stu-id="38e55-128">After the data is transferred to the server, the SendLongs function frees the dynamically allocated buffer.</span></span>

<span data-ttu-id="38e55-129">Anstatt Arbeitsspeicher jedes Mal zuzuweisen, wenn ein Puffer benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="38e55-129">Rather than allocate memory each time a buffer is needed.</span></span> <span data-ttu-id="38e55-130">die "Zuweisung"-Prozedur in diesem Beispiel legt einfach einen Zeiger auf die Variable "globalbuffer" fest.</span><span class="sxs-lookup"><span data-stu-id="38e55-130">the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="38e55-131">Der Puffer wird von der Pull-Prozedur jedes Mal wieder verwendet, wenn Daten übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="38e55-131">The pull procedure reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="38e55-132">Komplexere Client Programme müssen möglicherweise jedes Mal einen neuen Puffer zuordnen, wenn der Serverdaten vom Client abruft.</span><span class="sxs-lookup"><span data-stu-id="38e55-132">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="38e55-133">Der Clientstub Ruft die Pull-Prozedur auf.</span><span class="sxs-lookup"><span data-stu-id="38e55-133">The client stub calls the pull procedure.</span></span> <span data-ttu-id="38e55-134">Die Pull-Prozedur in diesem Beispiel verwendet die State-Variable, um die nächste Position im globalen Datenquellen Puffer zu verfolgen, aus dem gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="38e55-134">The pull procedure in this example uses the state variable to track the next position in the global data source buffer to read from.</span></span> <span data-ttu-id="38e55-135">Er liest Daten aus dem Quell Puffer in den Pipepuffer.</span><span class="sxs-lookup"><span data-stu-id="38e55-135">It reads data from the source buffer into the pipe buffer.</span></span> <span data-ttu-id="38e55-136">Der Client-Stub überträgt die Daten an den Server.</span><span class="sxs-lookup"><span data-stu-id="38e55-136">The client stub transmits the data to the server.</span></span> <span data-ttu-id="38e55-137">Wenn alle Daten gesendet wurden, wird die Puffergröße von der Pull-Prozedur auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="38e55-137">When all the data has been sent, the pull procedure sets the buffer size to zero.</span></span> <span data-ttu-id="38e55-138">Dies weist den Server an, das Abrufen von Daten zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="38e55-138">This tells the server to stop pulling data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38e55-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38e55-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38e55-140">Kanal</span><span class="sxs-lookup"><span data-stu-id="38e55-140">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="38e55-141">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="38e55-141">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 