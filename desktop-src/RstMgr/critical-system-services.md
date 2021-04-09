---
title: Wichtige System Dienste
description: Kritische Systemdienste können vom Neustart-Manager ohne Systemneustart nicht beendet und neu gestartet werden. Updates an Dateien oder Ressourcen, die von einem dieser Dienste verwendet werden, erfordern einen Systemneustart.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037655"
---
# <a name="critical-system-services"></a><span data-ttu-id="7a8e0-104">Wichtige System Dienste</span><span class="sxs-lookup"><span data-stu-id="7a8e0-104">Critical System Services</span></span>

<span data-ttu-id="7a8e0-105">Kritische Systemdienste können vom Neustart-Manager ohne Systemneustart nicht beendet und neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-105">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="7a8e0-106">Updates an Dateien oder Ressourcen, die von einem dieser Dienste verwendet werden, erfordern einen Systemneustart.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-106">Updates to any file or resource in use by one of these services requires a system restart.</span></span>

<span data-ttu-id="7a8e0-107">**, Um zu bestimmen, ob ein Prozess ein kritischer Systemdienst ist.**</span><span class="sxs-lookup"><span data-stu-id="7a8e0-107">**To determine whether a process is a critical system service.**</span></span>

1.  <span data-ttu-id="7a8e0-108">Registrieren Sie den Prozess mit der [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-108">Register the process using the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function.</span></span>
2.  <span data-ttu-id="7a8e0-109">Aufrufen der [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion zum Abrufen der [**RM- \_ Prozess \_ Informations**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) Struktur.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-109">Call the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to get the [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure.</span></span>
3.  <span data-ttu-id="7a8e0-110">Der **applicationtype** -Member der zurückgegebenen [**RM- \_ Prozess \_ Informations**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) Struktur enthält den Enumerationswert des [**RM-APP- \_ \_ Typs**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) .</span><span class="sxs-lookup"><span data-stu-id="7a8e0-110">The **ApplicationType** member of the returned [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure contains a [**RM\_APP\_TYPE**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) enumeration value.</span></span> <span data-ttu-id="7a8e0-111">Dieser Wert wird für einen kritischen System Prozess auf **rmcriticial** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-111">This value is set to **RmCriticial** for a critical system process.</span></span>

<span data-ttu-id="7a8e0-112">Wichtige Systemdienste sind smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe mit RPCSS und svchost.exe mit DCOM/PNP.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-112">Critical system services include smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe with RPCSS, and svchost.exe with Dcom/PnP.</span></span>

 

 




