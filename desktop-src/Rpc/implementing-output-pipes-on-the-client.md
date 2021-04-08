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
# <a name="implementing-output-pipes-on-the-client"></a><span data-ttu-id="745ff-103">Implementieren von Ausgabe Pipes auf dem Client</span><span class="sxs-lookup"><span data-stu-id="745ff-103">Implementing Output Pipes on the Client</span></span>

<span data-ttu-id="745ff-104">Wenn Sie zum Übertragen von Daten vom Server an den Client eine ausgabepipe verwenden, müssen Sie eine pushprozedur in Ihrem Client implementieren.</span><span class="sxs-lookup"><span data-stu-id="745ff-104">When using an output pipe to transfer data from the server to the client, you must implement a push procedure in your client.</span></span> <span data-ttu-id="745ff-105">Die Push-Prozedur nimmt einen Zeiger auf einen Puffer und eine Element Anzahl aus dem Stub des Clients auf. wenn die Element Anzahl größer als 0 ist, werden die Daten von verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="745ff-105">The push procedure takes a pointer to a buffer and an element count from the client stub and, if the element count is greater than 0, processes the data.</span></span> <span data-ttu-id="745ff-106">Beispielsweise können die Daten aus dem Puffer des Stubs in ihren eigenen Arbeitsspeicher kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="745ff-106">For example, it could copy the data from the stub's buffer to its own memory.</span></span> <span data-ttu-id="745ff-107">Alternativ können die Daten im Puffer des Stubs verarbeitet und in einer Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="745ff-107">Alternately, it could process the data in the stub's buffer and save it to a file.</span></span> <span data-ttu-id="745ff-108">Wenn die Element Anzahl gleich 0 (null) ist, werden alle erforderlichen Cleanuptasks von der Push-Prozedur vor der Rückgabe abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="745ff-108">When the element count equals zero, the push procedure completes any needed cleanup tasks before returning.</span></span>

<span data-ttu-id="745ff-109">Im folgenden Beispiel ordnet die Client Funktion receivelongs eine Pipe-Struktur und einen globalen Speicherpuffer zu.</span><span class="sxs-lookup"><span data-stu-id="745ff-109">In the following example, the client function ReceiveLongs allocates a pipe structure and a global memory buffer.</span></span> <span data-ttu-id="745ff-110">Sie initialisiert die-Struktur, führt den Remote Prozedur Rückruf durch und gibt dann den Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="745ff-110">It initializes the structure, makes the remote procedure call, and then frees the memory.</span></span>

## <a name="example"></a><span data-ttu-id="745ff-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="745ff-111">Example</span></span>


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



<span data-ttu-id="745ff-112">Dieses Beispiel enthält die Header Datei, die vom-Mittell-Compiler generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="745ff-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="745ff-113">Weitere Informationen finden Sie [unter Definieren von Pipes in der IDL-Datei](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="745ff-113">For details see [Defining Pipes in IDL File](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="745ff-114">Außerdem wird eine Variable, globalpipedata, deklariert, die als Daten Senke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="745ff-114">It also declares a variable, globalPipeData, that it uses as the data sink.</span></span> <span data-ttu-id="745ff-115">Die Variable globalbuffer ist ein Puffer, den die pushprozedur zum Empfangen von Datenblöcken verwendet, die in globalpipedata gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="745ff-115">The variable globalBuffer is a buffer that the push procedure uses to receive blocks of data it stores in globalPipeData.</span></span>

<span data-ttu-id="745ff-116">Die receivelongs-Funktion deklariert eine Pipe und ordnet Speicherplatz für die Variable der globalen Daten Senke zu.</span><span class="sxs-lookup"><span data-stu-id="745ff-116">The ReceiveLongs function declares a pipe and allocates memory space for the global data sink variable.</span></span> <span data-ttu-id="745ff-117">In Ihrem Client/Server-Programm kann die Daten Senke eine vom Client erstellte Datei-oder Datenstruktur sein.</span><span class="sxs-lookup"><span data-stu-id="745ff-117">In your client/server program, the data sink can be a file or data structure the client creates.</span></span> <span data-ttu-id="745ff-118">In diesem einfachen Beispiel ist die Datenquelle ein dynamisch zugewiesener Puffer mit langen ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="745ff-118">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="745ff-119">Bevor die Datenübertragung beginnen kann, muss das Client Programm die ausgabepipestruktur initialisieren.</span><span class="sxs-lookup"><span data-stu-id="745ff-119">Before the data transfer can begin, your client program must initialize the output pipe structure.</span></span> <span data-ttu-id="745ff-120">Sie muss Zeiger auf die Zustands Variable, die pushprozedur und die zuordnungsprozedur festlegen.</span><span class="sxs-lookup"><span data-stu-id="745ff-120">It must set pointers to the state variable, the push procedure, and the alloc procedure.</span></span> <span data-ttu-id="745ff-121">In diesem Beispiel heißt die ausgabepipe-Variable outputpipe.</span><span class="sxs-lookup"><span data-stu-id="745ff-121">In this example, the output pipe variable is called outputPipe.</span></span>

<span data-ttu-id="745ff-122">Clients signalisieren Servern, dass Sie bereit sind, Daten zu empfangen, indem Sie eine Remote Prozedur auf dem Server aufrufen.</span><span class="sxs-lookup"><span data-stu-id="745ff-122">Clients signal servers that they are ready to receive data by invoking a remote procedure on the server.</span></span> <span data-ttu-id="745ff-123">In diesem Beispiel wird die Remote Prozedur als outpipe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="745ff-123">In this example, the remote procedure is called OutPipe.</span></span> <span data-ttu-id="745ff-124">Wenn der Client die Remote Prozedur aufruft, beginnt der Server mit der Datenübertragung.</span><span class="sxs-lookup"><span data-stu-id="745ff-124">When the client calls the remote procedure, the server begins the data transfer.</span></span> <span data-ttu-id="745ff-125">Jedes Mal, wenn Daten eintreffen, ruft der Clientstub die Zustellungs-und pushprozeduren des Clients nach Bedarf auf.</span><span class="sxs-lookup"><span data-stu-id="745ff-125">Each time data arrives, the client stub calls the client's alloc and push procedures as needed.</span></span>

<span data-ttu-id="745ff-126">Anstatt Arbeitsspeicher jedes Mal zuzuweisen, wenn ein Puffer benötigt wird, legt die Zuordnungs Prozedur in diesem Beispiel einfach einen Zeiger auf die Variable globalbuffer fest.</span><span class="sxs-lookup"><span data-stu-id="745ff-126">Rather than allocate memory each time a buffer is needed, the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="745ff-127">Der Pull-Vorgang wird dann bei jedem Datentransfer erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="745ff-127">The pull procedure then reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="745ff-128">Komplexere Client Programme müssen möglicherweise jedes Mal einen neuen Puffer zuordnen, wenn der Serverdaten vom Client abruft.</span><span class="sxs-lookup"><span data-stu-id="745ff-128">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="745ff-129">Das Push-Verfahren in diesem Beispiel verwendet die State-Variable, um die nächste Position zu verfolgen, an der die Daten im globalen Daten Senke-Puffer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="745ff-129">The push procedure in this example uses the state variable to track the next position where it will store data in the global data sink buffer.</span></span> <span data-ttu-id="745ff-130">Er schreibt Daten aus dem Pipe-Puffer in den Senke Puffer.</span><span class="sxs-lookup"><span data-stu-id="745ff-130">It writes data from the pipe buffer into sink buffer.</span></span> <span data-ttu-id="745ff-131">Der Client-Stub empfängt dann den nächsten Datenblock vom Server und speichert ihn im Pipepuffer.</span><span class="sxs-lookup"><span data-stu-id="745ff-131">The client stub then receives the next block of data from the server and stores it in the pipe buffer.</span></span> <span data-ttu-id="745ff-132">Wenn alle Daten gesendet wurden, überträgt der Server einen Puffer der Größe 0 (null).</span><span class="sxs-lookup"><span data-stu-id="745ff-132">When all the data has been sent, the server transmits a zero-sized buffer.</span></span> <span data-ttu-id="745ff-133">Dies gibt die pushprozedur an, um den Empfang von Daten zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="745ff-133">This cues the push procedure to stop receiving data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="745ff-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="745ff-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="745ff-135">Kanal</span><span class="sxs-lookup"><span data-stu-id="745ff-135">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="745ff-136">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="745ff-136">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 