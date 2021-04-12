---
title: Eigenschaften von Message und Message Queue
description: Eine Nachricht verfügt über Eigenschaften, mit denen eine Bezeichnung, ein Nachrichtentext und eine Reihe von Optionen angegeben werden.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310516"
---
# <a name="message-and-message-queue-properties"></a><span data-ttu-id="15f00-103">Eigenschaften von Message und Message Queue</span><span class="sxs-lookup"><span data-stu-id="15f00-103">Message and Message Queue Properties</span></span>

<span data-ttu-id="15f00-104">Eine Nachricht verfügt über Eigenschaften, mit denen eine Bezeichnung, ein Nachrichtentext und eine Reihe von Optionen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15f00-104">A message has properties, which specify a label, a message body, and a number of options.</span></span> <span data-ttu-id="15f00-105">Nachrichten Eigenschaften Optionen können Servicequalität, Priorität, Journalisierung, Datenschutz und Authentifizierungs Ebenen sowie die Lebensdauer der Nachricht einschließen.</span><span class="sxs-lookup"><span data-stu-id="15f00-105">Message property options can include quality of service, priority, journaling, privacy and authentication levels, and the lifetime of the message.</span></span> <span data-ttu-id="15f00-106">In herkömmlichen Message Queuinganwendungen (nicht-RPC) geben Sie diese Eigenschaften durch Aufrufen der MSMQ-API-Funktionen oder der com-Objektmethoden an, die in der MSMQ SDK-Dokumentation beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="15f00-106">In conventional (non-RPC) message-queuing applications, you specify these properties by calling the MSMQ API functions or COM object methods, which are described in the MSMQ SDK documentation.</span></span> <span data-ttu-id="15f00-107">RPC-Client Anwendungen können bestimmte Eigenschaften für Remote Prozedur Aufrufe festlegen, indem [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) und [**rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="15f00-107">RPC client applications can set certain properties for remote procedure calls by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) and [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span> <span data-ttu-id="15f00-108">Nachdem die Eigenschaften festgelegt wurden, bleiben Sie für jede Nachricht wirksam, bis Sie von der Client Anwendung zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="15f00-108">Once set, the properties remain in effect for each message until the client application resets them.</span></span>

<span data-ttu-id="15f00-109">Eine Nachrichten Warteschlange verfügt über einen eigenen Satz von Eigenschaften, abgesehen von den Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="15f00-109">A message queue has its own set of properties, apart from those of the messages.</span></span> <span data-ttu-id="15f00-110">Diese Eigenschaften identifizieren eine Warteschlange eindeutig und definieren die Dienstklasse, die von der Warteschlange bereitgestellt wird, den Datenschutz und die Authentifizierungs Stufen, die für die Nachrichten in dieser Warteschlange erforderlich sind, und ob die Nachrichten Teil einer verteilten Transaktion sind.</span><span class="sxs-lookup"><span data-stu-id="15f00-110">These properties uniquely identify a queue and define the class of service that the queue provides, the privacy and authentication levels required for messages in this queue, and whether the messages are to be part of a distributed transaction.</span></span> <span data-ttu-id="15f00-111">Wie bei den Nachrichten Eigenschaften geben Sie die Eigenschaften einer Nachrichten Warteschlange an, indem Sie die MSMQ-API-Funktionen oder com-Objektmethoden aufrufen, die in der MSMQ-Dokumentation beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="15f00-111">As with message properties, you specify the properties of a message queue by calling the MSMQ API functions or COM object methods, which are described in the MSMQ documentation.</span></span> <span data-ttu-id="15f00-112">Eine RPC-Serveranwendung kann jedoch Eigenschaften der eigenen Empfangs Warteschlange angeben, wenn [**rpcserveruseprotseqepex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) zum Einrichten der Bindung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="15f00-112">However, an RPC server application can specify properties of its own receive queue when it calls [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) to establish the binding.</span></span>

 

 




