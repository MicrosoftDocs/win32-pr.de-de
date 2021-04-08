---
title: Implementieren von eingabepipes auf dem Server
description: Um mit dem Senden von Daten an einen Server zu beginnen, Ruft ein Client eine der Remote Prozeduren des Servers auf.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856331"
---
# <a name="implementing-input-pipes-on-the-server"></a><span data-ttu-id="b0899-103">Implementieren von eingabepipes auf dem Server</span><span class="sxs-lookup"><span data-stu-id="b0899-103">Implementing Input Pipes on the Server</span></span>

<span data-ttu-id="b0899-104">Um mit dem Senden von Daten an einen Server zu beginnen, Ruft ein Client eine der Remote Prozeduren des Servers auf.</span><span class="sxs-lookup"><span data-stu-id="b0899-104">To begin sending data to a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="b0899-105">Diese Prozedur muss die Pull-Prozedur wiederholt im Stub des Servers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b0899-105">This procedure must repeatedly call the pull procedure in the server's stub.</span></span> <span data-ttu-id="b0899-106">Der mittlerer l-Compiler verwendet die IDL-Datei der Anwendung, um die Pull-Prozeduren des Servers automatisch zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b0899-106">The MIDL compiler uses the application's IDL file to automatically generate the server's pull procedure.</span></span>

<span data-ttu-id="b0899-107">Jedes Mal, wenn das Serverprogramm die Pull-Prozedur im Stub aufruft, empfängt die Pull-Prozedur Datenblöcke vom Client.</span><span class="sxs-lookup"><span data-stu-id="b0899-107">Each time the server program invokes the pull procedure in its stub, the pull procedure receives blocks of data from the client.</span></span> <span data-ttu-id="b0899-108">Dabei werden die Daten in den Puffer des Servers entmarshunplizierung.</span><span class="sxs-lookup"><span data-stu-id="b0899-108">It unmarshals the data into the server's buffer.</span></span> <span data-ttu-id="b0899-109">Die Remote Prozedur des Servers kann diese Daten dann in beliebiger Weise verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b0899-109">The server's remote procedure can then process this data in any way required.</span></span> <span data-ttu-id="b0899-110">Die Schleife wird fortgesetzt, bis der Server einen Puffer mit einer Länge von NULL erhält.</span><span class="sxs-lookup"><span data-stu-id="b0899-110">The loop continues until the server receives a buffer of zero length.</span></span>

<span data-ttu-id="b0899-111">Das folgende Beispiel stammt aus dem pipedemo-Programm, das in den Beispielen für das Platform Software Development Kit (SDK) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b0899-111">The following example is from the Pipedemo program contained in the samples that come with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="b0899-112">Es wird eine Remote Server Prozedur veranschaulicht, die eine Pipe zum Abrufen von Daten vom Client zum Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0899-112">It illustrates a remote server procedure that uses a pipe to pull data from the client to the server.</span></span>

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

 

 




