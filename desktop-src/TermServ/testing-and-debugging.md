---
title: Testen und Debuggen
description: Es ist ein \ 0034; Echo \ 0034; vorhanden. der Listener, der vom RDC-Client (Remotedesktopverbindung) implementiert wird und auf eingehende Verbindungen lauscht.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338165"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="9a8da-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="9a8da-103">Testing and Debugging</span></span>

<span data-ttu-id="9a8da-104">Es gibt einen "Echo"-Listener, der vom RDC-Client (Remotedesktopverbindung) implementiert wird, der immer vorhanden ist und auf eingehende Verbindungen lauscht.</span><span class="sxs-lookup"><span data-stu-id="9a8da-104">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span> <span data-ttu-id="9a8da-105">Wenn Sie die Serverseite eines Moduls eines dynamischen virtuellen Kanals (DVC) schreiben, können Sie als Schnelltest einen Endpunkt mit dem Namen "Echo" öffnen.</span><span class="sxs-lookup"><span data-stu-id="9a8da-105">When you are writing the server side of a dynamic virtual channel (DVC) module, as a quick test you can open an endpoint named "ECHO".</span></span> <span data-ttu-id="9a8da-106">Jeder Schreibvorgang in einen Kanal, der von diesem Endpunkt aus instanziiert wird, führt zum Empfang der gleichen Daten.</span><span class="sxs-lookup"><span data-stu-id="9a8da-106">Any write to a channel that is instantiated from this endpoint will result in the receipt of the same data.</span></span>

<span data-ttu-id="9a8da-107">Mit dieser Technik können Sie eine Eingabe-/Ausgabe-Implementierung (e/a) des serverseitigen Moduls testen, um die Reaktionszeit für ein Remotedesktopverbindung (RDC)-Client-Plug-in zu messen oder um die Netzwerkverzögerung für den Remotedesktopverbindung-Client (RDC) zu messen.</span><span class="sxs-lookup"><span data-stu-id="9a8da-107">You can use this technique to test an input/output (I/O) implementation of the server-side module, to measure the response time for a Remote Desktop Connection (RDC) client plug-in, or to measure the network delay for the Remote Desktop Connection (RDC) client.</span></span> <span data-ttu-id="9a8da-108">Es gibt keine Einschränkung hinsichtlich der Datenmenge, die über diesen Kanal gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9a8da-108">There is no limitation on the amount of data that can be sent over this channel.</span></span>

 

 




