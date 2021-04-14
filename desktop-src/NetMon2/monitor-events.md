---
description: Monitore wurden für die Verwendung von Windows-Verwaltungsinstrumentation (WMI) zum Auslösen von Ereignissen auf lokalen Computern oder Remote Computern konzipiert.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Überwachen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485147"
---
# <a name="monitor-events"></a><span data-ttu-id="28ad2-103">Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="28ad2-103">Monitor Events</span></span>

<span data-ttu-id="28ad2-104">Monitore wurden für die Verwendung von [Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) zum Auslösen von Ereignissen auf lokalen Computern oder Remote Computern konzipiert.</span><span class="sxs-lookup"><span data-stu-id="28ad2-104">Monitors are designed to use [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to fire events to local or remote computers.</span></span>

> [!Note]  
> <span data-ttu-id="28ad2-105">Da Monitore eine echt Zeiterfassung verwenden, können Sie nur Daten auf dem lokalen Computer erfassen.</span><span class="sxs-lookup"><span data-stu-id="28ad2-105">Because monitors use a real-time capture they can only capture data at the local computer.</span></span> <span data-ttu-id="28ad2-106">Dies ist eine Einschränkung der **untc** -Schnittstelle des Netzwerk Paket Anbieters.</span><span class="sxs-lookup"><span data-stu-id="28ad2-106">This is a limitation of the network packet provider's **IRTC** interface.</span></span> <span data-ttu-id="28ad2-107">Mithilfe von WMI-Ereignissen können die erfassten Daten jedoch lokal überprüft werden, während Ereignisse an lokale oder Remote Computer gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="28ad2-107">However, by using WMI events, the captured data can be examined locally while events can be sent to local or remote computers.</span></span>

 

<span data-ttu-id="28ad2-108">Monitore kommunizieren nicht direkt mit WMI.</span><span class="sxs-lookup"><span data-stu-id="28ad2-108">Monitors do not communicate directly with WMI.</span></span> <span data-ttu-id="28ad2-109">Der [*Überwachungs Steuerungs Dienst (Monitor Control Service*](m.md) , mcsvc) stellt eine Schnittstelle (" [imonitoreventer Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter Enter](imonitoreventer.md))" bereit, mit der der Monitor eine Ereignisdaten Struktur</span><span class="sxs-lookup"><span data-stu-id="28ad2-109">The [*Monitor Control Service*](m.md) (MCSVC) provides an interface (called [IMonitorEventer](imonitoreventer.md)), which the monitor can use to obtain an event data structure and fill it with the relevant information.</span></span> <span data-ttu-id="28ad2-110">Die mcsvc kann dann die Ereignisdaten Struktur an WMI senden, wodurch wiederum das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="28ad2-110">The MCSVC can then send the event data structure to WMI, which in turn fires the event.</span></span>

 

 
