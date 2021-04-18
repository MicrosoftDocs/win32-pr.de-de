---
description: Ein Zeit Anbieter wird als dll implementiert. Jede DLL kann mehrere Zeit Anbieter unterstützen. Jeder Anbieter ist für seine eigene Konfiguration und Synchronisierung verantwortlich.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Erstellen eines Zeit Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354868"
---
# <a name="creating-a-time-provider"></a><span data-ttu-id="a9b0c-105">Erstellen eines Zeit Anbieters</span><span class="sxs-lookup"><span data-stu-id="a9b0c-105">Creating a Time Provider</span></span>

<span data-ttu-id="a9b0c-106">Ein Zeit Anbieter wird als dll implementiert.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-106">A time provider is implemented as a DLL.</span></span> <span data-ttu-id="a9b0c-107">Jede DLL kann mehrere Zeit Anbieter unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-107">Each DLL can support multiple time providers.</span></span> <span data-ttu-id="a9b0c-108">Jeder Anbieter ist für seine eigene Konfiguration und Synchronisierung verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-108">Each provider is responsible for its own configuration and synchronization.</span></span>

<span data-ttu-id="a9b0c-109">Zeit Anbieter müssen die folgenden Rückruf Funktionen implementieren:</span><span class="sxs-lookup"><span data-stu-id="a9b0c-109">Time providers must implement the following callback functions:</span></span>

-   [<span data-ttu-id="a9b0c-110">**Timeprovclose**</span><span class="sxs-lookup"><span data-stu-id="a9b0c-110">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [<span data-ttu-id="a9b0c-111">**Timeprovcommand**</span><span class="sxs-lookup"><span data-stu-id="a9b0c-111">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [<span data-ttu-id="a9b0c-112">**Timeprovopen**</span><span class="sxs-lookup"><span data-stu-id="a9b0c-112">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

<span data-ttu-id="a9b0c-113">Nachdem die Anbieter-DLL geladen wurde, ruft der Zeit Anbieter-Manager [**timeprovopen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)auf und übergibt den Namen des Anbieters und Zeiger auf die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="a9b0c-113">After it has loaded the provider DLL, the time provider manager calls [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passing the name of the provider and pointers to the following functions:</span></span>

-   [<span data-ttu-id="a9b0c-114">**Alertsamplesavailfunc**</span><span class="sxs-lookup"><span data-stu-id="a9b0c-114">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [<span data-ttu-id="a9b0c-115">**Gettimesysinfofunc**</span><span class="sxs-lookup"><span data-stu-id="a9b0c-115">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [<span data-ttu-id="a9b0c-116">**Logtimeproveventfunc**</span><span class="sxs-lookup"><span data-stu-id="a9b0c-116">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

<span data-ttu-id="a9b0c-117">Diese Funktionen sind für die Verwendung durch den Zeit Anbieter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-117">These functions are for use by the time provider.</span></span> <span data-ttu-id="a9b0c-118">Der Zeit Anbieter verwendet [**timeprovopen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) , um ein Anbieter handle zurückzugeben, das der Zeit Anbieter-Manager beim Senden von Befehlen an den Zeit Anbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-118">The time provider uses [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) to return a provider handle that the time provider manager uses when sending commands to the time provider.</span></span> <span data-ttu-id="a9b0c-119">Der Handle-Wert wird durch den Zeit Anbieter definiert und wird hauptsächlich verwendet, um zwischen verschiedenen Anbietern zu unterscheiden, die in derselben dll implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-119">The handle value is defined by the time provider and is used primarily to distinguish between different providers implemented in the same DLL.</span></span> <span data-ttu-id="a9b0c-120">Der Zeit Anbieter kann mit [**logtimeproveventfunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)bedeutende Ereignisse protokollieren.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-120">The time provider can log significant events using [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span></span>

<span data-ttu-id="a9b0c-121">Der Zeit Anbieter-Manager verwendet [**timeprovcommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) zum Senden von Befehlen an den Zeit Anbieter.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-121">The time provider manager uses [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) to send commands to the time provider.</span></span> <span data-ttu-id="a9b0c-122">Wenn der Zeit Anbieter den Zeit Anbieter-Manager benachrichtigen muss, dass Zeit Beispiele verfügbar sind, wird [**alertsamplesavailfunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-122">When the time provider needs to notify the time provider manager that it has time samples available, it calls [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span></span> <span data-ttu-id="a9b0c-123">Der Zeit Anbieter-Manager ruft dann **timeprovcommand** mit dem TPC \_ getSamples-Befehl auf, um die Zeit Beispiele abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-123">The time provider manager then calls **TimeProvCommand** with the TPC\_GetSamples command to retrieve the time samples.</span></span> <span data-ttu-id="a9b0c-124">Es kann bis zu 16 Sekunden dauern, bis der Zeit Anbieter-Manager das Beispiel anfordert.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-124">It can take up to 16 seconds for the time provider manager to request the sample.</span></span> <span data-ttu-id="a9b0c-125">Daher sollte die Anwendung nicht auf die Anforderung warten.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-125">Therefore, the application should not wait for the request.</span></span>

<span data-ttu-id="a9b0c-126">Um die Genauigkeit zu gewährleisten, sollte der Zeit Anbieter alle zeitbezogenen Informationen mithilfe von [**gettimesysinfofunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)abrufen.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-126">To ensure accuracy, the time provider should retrieve all time-related information using [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span></span>

<span data-ttu-id="a9b0c-127">Wenn der Zeit Anbieter heruntergefahren werden soll, ruft der Zeit Anbieter-Manager [**timeprovclose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)auf.</span><span class="sxs-lookup"><span data-stu-id="a9b0c-127">When it is time to shut down the time provider, the time provider manager calls [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span></span>

 

 



