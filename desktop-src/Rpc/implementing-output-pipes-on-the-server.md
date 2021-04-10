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
# <a name="implementing-output-pipes-on-the-server"></a><span data-ttu-id="b3546-103">Implementieren von ausgabepipes auf dem Server</span><span class="sxs-lookup"><span data-stu-id="b3546-103">Implementing Output Pipes on the Server</span></span>

<span data-ttu-id="b3546-104">Um mit dem Empfang von Daten von einem Server zu beginnen, Ruft ein Client eine der Remote Prozeduren des Servers auf.</span><span class="sxs-lookup"><span data-stu-id="b3546-104">To begin receiving data from a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="b3546-105">Diese Prozedur muss das Push-Verfahren wiederholt im Stub des Servers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3546-105">This procedure must repeatedly call the push procedure in the server's stub.</span></span> <span data-ttu-id="b3546-106">Der mittlerer l-Compiler verwendet die IDL-Datei der Anwendung, um die Push-Prozedur des Servers automatisch zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b3546-106">The MIDL compiler uses the application's IDL file to automatically generate the server's push procedure.</span></span>

<span data-ttu-id="b3546-107">Die Remote Server Routine muss den Puffer der ausgabepipe mit Daten füllen, bevor die pushprozedur aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b3546-107">The remote server routine must fill the output pipe's buffer with data before it calls the push procedure.</span></span> <span data-ttu-id="b3546-108">Jedes Mal, wenn das Serverprogramm das Push-Verfahren im Stub aufruft, werden die Daten von der Push-Prozedur an den Client übertragen und an den Client übermittelt.</span><span class="sxs-lookup"><span data-stu-id="b3546-108">Each time the server program invokes the push procedure in its stub, the push procedure marshals the data and transmits it to the client.</span></span> <span data-ttu-id="b3546-109">Die Schleife wird fortgesetzt, bis der Server einen Puffer der Länge 0 (null) sendet.</span><span class="sxs-lookup"><span data-stu-id="b3546-109">The loop continues until the server sends a buffer of zero length.</span></span>

<span data-ttu-id="b3546-110">Das folgende Beispiel stammt aus dem pipedemo-Programm, das in den Beispielen für die Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b3546-110">The following example is from the Pipedemo program contained in the samples that come with the Windows SDK.</span></span> <span data-ttu-id="b3546-111">Es wird eine Remote Server Prozedur veranschaulicht, die eine Pipe verwendet, um Daten vom Server an den Client zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="b3546-111">It illustrates a remote server procedure that uses a pipe to push data from the server to the client.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b3546-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3546-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3546-113">Kanal</span><span class="sxs-lookup"><span data-stu-id="b3546-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="b3546-114">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="b3546-114">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 