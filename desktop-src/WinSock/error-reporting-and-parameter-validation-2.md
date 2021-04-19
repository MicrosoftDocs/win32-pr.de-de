---
description: Das Schema für die Fehlerberichterstattung unterscheidet sich zwischen den SPI-und API-Schnittstellen.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Fehlerberichterstattung und Parameter Validierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346942"
---
# <a name="error-reporting-and-parameter-validation"></a><span data-ttu-id="ef208-103">Fehlerberichterstattung und Parameter Validierung</span><span class="sxs-lookup"><span data-stu-id="ef208-103">Error Reporting and Parameter Validation</span></span>

<span data-ttu-id="ef208-104">Das Schema für die Fehlerberichterstattung unterscheidet sich zwischen den SPI-und API-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="ef208-104">The scheme for error reporting differs between the SPI and API interfaces.</span></span> <span data-ttu-id="ef208-105">Windows Sockets Service-Anbieter melden Fehler zusammen mit der Funktion, die zurückgibt, im Gegensatz zu dem Thread basierten Ansatz, der in der API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef208-105">Windows Sockets service providers report errors along with the function returning, as opposed to the per-thread based approach utilized in the API.</span></span> <span data-ttu-id="ef208-106">Der Ws2 \_ -32.dll verwendet den Funktions spezifischen Fehlercode des Dienstanbieters, um den Fehlerwert pro Thread zu aktualisieren, der über die [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -API-Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef208-106">The Ws2\_32.dll uses the service provider's per-function error code to update the per-thread error value that is obtained through the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API function.</span></span> <span data-ttu-id="ef208-107">Dienstanbieter sind jedoch weiterhin erforderlich, um den pro-Socket-basierten Fehler beizubehalten, der über die Option "so Error Socket" abgerufen werden kann \_ .</span><span class="sxs-lookup"><span data-stu-id="ef208-107">Service providers are still required, however, to maintain the per-socket based error which can be retrieved through the SO\_ERROR socket option.</span></span>

<span data-ttu-id="ef208-108">Der Ws2- \_32.dll führt die Parameter Validierung nur bei Funktionsaufrufen aus, die vollständig in sich selbst implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef208-108">The Ws2\_32.dll performs parameter validation only on function calls that are implemented entirely within itself.</span></span> <span data-ttu-id="ef208-109">Dienstanbieter sind für die Durchführung ihrer eigenen Parameter Validierung verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="ef208-109">Service providers are responsible for performing all of their own parameter validation.</span></span>

 

 



