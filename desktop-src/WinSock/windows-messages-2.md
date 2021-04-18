---
description: In Windows Sockets 1,1 wurde der Async-Select-Mechanismus eingeführt, um Netzwerk Ereignis Hinweise bereitzustellen, für die weder Abruf noch Blockierung aufgetreten ist.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Windows-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368167"
---
# <a name="windows-messages"></a><span data-ttu-id="b0ea3-103">Windows-Meldungen</span><span class="sxs-lookup"><span data-stu-id="b0ea3-103">Windows Messages</span></span>

<span data-ttu-id="b0ea3-104">In Windows Sockets 1,1 wurde der Async-Select-Mechanismus eingeführt, um Netzwerk Ereignis Hinweise bereitzustellen, für die weder Abruf noch Blockierung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b0ea3-104">Windows Sockets 1.1 introduced the async-select mechanism to provide network event indications that did not involve either polling or blocking.</span></span> <span data-ttu-id="b0ea3-105">Die [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) -Funktion wird verwendet, um ein Interesse an einem oder mehreren Netzwerk Ereignissen zu registrieren, wie im vorherigen Abschnitt aufgeführt, und stellt ein Fenster Handle bereit, das für die Benachrichtigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0ea3-105">The [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) function is used to register an interest in one or more network events as listed in the preceding, and supply a window handle to be used for notification.</span></span> <span data-ttu-id="b0ea3-106">Wenn ein gedesigniertes Netzwerk Ereignis auftritt, wird eine vom Client angegebene Windows-Meldung an das angegebene Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="b0ea3-106">When a nominated network event occurs, a client-specified Windows message is sent to the indicated window.</span></span> <span data-ttu-id="b0ea3-107">Der Dienstanbieter muss die [**wpupostmessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) -Funktion verwenden, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="b0ea3-107">The service provider must use the [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) function to accomplish this.</span></span>

<span data-ttu-id="b0ea3-108">In Windows ist dies möglicherweise nicht der effizienteste Benachrichtigungs Mechanismus und für Daemons und Dienste, die keine Fenster öffnen möchten, unpraktisch.</span><span class="sxs-lookup"><span data-stu-id="b0ea3-108">In Windows, this may not be the most efficient notification mechanism, and is inconvenient for daemons and services that do not want to open any windows.</span></span> <span data-ttu-id="b0ea3-109">Das in den folgenden beschriebenen Verfahren zum Signalisieren von Ereignis Objekten wird eingeführt, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="b0ea3-109">The event object signaling mechanism described in the following is introduced to solve this problem.</span></span>

 

 
