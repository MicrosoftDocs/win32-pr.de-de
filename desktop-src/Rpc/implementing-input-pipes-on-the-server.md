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
# <a name="implementing-input-pipes-on-the-server"></a>Implementieren von eingabepipes auf dem Server

Um mit dem Senden von Daten an einen Server zu beginnen, Ruft ein Client eine der Remote Prozeduren des Servers auf. Diese Prozedur muss die Pull-Prozedur wiederholt im Stub des Servers aufzurufen. Der mittlerer l-Compiler verwendet die IDL-Datei der Anwendung, um die Pull-Prozeduren des Servers automatisch zu generieren.

Jedes Mal, wenn das Serverprogramm die Pull-Prozedur im Stub aufruft, empfängt die Pull-Prozedur Datenblöcke vom Client. Dabei werden die Daten in den Puffer des Servers entmarshunplizierung. Die Remote Prozedur des Servers kann diese Daten dann in beliebiger Weise verarbeiten. Die Schleife wird fortgesetzt, bis der Server einen Puffer mit einer Länge von NULL erhält.

Das folgende Beispiel stammt aus dem pipedemo-Programm, das in den Beispielen für das Platform Software Development Kit (SDK) enthalten ist. Es wird eine Remote Server Prozedur veranschaulicht, die eine Pipe zum Abrufen von Daten vom Client zum Server verwendet.

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

 

 




