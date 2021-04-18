---
description: Derzeit werden alle Aufrufe von-Aufrufen an Anwendungen übergegangen.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Timer für den CallState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357386"
---
# <a name="call-state-timer"></a><span data-ttu-id="bc357-103">Timer für den CallState</span><span class="sxs-lookup"><span data-stu-id="bc357-103">Call State Timer</span></span>

<span data-ttu-id="bc357-104">Derzeit werden alle Aufrufe von-Aufrufen an Anwendungen übergegangen.</span><span class="sxs-lookup"><span data-stu-id="bc357-104">Currently, all timing of calls is left up to applications.</span></span> <span data-ttu-id="bc357-105">Dies kann sehr aufwändiger sein, wenn die Anwendung eine große Anzahl von Aufrufen überwacht, und wenn mehrere Anwendungen vorhanden sind, möglicherweise auf mehreren Servern, kann es erforderlich sein, dass alle Timer bei denselben aufrufen gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="bc357-105">This can be burdensome if the application is monitoring a large number of calls, and if multiple applications are present, possibly on multiple servers, it can be necessary for them to all maintain timers on the same calls.</span></span> <span data-ttu-id="bc357-106">Daher ist es sinnvoller, die zeitliche Steuerung des Ansichts Zustands vom Server zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bc357-106">It therefore makes more sense for call state timing to be handled by the server.</span></span>

<span data-ttu-id="bc357-107">Das **tstateentrytime** -Element in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ermöglicht die zeitliche Steuerung von Aufrufen in Zuständen, die gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bc357-107">The **tStateEntryTime** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) allows timing of calls in states to be reported.</span></span> <span data-ttu-id="bc357-108">Der Member (des Typs **SysTime**) gibt den Zeitpunkt an, zu dem der aktuelle Status eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="bc357-108">The member (of type **SYSTIME**) indicates the time at which the current state was entered.</span></span>

 

 



