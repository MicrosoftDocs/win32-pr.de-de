---
description: Die Installation eines neuen Dienstanbieters ist hochgradig Geräte-und betriebssystemspezifisch, sodass die Details nicht in den Rahmen dieses SDK fallen.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installation und Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362683"
---
# <a name="installation-and-initialization"></a><span data-ttu-id="5f23d-103">Installation und Initialisierung</span><span class="sxs-lookup"><span data-stu-id="5f23d-103">Installation and Initialization</span></span>

<span data-ttu-id="5f23d-104">Die Installation eines neuen Dienstanbieters ist hochgradig Geräte-und betriebssystemspezifisch, sodass die Details nicht in den Rahmen dieses SDK fallen.</span><span class="sxs-lookup"><span data-stu-id="5f23d-104">Installation of a new service provider is highly device- and operating-system-specific, so the details are outside the scope of this SDK.</span></span> <span data-ttu-id="5f23d-105">Im Allgemeinen ist das Ziel der Installation die Konfiguration des Dienstanbieters für die aktuelle Kommunikationsumgebung.</span><span class="sxs-lookup"><span data-stu-id="5f23d-105">Generally speaking, the goal of installation is configuration of the service provider for the current communications environment.</span></span> <span data-ttu-id="5f23d-106">Dabei handelt es sich in der Regel um Registrierungseinträge und die Einstellung von Dienst Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="5f23d-106">This usually involves registry entries and the setting of service dependencies.</span></span>

<span data-ttu-id="5f23d-107">Die Initialisierung eines Telefoniedienstanbieters beginnt mit der Versions Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="5f23d-107">Initialization of a telephony service provider starts with version negotiation.</span></span> <span data-ttu-id="5f23d-108">Eine Erörterung der Versions Aushandlung und der aktuellen Version finden Sie unter [TSPI-Versions](tspi-versioning.md) Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="5f23d-108">See [TSPI Versioning](tspi-versioning.md) for a discussion of version negotiation and current version.</span></span>

<span data-ttu-id="5f23d-109">TAPI ruft dann [**TSPI \_ providerinit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)auf, die dem Anbieter einen Zeiger auf eine Rückruffunktion übergibt, mit der der Fortschritt der asynchronen Funktionen gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="5f23d-109">TAPI then calls [**TSPI\_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), which passes the provider a pointer to a callback function used to report on asynchronous functions progress.</span></span> <span data-ttu-id="5f23d-110">Der TSP gibt die Anzahl der Zeilen-und Telefongeräte zurück, die mit dem aktuellen Geräte Bezeichner verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="5f23d-110">The TSP returns a count of line and phone devices associated with the current device identifier.</span></span>

<span data-ttu-id="5f23d-111">In der Regel ist der nächste Schritt die Ressourcen Inventur, die von TAPI durchgeführt wird, indem [**TSPI \_ linegetdevcaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) und [**TSPI \_ linegetaddresscaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5f23d-111">Typically, the next step will be resource inventory, conducted by TAPI invoking [**TSPI\_lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) and [**TSPI\_lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span></span> <span data-ttu-id="5f23d-112">Der Dienstanbieter soll die Elemente der beteiligten Datenstrukturen ausfüllen, die sich auf die von ihm unterstützten Geräte-und Sitzungs Funktionen beziehen.</span><span class="sxs-lookup"><span data-stu-id="5f23d-112">The service provider is expected to fill in those elements of the data structures involved that pertain to device and session capabilities it supports.</span></span>

<span data-ttu-id="5f23d-113">TAPI sammelt Informationen aus den verschiedenen Anwendungen bezüglich der Ereignis Benachrichtigungs Anforderungen und weist den TSP mit [**TSPI \_ linesetdefaultmediadetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) an, um anzugeben, welche Medientypen für eine Zeile und [**TSPI \_ linesetstatus-Meldungen**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) erkannt werden sollen, um anzugeben, welche Zeilen-und Adress Ereignisse gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f23d-113">TAPI collects information from the various applications concerning event notification requirements, and instructs the TSP using [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) to indicate which media types to detect for a line and [**TSPI\_lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) to indicate which line and address events should be reported.</span></span>

 

 
