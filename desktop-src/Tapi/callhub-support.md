---
description: Die callhub-Nachverfolgung ist ein neues Feature in TAPI, Version 3,0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Callhub-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362338"
---
# <a name="callhub-support"></a><span data-ttu-id="f7bff-103">Callhub-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="f7bff-103">CallHub Support</span></span>

<span data-ttu-id="f7bff-104">Die callhub-Nachverfolgung ist ein neues Feature in TAPI, Version 3,0.</span><span class="sxs-lookup"><span data-stu-id="f7bff-104">CallHub tracking is a new feature in TAPI version 3.0.</span></span> <span data-ttu-id="f7bff-105">Die callhub-Funktionalität wurde den Programmier Elementen TAPI 2,1 mit der Übermittlung von Windows 2000 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f7bff-105">CallHub functionality was added to the TAPI 2.1 programming elements with the delivery of Windows 2000.</span></span> <span data-ttu-id="f7bff-106">Ein *callhub* stellt eine Drittanbieter Ansicht eines Aufrufes dar, und die Aufruf Handles von TAPI stellen die erste Ansicht eines Aufrufes dar.</span><span class="sxs-lookup"><span data-stu-id="f7bff-106">A *CallHub* represents a third-party view of a call, and TAPI's call handles represent the first-party view of a call.</span></span> <span data-ttu-id="f7bff-107">Bei der callhub-Nachverfolgung wird der Dienstanbieter aufgefordert, callhubs zu folgen und während der Lebensdauer eines callhubs Informationen über den Aufruf zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7bff-107">With CallHub tracking, the service provider is requested to follow CallHubs and give information about the call during the lifetime of a CallHub.</span></span> <span data-ttu-id="f7bff-108">Wenn neue Parteien beitreten und den callhub verlassen, sollte der Dienstanbieter TAPI informieren.</span><span class="sxs-lookup"><span data-stu-id="f7bff-108">As new parties join and leave the CallHub, the service provider should inform TAPI.</span></span>

<span data-ttu-id="f7bff-109">Ein Dienstanbieter muss keine neuen Funktionen implementieren, um callhub zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f7bff-109">A service provider does not need to implement any new functions in order to support CallHub.</span></span> <span data-ttu-id="f7bff-110">Er muss lediglich den **dwcallid** -Member der [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) -Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="f7bff-110">It simply needs to fill in the **dwCallID** member of the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="f7bff-111">In TAPI 3 sammelt TAPI alle Aufrufe mit dem gleichen **dwcallid** und erstellt ein callhub-handle, das von der Anwendung zum Nachverfolgen des Aufrufs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f7bff-111">In TAPI 3, TAPI collects all calls with the same **dwCallID** and creates a CallHub handle that the application can use to track the call.</span></span>

 

 
