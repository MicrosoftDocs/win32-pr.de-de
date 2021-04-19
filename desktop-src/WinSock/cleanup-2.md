---
description: Die Ws2 \_ -32.dll (und geschichtete Protokolle) werden für jeden Aufruf von WSPStartup einmal wspcleanup aufrufen.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Cleanup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372818"
---
# <a name="cleanup"></a><span data-ttu-id="61048-103">Cleanup</span><span class="sxs-lookup"><span data-stu-id="61048-103">Cleanup</span></span>

<span data-ttu-id="61048-104">Die Ws2 \_ -32.dll (und geschichtete Protokolle) werden für jeden Aufruf von [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)einmal [**wspcleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="61048-104">The Ws2\_32.dll (and layered protocols) will call [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) once for each invocation of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span> <span data-ttu-id="61048-105">Bei jedem Aufruf sollte **wspcleanup** einen pro-Prozess-Verweis Leistungswert verringern, und wenn der Leistungswert Null erreicht, muss sich der Dienstanbieter darauf vorbereiten, dass er aus dem Arbeitsspeicher entladen wird.</span><span class="sxs-lookup"><span data-stu-id="61048-105">On each invocation, **WSPCleanup** should decrement a per-process reference counter, and when the counter reaches zero, the service provider must prepare itself to be unloaded from memory.</span></span> <span data-ttu-id="61048-106">Die erste Geschäftsordnung besteht darin, die Übertragung von nicht gesendeten Daten an Sockets abzuschließen, die für eine ordnungsgemäße Schließung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="61048-106">The first order of business is to finish transmitting any unsent data on sockets that are configured for a graceful close.</span></span> <span data-ttu-id="61048-107">Anschließend werden alle Ressourcen, die vom Anbieter gehalten werden, freigegeben.</span><span class="sxs-lookup"><span data-stu-id="61048-107">Thereafter, any and all resources held by the provider are to be freed.</span></span> <span data-ttu-id="61048-108">Der Dienstanbieter muss in einem Zustand belassen werden, in dem er durch einen **WSPStartup**-Aufrufvorgang sofort erneut initialisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="61048-108">The service provider must be left in a state where it can be immediately reinitialized by a call to **WSPStartup**.</span></span>

 

 
