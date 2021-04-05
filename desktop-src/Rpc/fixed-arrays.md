---
title: Fixierte Arrays
description: Wenn die Schnittstelle ein Array mit einer bestimmten Anzahl von Elementen als Parameter angibt, wird ein festes Array verwendet. Bei der Verwendung von "Mittel l" definieren Sie fixierte Arrays auf die gleiche Weise, wie Sie Sie in C definieren. Sie geben den Typ, den Namen und die Größe des Arrays an.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711430"
---
# <a name="fixed-arrays"></a><span data-ttu-id="3bd93-104">Fixierte Arrays</span><span class="sxs-lookup"><span data-stu-id="3bd93-104">Fixed Arrays</span></span>

<span data-ttu-id="3bd93-105">Wenn die Schnittstelle ein Array mit einer bestimmten Anzahl von Elementen als Parameter angibt, wird ein festes Array verwendet.</span><span class="sxs-lookup"><span data-stu-id="3bd93-105">If your interface specifies an array with a specific number of elements as a parameter, it is using a fixed array.</span></span> <span data-ttu-id="3bd93-106">Bei der Verwendung von "Mittel l" definieren Sie fixierte Arrays auf die gleiche Weise, wie Sie Sie in C definieren. Sie geben den Typ, den Namen und die Größe des Arrays an.</span><span class="sxs-lookup"><span data-stu-id="3bd93-106">When using MIDL, you define fixed arrays in the same way you define them in C. You specify the array's type, name, and size.</span></span>

<span data-ttu-id="3bd93-107">Im folgenden Beispiel wird veranschaulicht, wie ein festes Array definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3bd93-107">The following example demonstrates how to define a fixed array.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="3bd93-108">Wenn ein Client Programm ein festes Array an ein Serverprogramm übergibt, sendet der Clientstub das gesamte Array an den Serverstub.</span><span class="sxs-lookup"><span data-stu-id="3bd93-108">When a client program passes a fixed array to a server program, the client stub sends the entire array to the server stub.</span></span> <span data-ttu-id="3bd93-109">Der Serverstub ordnet Speicher für das Array zu und speichert die Array Daten, die er über das Netzwerk empfängt, in den zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3bd93-109">The server stub allocates memory for the array and stores the array data it receives across the network into the allocated memory.</span></span> <span data-ttu-id="3bd93-110">Anschließend wird das Array an die Remote Prozedur auf dem Server weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="3bd93-110">It then passes the array to the remote procedure on the server.</span></span> <span data-ttu-id="3bd93-111">Der Server kann die Daten im Array ändern.</span><span class="sxs-lookup"><span data-stu-id="3bd93-111">The server may modify the data in the array.</span></span>

<span data-ttu-id="3bd93-112">Wenn die Remote Prozedur beendet wird, sendet der Server-Stub den Inhalt des Arrays an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="3bd93-112">When the remote procedure terminates, the server stub sends the contents of the array back to the client.</span></span> <span data-ttu-id="3bd93-113">Der Client-Stub kopiert die Daten, die er aus dem Serverstub empfangen hat, in das ursprüngliche Array.</span><span class="sxs-lookup"><span data-stu-id="3bd93-113">The client stub copies the data it received from the server stub into the original array.</span></span> <span data-ttu-id="3bd93-114">Das Client Programm kann dann die Daten wie beim Empfang der Daten von einem lokalen Prozedur aufrufsvorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bd93-114">The client program can then use the data as it would if it received the data from a local procedure call.</span></span>

 

 




