---
title: Suchen des Server Programms
description: Nachdem die Client seitige RPC-Laufzeit eine Verbindung mit einem im Bindungs handle angeforderten Server Host System hergestellt hat, wird der Server Prozess von der RPC-Lauf Zeit Bibliothek des Clients gefunden.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Auffinden des Server Programms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341241"
---
# <a name="finding-the-server-program"></a><span data-ttu-id="37235-104">Suchen des Server Programms</span><span class="sxs-lookup"><span data-stu-id="37235-104">Finding the Server Program</span></span>

<span data-ttu-id="37235-105">Nachdem die Client seitige RPC-Laufzeit eine Verbindung mit einem im Bindungs handle angeforderten Server Host System hergestellt hat, wird der Server Prozess von der RPC-Lauf Zeit Bibliothek des Clients gefunden.</span><span class="sxs-lookup"><span data-stu-id="37235-105">After the client side RPC run time connects to a server host system requested in the binding handle, the client RPC run-time library finds the server process.</span></span> <span data-ttu-id="37235-106">Zu diesem Zweck wird die Endpunkt Zuordnung auf dem Server Host System abgefragt.</span><span class="sxs-lookup"><span data-stu-id="37235-106">To do this, it queries the endpoint map on the server host system.</span></span> <span data-ttu-id="37235-107">Die Endpunkt Zuordnung enthält Informationen zu dem Endpunkt, an dem der Server lauscht.</span><span class="sxs-lookup"><span data-stu-id="37235-107">The endpoint map contains information about which endpoint the server is listening to.</span></span>

 

 




