---
title: Entwicklung und Bereitstellung im Netzwerk
description: Die meisten Entwickler schreiben und testen Ihre Software auf einem schnellen zuverlässigen LAN.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036838"
---
# <a name="development-vs-deployment-in-the-network"></a><span data-ttu-id="e9c63-103">Entwicklung und Bereitstellung im Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e9c63-103">Development vs. Deployment in the Network</span></span>

<span data-ttu-id="e9c63-104">Die meisten Entwickler schreiben und testen Ihre Software auf einem schnellen zuverlässigen LAN.</span><span class="sxs-lookup"><span data-stu-id="e9c63-104">Most developers write and test their software on a fast reliable LAN.</span></span> <span data-ttu-id="e9c63-105">Client und Server befinden sich häufig in demselben Netzwerksegment.</span><span class="sxs-lookup"><span data-stu-id="e9c63-105">Their client and server are often on the same network segment.</span></span> <span data-ttu-id="e9c63-106">Unter solchen Umständen reagiert das Netzwerk selten nicht, und die Konnektivität geht selten verloren.</span><span class="sxs-lookup"><span data-stu-id="e9c63-106">In such circumstances the network is rarely unresponsive, and connectivity rarely lost.</span></span> <span data-ttu-id="e9c63-107">Bei der Bereitstellung in einer Kundenumgebung befinden sich Client und Server häufig in verschiedenen Netzwerksegmenten, die möglicherweise geografisch Remote sind, und der Server ist stark mit anderen Clients ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="e9c63-107">When deployed in a customer environment however, client and server are often on different network segments, possibly geographically remote, and the server is heavily loaded with other clients.</span></span> <span data-ttu-id="e9c63-108">Anders ausgedrückt: die Reaktionsfähigkeit des Netzwerks kann nicht angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="e9c63-108">In other words: network responsiveness cannot be assumed.</span></span>

<span data-ttu-id="e9c63-109">In diesem Artikel wird erläutert, wie robuste Client-/Serverarchitekturen erstellt werden, wenn die Unsicherheit durch ein intrinsisch unzuverlässiges Netzwerk und potenziell nicht verfügbare Server verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="e9c63-109">This article explains how to construct robust client/server architectures in the face of uncertainty introduced by an intrinsically unreliable network and potentially unavailable servers.</span></span>

 

 




