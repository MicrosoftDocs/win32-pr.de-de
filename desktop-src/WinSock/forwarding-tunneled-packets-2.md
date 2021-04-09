---
description: Der Code weist eine Einschränkung auf, die gekapselte (getunnerte) Pakete empfängt und Sie in eine bestimmte Schnittstelle demultipleert.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: IPv6-Weiterleitungs Tunneled-Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862568"
---
# <a name="ipv6-forwarding-tunneled-packets"></a><span data-ttu-id="b9479-103">IPv6-Weiterleitungs Tunneled-Pakete</span><span class="sxs-lookup"><span data-stu-id="b9479-103">IPv6 Forwarding Tunneled Packets</span></span>

<span data-ttu-id="b9479-104">Der Code weist eine Einschränkung auf, die gekapselte (getunnerte) Pakete empfängt und Sie in eine bestimmte Schnittstelle demultipleert.</span><span class="sxs-lookup"><span data-stu-id="b9479-104">There is a limitation in the code that receives encapsulated (tunneled) packets and demultiplexes them to a specific interface.</span></span> <span data-ttu-id="b9479-105">Wenn Sie über einen konfigurierten Tunnel empfangene getunnelt-Pakete weiterleiten möchten, müssen Sie die Weiterleitung an allen sechs über vier Schnittstellen und Schnittstelle \# 2 aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b9479-105">If you want to forward tunneled packets received through a configured tunnel, then it is necessary to enable forwarding on any 6-over-4 interfaces as well as interface \#2.</span></span> <span data-ttu-id="b9479-106">Das Aktivieren der Weiterleitung auf Schnittstelle \# 2 funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="b9479-106">Just enabling forwarding on interface \#2 will not work.</span></span> <span data-ttu-id="b9479-107">Wenn Sie einen Router konfigurieren, aktivieren Sie in der Regel die Weiterleitung an allen Schnittstellen außer Loopback.</span><span class="sxs-lookup"><span data-stu-id="b9479-107">Typically when configuring a router, you would enable forwarding on all interfaces except loopback.</span></span>

 

 



