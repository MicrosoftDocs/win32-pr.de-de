---
title: Senden des Aufrufes an das Server Programm
description: Sobald die Client seitige RPC-Laufzeit eine Verbindung mit dem Server Endpunkt hergestellt hat, Marshalls Sie die Argumente und sendet Sie an den Server.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Senden des Aufrufs an den Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310932"
---
# <a name="sending-the-call-to-the-server-program"></a><span data-ttu-id="632c9-104">Senden des Aufrufes an das Server Programm</span><span class="sxs-lookup"><span data-stu-id="632c9-104">Sending the Call to the Server Program</span></span>

<span data-ttu-id="632c9-105">Sobald die Client seitige RPC-Laufzeit eine Verbindung mit dem Server Endpunkt hergestellt hat, Marshalls Sie die Argumente und sendet Sie an den Server.</span><span class="sxs-lookup"><span data-stu-id="632c9-105">Once the client side RPC run time has connected to the server endpoint, it marshalls the arguments and sends them to the server.</span></span> <span data-ttu-id="632c9-106">Die RPC-Laufzeit des Servers übergibt die marshallte Argumente an den Stub, der Sie unmarshallt und dann an die Server Routinen übergibt.</span><span class="sxs-lookup"><span data-stu-id="632c9-106">The server RPC run time gives the marshalled arguments to the stub that unmarshalls them, and then passes them to the server routines.</span></span> <span data-ttu-id="632c9-107">Beim Zurückgeben der Server Routinen übernimmt der Stub die \[ out \] -und \[ in-out- \] Parameter und den Rückgabewert, marshallt Sie und sendet die marshallte Daten an die RPC-Laufzeit des Servers.</span><span class="sxs-lookup"><span data-stu-id="632c9-107">When the server routines return, the stub picks up the \[out\] and \[in,out\] parameters and the return value, marshalls them, and sends the marshalled data to the server RPC run time.</span></span> <span data-ttu-id="632c9-108">Die RPC-Laufzeit sendet die Daten an den Client zurück, wobei die RPC-Laufzeit des Clients Sie an den Client seitigen Stub übergibt, der Sie unmarshalls und an den Aufrufer zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="632c9-108">The RPC run time sends the data back to the client, where the client RPC run time hands them off to the client side stub that unmarshalls them and returns them to the caller.</span></span>

 

 




