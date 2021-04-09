---
description: Listet die DLL-Exporte auf, die implementiert werden müssen, um einen Anmelde Informationen-Manager zu erstellen.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementieren eines Credential-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867863"
---
# <a name="implementing-a-credential-manager"></a><span data-ttu-id="43ba3-103">Implementieren eines Credential-Managers</span><span class="sxs-lookup"><span data-stu-id="43ba3-103">Implementing a Credential Manager</span></span>

<span data-ttu-id="43ba3-104">Zum Erstellen eines Anmelde Informationen-Managers müssen Sie eine DLL erstellen, die die folgenden Funktionen exportiert:</span><span class="sxs-lookup"><span data-stu-id="43ba3-104">To create a credential manager, you must create a DLL that exports the following functions:</span></span>

-   [<span data-ttu-id="43ba3-105">**Nplogonnotify**</span><span class="sxs-lookup"><span data-stu-id="43ba3-105">**NPLogonNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [<span data-ttu-id="43ba3-106">**Nppasswordchangenotify**</span><span class="sxs-lookup"><span data-stu-id="43ba3-106">**NPPasswordChangeNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

<span data-ttu-id="43ba3-107">Erstellen Sie einen Registrierungs Eintrag mit dem Namen **smartcardlogonnotify** als **DWORD**, und legen Sie ihn auf 1 fest, um Benachrichtigungen zu den Funktionen [**nplogonnotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) und [**nppasswordchangenotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) für die Smartcard-Anmeldung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="43ba3-107">To restore notifications to the [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) functions for smart card logon, create a registry entry called **SmartCardLogonNotify** as a **DWORD**, and set it to 1:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

<span data-ttu-id="43ba3-108">**Windows Server 2003 und Windows XP:** Der Registrierungs Eintrag " **smartcardlogonnotify** " ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="43ba3-108">**Windows Server 2003 and Windows XP:** The **SmartCardLogonNotify** registry entry is not required.</span></span>

<span data-ttu-id="43ba3-109">Außerdem sollten Anmelde Informationen-Manager auch die [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) -Funktion für den wnnc-Start unterstützen \_ (die Unterstützung anderer Indizes ist für Anmelde Informations Verwalter nicht erforderlich).</span><span class="sxs-lookup"><span data-stu-id="43ba3-109">In addition, credential managers should also support the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function for WNNC\_START (supporting other indexes is not required for credential managers).</span></span> <span data-ttu-id="43ba3-110">Dies weist MPR an, wenn ein Anmelde Informationen-Manager gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="43ba3-110">This tells MPR when a credential manager will start.</span></span> <span data-ttu-id="43ba3-111">Durch Aufrufen von **NPgetCaps** , bei dem der *nIndex* -Parameter auf wnnc Start festgelegt \_ ist, erhält die MPR die Zeit, die gewartet wird, bevor die Einstiegspunkt Funktionen der Anmelde Informationsverwaltung des Anbieters aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="43ba3-111">By calling **NPGetCaps** with the *nIndex* parameter set to WNNC\_START, the MPR gets the time to wait before calling the provider's credential management entry point functions.</span></span> <span data-ttu-id="43ba3-112">Wenn die MPR über diese Informationen verfügt, kann Sie an die Anmelde Informationsverwaltung weiterleiten und das Timeout festlegen.</span><span class="sxs-lookup"><span data-stu-id="43ba3-112">And if the MPR has this information, it can forward it to the credential manager, setting the time out.</span></span>

 

 



