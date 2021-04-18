---
description: Updates, für die eine Benutzerinteraktion erforderlich ist, können nicht von Windows Update-Agent (WUA)-Anwendungen installiert werden, wenn die WUA-Anwendungen im Kontext des sekundären Anmelde Diensts ausgeführt werden.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Verwenden von WUA über einen sekundären Anmeldungs Prozess (Ausführen als)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343323"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a><span data-ttu-id="2516e-103">Verwenden von WUA über einen sekundären Anmeldungs Prozess (Ausführen als)</span><span class="sxs-lookup"><span data-stu-id="2516e-103">Using WUA from a Secondary Logon (Run As) Process</span></span>

<span data-ttu-id="2516e-104">Updates, für die eine Benutzerinteraktion erforderlich ist, können nicht von Windows Update-Agent (WUA)-Anwendungen installiert werden, wenn die WUA-Anwendungen im Kontext des sekundären Anmelde Diensts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2516e-104">Updates that require user interaction cannot be installed by Windows Update Agent (WUA) applications if the WUA applications are running in the context of the Secondary Logon service.</span></span>

<span data-ttu-id="2516e-105">Wenn der Prozess, der WUA aufruft, im Kontext des runas-Diensts oder des sekundären Anmelde Diensts ausgeführt wird, tritt beim Versuch, ein Update zu installieren, für das eine Benutzerinteraktion erforderlich ist, **ein Fehler auf \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="2516e-105">If the process that is calling WUA is running in the context of the RunAs service or the Secondary Logon service, an attempt to install an update that requires user interaction fails and returns the **WU\_E\_NO\_INTERACTIVE\_USER** error.</span></span>

<span data-ttu-id="2516e-106">In Microsoft Windows können Sie Programme als Benutzer ausführen, der sich von dem aktuell angemeldeten Benutzer unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="2516e-106">In Microsoft Windows, you can run programs as a user who differs from the user who is currently logged on.</span></span> <span data-ttu-id="2516e-107">Zu diesem Zweck muss der sekundäre Anmeldedienst ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2516e-107">To do this the Secondary Logon service must be running.</span></span>

 

 



