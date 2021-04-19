---
description: Um zu verhindern, dass sich Anrufe im Telefoniesystem befinden, löscht TAPI die von einem Dienstanbieter signalisierten Aufrufe, wenn eine Anwendung nicht als anfänglicher Besitzer des Aufrufs identifiziert werden kann.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Nicht im Besitz befindliche Anrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349027"
---
# <a name="unowned-calls"></a><span data-ttu-id="6e95a-103">Nicht im Besitz befindliche Anrufe</span><span class="sxs-lookup"><span data-stu-id="6e95a-103">Unowned Calls</span></span>

<span data-ttu-id="6e95a-104">Um zu verhindern, dass sich Anrufe im Telefoniesystem befinden, löscht TAPI die von einem Dienstanbieter signalisierten Aufrufe, wenn eine Anwendung nicht als anfänglicher Besitzer des Aufrufs identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e95a-104">To prevent unowned calls from being in the telephony system, TAPI drops calls that have been signaled up from a service provider if it cannot identify an application to be the initial owner of the call.</span></span> <span data-ttu-id="6e95a-105">In TAPI, Version 2,0 und höher, ruft TAPI die [**TSPI-Funktion \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) auf, um den Aufruf zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6e95a-105">In TAPI version 2.0 and later, TAPI calls the [**TSPI\_lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) function to drop the call.</span></span>

<span data-ttu-id="6e95a-106">Der Dienstanbieter kann im Voraus wissen, ob eine Anwendung verfügbar ist, um den Besitz eines neuen Aufrufes zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="6e95a-106">The service provider can know in advance whether or not there is an application available to take ownership of a new call.</span></span> <span data-ttu-id="6e95a-107">TAPI informiert den Dienstanbieter stets über die Medientypen, für die eine Anwendung verfügbar ist, indem er die Funktion [**TSPI \_ linesetdefaultmediadetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e95a-107">TAPI always informs the service provider of the media types for which there is an application available by using the [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) function.</span></span>

<span data-ttu-id="6e95a-108">Wenn ein Dienstanbieter z. b. feststellt, dass ein aktiver Aufruf in der Zeile mit linemediamode \_ interactivevoice Mode vorhanden ist, sollte die Standard Medien Erkennung überprüft werden, bevor die [**Zeilen- \_ newcall-**](line-newcall.md) und die [**line \_ CallState**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) -Nachricht erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="6e95a-108">For example, if a service provider determines that there is an active call on the line having LINEMEDIAMODE\_INTERACTIVEVOICE mode, it should check the default media detection before generating the [**LINE\_NEWCALL**](line-newcall.md) and [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages.</span></span> <span data-ttu-id="6e95a-109">Wenn die Standard Medien Erkennung anzeigt, dass keine Anwendung nach einem linemediamode \_ interactivevoice-Befehl sucht, sollte der Dienstanbieter die Nachrichten nicht senden, da TAPI ihn sofort löscht.</span><span class="sxs-lookup"><span data-stu-id="6e95a-109">If the default media detection shows that no application is looking for a LINEMEDIAMODE\_INTERACTIVEVOICE call, the service provider should not send the messages because TAPI will immediately drop it.</span></span>

 

 
