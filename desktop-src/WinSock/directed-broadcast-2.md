---
description: In der Regel als mehr Netzwerk freundlich als bei einem Broadcast für alle Routen, wird eine gesteuerte Übertragung auf das von Ihnen angegebene lokale Netzwerk beschränkt.
ms.assetid: e2358580-5a65-434d-ba4c-a6b0615bccc3
title: Gesteuerte Übertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3a47bd47e9800e1f9c93cffa555b76feb77373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368077"
---
# <a name="directed-broadcast"></a><span data-ttu-id="374d5-103">Gesteuerte Übertragung</span><span class="sxs-lookup"><span data-stu-id="374d5-103">Directed Broadcast</span></span>

<span data-ttu-id="374d5-104">In der Regel als mehr Netzwerk freundlich als bei einem Broadcast für alle Routen, wird eine gesteuerte Übertragung auf das von Ihnen angegebene lokale Netzwerk beschränkt.</span><span class="sxs-lookup"><span data-stu-id="374d5-104">Generally considered more network friendly than an all-routes broadcast, a directed broadcast limits itself to the local network that you specify.</span></span> <span data-ttu-id="374d5-105">Füllen Sie **sa \_ netnum** mit der Zielnetzwerk Nummer und dem **sa- \_ nodenum** mit Binärdateien.</span><span class="sxs-lookup"><span data-stu-id="374d5-105">Fill **sa\_netnum** with the target network number and **sa\_nodenum** with binary ones.</span></span> <span data-ttu-id="374d5-106">Router leiten diese Anforderung an das Zielnetzwerk weiter, wo Sie zu einer lokalen Übertragung wird.</span><span class="sxs-lookup"><span data-stu-id="374d5-106">Routers forward this request to the destination network where it becomes a local broadcast.</span></span> <span data-ttu-id="374d5-107">Zwischen Netzwerken wird dieses Paket nicht als Broadcast angezeigt.</span><span class="sxs-lookup"><span data-stu-id="374d5-107">Intermediate networks do not see this packet as a broadcast.</span></span>

 

 



