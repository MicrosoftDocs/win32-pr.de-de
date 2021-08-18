---
description: Listet die DLL-Exporte auf, die implementiert werden müssen, um einen Anmeldeinformations-Manager zu erstellen.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementieren eines Anmeldeinformationsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a1787fcf72d88ad809f904f9f83179ac86631b83a23314f9d24ee31ce3dec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482660"
---
# <a name="implementing-a-credential-manager"></a>Implementieren eines Anmeldeinformationsverwaltung

Um einen Anmeldeinformations-Manager zu erstellen, müssen Sie eine DLL erstellen, die die folgenden Funktionen exportiert:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Um Benachrichtigungen für die [**Funktionen NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) und [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) für die Smartcardanmeldung wiederherzustellen, erstellen Sie einen Registrierungseintrag namens **SmartCardLogonNotify** als **DWORD,** und legen Sie ihn auf 1 fest:

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

**Windows Server 2003 und Windows XP:** Der **Registrierungseintrag SmartCardLogonNotify** ist nicht erforderlich.

Darüber hinaus sollten Anmeldeinformations-Manager auch die [**NPGetCaps-Funktion**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) für WNNC START unterstützen (die Unterstützung anderer Indizes ist für \_ Anmeldeinformations-Manager nicht erforderlich). Dadurch wird MPR informiert, wann ein Anmeldeinformations-Manager gestartet wird. Durch Aufrufen **von NPGetCaps,** bei dem der *nIndex-Parameter* auf WNNC START festgelegt ist, erhält das MPR die Wartezeit, bevor die Einstiegspunktfunktionen für die Verwaltung von Anmeldeinformationen des Anbieters \_ aufrufen. Wenn der MPR über diese Informationen verfügt, kann er diese an den Anmeldeinformations-Manager weitersend und das Time out festlegen.

 

 



