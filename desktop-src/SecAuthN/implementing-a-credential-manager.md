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
# <a name="implementing-a-credential-manager"></a>Implementieren eines Credential-Managers

Zum Erstellen eines Anmelde Informationen-Managers müssen Sie eine DLL erstellen, die die folgenden Funktionen exportiert:

-   [**Nplogonnotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**Nppasswordchangenotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Erstellen Sie einen Registrierungs Eintrag mit dem Namen **smartcardlogonnotify** als **DWORD**, und legen Sie ihn auf 1 fest, um Benachrichtigungen zu den Funktionen [**nplogonnotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) und [**nppasswordchangenotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) für die Smartcard-Anmeldung wiederherzustellen.

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

**Windows Server 2003 und Windows XP:** Der Registrierungs Eintrag " **smartcardlogonnotify** " ist nicht erforderlich.

Außerdem sollten Anmelde Informationen-Manager auch die [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) -Funktion für den wnnc-Start unterstützen \_ (die Unterstützung anderer Indizes ist für Anmelde Informations Verwalter nicht erforderlich). Dies weist MPR an, wenn ein Anmelde Informationen-Manager gestartet wird. Durch Aufrufen von **NPgetCaps** , bei dem der *nIndex* -Parameter auf wnnc Start festgelegt \_ ist, erhält die MPR die Zeit, die gewartet wird, bevor die Einstiegspunkt Funktionen der Anmelde Informationsverwaltung des Anbieters aufgerufen werden. Wenn die MPR über diese Informationen verfügt, kann Sie an die Anmelde Informationsverwaltung weiterleiten und das Timeout festlegen.

 

 



