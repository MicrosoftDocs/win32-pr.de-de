---
title: Registrierungs Einrichtung der RAS-Verwaltungs-dll
description: Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem Sie Informationen unter dem folgenden Schlüssel in der Registrierung bereitstellt.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516023"
---
# <a name="ras-administration-dll-registry-setup"></a>Registrierungs Einrichtung der RAS-Verwaltungs-dll

Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem Sie Informationen unter dem folgenden Schlüssel in der Registrierung bereitstellt.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Um die dll zu registrieren, legen Sie die folgenden Werte unter diesem Schlüssel fest.



| Wertname    | Wertdaten                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Eine **reg \_ SZ** -Zeichenfolge, die den benutzerfreundlichen anzeigen amen der dll enthält. |
| *Dll*     | Eine **reg- \_ SZ** -Zeichenfolge, die den vollständigen Pfad der dll enthält.                  |



 

Beispielsweise könnte der Registrierungs Eintrag für eine RAS-Verwaltungs-dll von einem fiktiven Unternehmen mit dem Namen ProElectron, Inc. wie folgt lauten:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*Display Name* : **reg \_ SZ** : ProElectron RAS admin dll

*DllPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll

Das Setup Programm für eine RAS-Verwaltungs-dll sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen. Wenn ein Benutzer die dll entfernt, sollte das Setup Programm die Registrierungseinträge der dll löschen.

 

 




