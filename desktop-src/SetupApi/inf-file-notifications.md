---
description: Die folgenden Benachrichtigungen werden mit den Funktionen "setupinstallfile", "setupinstallfileex" und "setupinstallfrominlosection" verwendet. Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter Benachrichtigungen.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: INF-Datei Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959859"
---
# <a name="inf-file-notifications"></a><span data-ttu-id="8df0e-104">INF-Datei Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="8df0e-104">INF File Notifications</span></span>

<span data-ttu-id="8df0e-105">Die folgenden Benachrichtigungen werden mit den Funktionen " [**setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)", " [**setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)" und " [**setupinstallfrominlosection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="8df0e-105">The following notifications are used with the [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) functions.</span></span> <span data-ttu-id="8df0e-106">Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter [Benachrichtigungen](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="8df0e-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="8df0e-107">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8df0e-107">Notification</span></span>                                                      | <span data-ttu-id="8df0e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8df0e-108">Description</span></span>                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8df0e-109">**\_spfilenotififileopverzögert**</span><span class="sxs-lookup"><span data-stu-id="8df0e-109">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="8df0e-110">Die Datei wird verwendet, und der aktuelle Vorgang wird verzögert, bis das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8df0e-110">The file is in use, and the current operation is delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="8df0e-111">**spfilenotify nicht übereinstimmende \_**</span><span class="sxs-lookup"><span data-stu-id="8df0e-111">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="8df0e-112">Die Sprache der aktuellen Datei stimmt nicht mit der Systemsprache zusammen.</span><span class="sxs-lookup"><span data-stu-id="8df0e-112">The language of the current file does not match the system language.</span></span>                   |
| [<span data-ttu-id="8df0e-113">**spfilenotify \_ targetexists**</span><span class="sxs-lookup"><span data-stu-id="8df0e-113">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="8df0e-114">Eine Kopie der angegebenen Datei ist bereits auf dem Ziel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8df0e-114">A copy of the specified file already exists on the target.</span></span>                             |
| [<span data-ttu-id="8df0e-115">**spfilenotify \_ targetneuere**</span><span class="sxs-lookup"><span data-stu-id="8df0e-115">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="8df0e-116">Eine neuere Version der angegebenen Datei ist auf dem Ziel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8df0e-116">A newer version of the specified file exists on the target.</span></span>                            |



 

> [!Note]  
> <span data-ttu-id="8df0e-117">Da [**setupinstallfrominlosection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) eine interne Datei Warteschlange erstellt und committet, verwendet Sie auch die [Benachrichtigungen der Datei Warteschlange](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="8df0e-117">Because [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) creates and commits an internal file queue, it also uses the [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 

 



