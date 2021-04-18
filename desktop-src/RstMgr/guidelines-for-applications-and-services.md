---
title: Richtlinien für Anwendungen und Dienste
description: Zum Reduzieren der Anzahl der Systemneustarts bei der Installation und Wartung von Anwendungen unter Windows Vista oder Windows Server 2008 sollten Sie die folgenden Richtlinien beachten, damit Ihre Anwendung oder Ihr Dienst ordnungsgemäß heruntergefahren und neu gestartet werden kann.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341642"
---
# <a name="guidelines-for-applications-and-services"></a><span data-ttu-id="c2ee5-103">Richtlinien für Anwendungen und Dienste</span><span class="sxs-lookup"><span data-stu-id="c2ee5-103">Guidelines for Applications and Services</span></span>

<span data-ttu-id="c2ee5-104">Zum Reduzieren der Anzahl der Systemneustarts bei der Installation und Wartung von Anwendungen unter Windows Vista oder Windows Server 2008 sollten Sie die folgenden Richtlinien beachten, damit Ihre Anwendung oder Ihr Dienst ordnungsgemäß heruntergefahren und neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2ee5-104">To reduce the number of system restarts when installing and servicing applications on Windows Vista or Windows Server 2008, you should observe the following guidelines to enable your application or service to be shut down cleanly and restarted.</span></span>

-   <span data-ttu-id="c2ee5-105">Ihre Anwendungen und Dienste sollten so vorbereitet werden, dass Sie vom System heruntergefahren und neu gestartet werden, wenn dies für die Installation eines Updates erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c2ee5-105">Your applications and services should be prepared to be shut down and restarted by the system when this is necessary to install an update.</span></span> <span data-ttu-id="c2ee5-106">Wenn ein Update installiert wird, muss in der Regel eine Anwendung oder ein Dienst heruntergefahren werden, da zurzeit eine betroffene Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2ee5-106">Typically, when an update is installed, an application or service needs to be shut down because it currently holds an affected file in use.</span></span> <span data-ttu-id="c2ee5-107">Alle Anwendungen oder Dienste, die eine Datei enthalten können, die während eines Updates verwendet wird, sollten ordnungsgemäß heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="c2ee5-107">All applications or services that can hold a file in use during an update should be prepared to shut down cleanly.</span></span>
-   <span data-ttu-id="c2ee5-108">Ihre Anwendungen sollten Benutzerdaten und Zustandsinformationen speichern, die nach einem Neustart benötigt werden, und die Richtlinien befolgen, die im Abschnitt [Richtlinien für Anwendungen](guidelines-for-applications.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c2ee5-108">Your applications should save user data and state information that are needed after a restart and should adhere to the guidelines that are described in the section [Guidelines for Applications](guidelines-for-applications.md).</span></span>
-   <span data-ttu-id="c2ee5-109">Ihre Dienste sollten den Richtlinien entsprechen, die im Abschnitt [Richtlinien für Dienste](guidelines-for-services.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c2ee5-109">Your services should adhere to the guidelines that are described in the section [Guidelines for Services](guidelines-for-services.md).</span></span>
-   <span data-ttu-id="c2ee5-110">Mit dem Neustart-Manager werden [wichtige Systemdienste](critical-system-services.md)nicht heruntergefahren. Daher sollten diese Dienste die Anzahl der DLLs begrenzen, von denen Sie abhängen.</span><span class="sxs-lookup"><span data-stu-id="c2ee5-110">Restart Manager does not shut down [critical system services](critical-system-services.md); therefore, these services should limit the number of DLLs they depend on.</span></span>

 

 




