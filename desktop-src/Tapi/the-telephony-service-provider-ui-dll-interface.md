---
description: In der Microsoft-telefonietelefonie werden Telefoniedienstanbieter in einem separaten Prozess von Telefonieanwendungen ausgeführt.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: UI-Dienstanbieter UI-DLL-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349204"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a><span data-ttu-id="5295c-103">UI-Dienstanbieter UI-DLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5295c-103">The Telephony Service Provider UI DLL Interface</span></span>

<span data-ttu-id="5295c-104">In der Microsoft-telefonietelefonie werden Telefoniedienstanbieter in einem separaten Prozess von Telefonieanwendungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5295c-104">In Microsoft Telephony, telephony service providers execute in a separate process from telephony applications.</span></span> <span data-ttu-id="5295c-105">Dienstanbieter kommunizieren über die Telefonie-Dienstanbieter Schnittstelle (TSPI) mit tapisrv und führen Sie in Ihrem Prozess aus. Anwendungen stellen eine Schnittstelle zu TAPI dar, die im Anwendungskontext geladen werden.</span><span class="sxs-lookup"><span data-stu-id="5295c-105">Service providers communicate with TAPISRV through the Telephony service provider interface (TSPI) and execute in its process; applications interface to TAPI, which are loaded in the application context.</span></span>

<span data-ttu-id="5295c-106">Die Komponenten von TAPI verwenden verschiedene prozessübergreifende Kommunikationsmechanismen, um Funktionsanforderungen und Nachrichten zwischen Anwendungen und Dienstanbietern zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5295c-106">The components of TAPI use various interprocess communications mechanisms to convey function requests and messages between applications and service providers.</span></span> <span data-ttu-id="5295c-107">Die Anwendungen und die Dienstanbieter können nicht nur in separaten Prozessen ausgeführt werden, sondern auf vollständig getrennten Systemen.</span><span class="sxs-lookup"><span data-stu-id="5295c-107">The applications and the service providers may be executing not only in separate processes, but on completely separate systems.</span></span> <span data-ttu-id="5295c-108">Dienstanbieter können daher keine Dialogfelder im Prozess oder sogar auf dem Computer anzeigen, auf dem Sie ausgeführt werden. Auf dem Computer, auf dem die Anwendung ausgeführt wird, muss die Benutzeroberfläche innerhalb des Anwendungs Kontexts aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5295c-108">Service providers therefore cannot display dialog boxes in the process or even on the computer on which they are executing; UI must be invoked from within the application context, on the computer on which the application is executing.</span></span>

<span data-ttu-id="5295c-109">In diesem Abschnitt wird der Mechanismus definiert, mit dem die Benutzeroberflächen Funktionen von Dienstanbietern geladen und innerhalb des Anwendungs Kontexts aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5295c-109">This section defines the mechanism by which service provider UI functions are loaded and invoked within the application context.</span></span> <span data-ttu-id="5295c-110">Außerdem wird ein Mechanismus definiert, durch den Dienstanbieter die Dialogfelder im Anwendungskontext spontan öffnen können, wenn Sie von der Anwendung nicht anderweitig erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="5295c-110">A mechanism is also defined by which service providers can spontaneously open dialog boxes in the application context when they would not otherwise be expected by the application.</span></span> <span data-ttu-id="5295c-111">Ein Beispiel für diesen letzteren Fall wäre das Dialogfeld **Talk/hangup** , das von einem Daten-Modem Dienstanbieter angezeigt wird, wenn das Modem als Einwählprogramm für interaktive Sprachanrufe verwendet wird, und der Benutzer muss aufgefordert werden, das Telefon zu übernehmen und den Dienstanbieter darüber zu informieren, wann er den Modem-OnHook platzieren soll.</span><span class="sxs-lookup"><span data-stu-id="5295c-111">An example of this latter case would be the **Talk/Hangup** dialog box that is displayed by a data modem service provider when the modem is being used as a dialer for interactive voice calls, and the user must be told to pick up the phone and inform the service provider when to place the modem onhook.</span></span>

 

 



