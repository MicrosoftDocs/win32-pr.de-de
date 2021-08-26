---
title: Setup der RAS-Administration-DLL-Registrierung
description: Hier finden Sie Informationen zu den Anforderungen für die Registrierung einer RAS-Verwaltungs-DLL (Remote Access Service) eines Drittanbieters mit RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e40ed8fe4fe853c12e33e6168cb72cf1b3ec5b33afc92e8767731a13ec37412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036364"
---
# <a name="ras-administration-dll-registry-setup"></a>Setup der RAS-Administration-DLL-Registrierung

Das Setupprogramm für eine RAS-Verwaltungs-DLL eines Drittanbieters muss die DLL mit RAS registrieren, indem informationen unter dem folgenden Schlüssel in der Registrierung zur Verfügung stellen.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Legen Sie die folgenden Werte unter diesem Schlüssel fest, um die DLL zu registrieren.



| Wertname    | Wertdaten                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Eine **REG \_ SZ-Zeichenfolge,** die den benutzerfreundlichen Anzeigenamen der DLL enthält. |
| *DLLPath*     | Eine **REG \_ SZ-Zeichenfolge,** die den vollständigen Pfad der DLL enthält.                  |



 

Der Registrierungseintrag für eine RAS-Verwaltungs-DLL eines fiktiven Unternehmens mit dem Namen ProElectron, Inc. könnte beispielsweise wie im folgenden Beispiel sein:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **REG \_ SZ** : ProElecweiter RAS-Administrator-DLL

*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

Das Setupprogramm für eine RAS-Verwaltungs-DLL sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen. Wenn ein Benutzer die DLL entfernt, sollte das Setupprogramm die Registrierungseinträge der DLL löschen.

 

 




