---
title: Abrufen von MCI-System Informationen
description: Abrufen von MCI-System Informationen
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947618"
---
# <a name="obtaining-mci-system-information"></a><span data-ttu-id="73a5f-104">Abrufen von MCI-System Informationen</span><span class="sxs-lookup"><span data-stu-id="73a5f-104">Obtaining MCI System Information</span></span>

<span data-ttu-id="73a5f-105">Der [sysinfo](sysinfo.md) ([**MCI \_ sysinfo**](mci-sysinfo.md))-Befehl ruft Systeminformationen zu MCI-Geräten ab.</span><span class="sxs-lookup"><span data-stu-id="73a5f-105">The [sysinfo](sysinfo.md) ([**MCI\_SYSINFO**](mci-sysinfo.md)) command obtains system information about MCI devices.</span></span> <span data-ttu-id="73a5f-106">MCI verarbeitet diesen Befehl, ohne ihn an ein beliebiges MCI-Gerät weiterleiten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="73a5f-106">MCI handles this command without relaying it to any MCI device.</span></span> <span data-ttu-id="73a5f-107">Für die befehlsnachrichten Schnittstelle gibt MCI die Systeminformationen in der [**MCI- \_ sysinfo \_**](mci-sysinfo-parms.md) -Struktur des Parametern zurück.</span><span class="sxs-lookup"><span data-stu-id="73a5f-107">For the command-message interface, MCI returns the system information in the [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

<span data-ttu-id="73a5f-108">Sie können den **sysinfo** (MCI \_ sysinfo)-Befehl verwenden, um Informationen wie die Anzahl der MCI-Geräte auf einem System, die Anzahl der MCI-Geräte eines bestimmten Typs, die Anzahl der geöffneten MCI-Geräte und die Namen der Geräte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="73a5f-108">You can use the **sysinfo** (MCI\_SYSINFO) command to retrieve information such as the number of MCI devices on a system, the number of MCI devices of a particular type, the number of open MCI devices, and the names of the devices.</span></span> <span data-ttu-id="73a5f-109">Dieser Befehl wird häufig mehrmals aufgerufen, um ein bestimmtes Informationselement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="73a5f-109">This command is often called more than once to retrieve a particular piece of information.</span></span> <span data-ttu-id="73a5f-110">Beispielsweise können Sie die Anzahl der Geräte eines bestimmten Typs im ersten-Befehl Abrufen und dann die Namen der Geräte in der nächsten Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="73a5f-110">For example, you might retrieve the number of devices of a particular type in the first call and then enumerate the names of the devices in the next.</span></span>

 

 




