---
description: 'Verwenden Sie die Richtlinien in der folgenden Liste, um eine Anwendung pro Benutzer-Installation anzukündigen, wenn die Anwendung erhöhte Rechte (d. h. Systemrechte) für die Installation erfordert:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347961"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a><span data-ttu-id="83218-103">Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll</span><span class="sxs-lookup"><span data-stu-id="83218-103">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>

<span data-ttu-id="83218-104">Verwenden Sie die Richtlinien in der folgenden Liste, um eine Anwendung pro Benutzer-Installation anzukündigen, wenn die Anwendung erhöhte Rechte (d. h. Systemrechte) für die Installation erfordert:</span><span class="sxs-lookup"><span data-stu-id="83218-104">To advertise an application on a per-user installation basis when the application requires elevated (that is, system) privileges for installation, use the guidelines in the following list:</span></span>

-   <span data-ttu-id="83218-105">Dabei muss es sich um einen Dienst handeln, der unter dem Systemkonto "LocalSystem" unter Windows XP oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83218-105">Your process must be a service that runs under the LocalSystem system account on Windows XP or later.</span></span>
-   <span data-ttu-id="83218-106">Generieren Sie ein Ankündigungs Skript, indem Sie [**msiankünderproduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) oder [**msiankünabproductex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="83218-106">Generate an advertise script by calling [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) or [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span></span>
-   <span data-ttu-id="83218-107">Ihr Prozess muss die Identität des Benutzers annehmen, der das Ziel für die Ankündigung ist.</span><span class="sxs-lookup"><span data-stu-id="83218-107">Your process must impersonate the user that is the target for the advertisement.</span></span>
-   <span data-ttu-id="83218-108">Rufen Sie [**msiappsescript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)auf, und verwenden Sie die Flags scriptflags \_ Cacheinfo \| scriptflags \_ regdata \_ appinfo \| scriptflags \_ regdata \_ cnfginfo \| scriptflags \_ -Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="83218-108">Call [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta), and use the flags SCRIPTFLAGS\_CACHEINFO \| SCRIPTFLAGS\_REGDATA\_APPINFO \| SCRIPTFLAGS\_REGDATA\_CNFGINFO \| SCRIPTFLAGS\_SHORTCUTS.</span></span>

<span data-ttu-id="83218-109">Wenn Sie den Richtlinien folgen, wird eine Anwendung für einen angegebenen Benutzer angekündigt, und wenn der Benutzer sich für die Installation entscheidet, wird die Anwendung mit erhöhten Rechten installiert.</span><span class="sxs-lookup"><span data-stu-id="83218-109">When you follow the guidelines, you advertise an application to a specified user, and when the user chooses to install, the application is installed with elevated privileges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83218-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83218-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83218-111">Patchen von verwalteten Anwendungen pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="83218-111">Patching Per-User Managed Applications</span></span>](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



