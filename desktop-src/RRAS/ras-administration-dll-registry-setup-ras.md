---
title: Setup der RAS-Verwaltungs-DLL-Registrierung
description: Machen Sie sich mit den Anforderungen für die Registrierung einer RAS-Verwaltungs-DLL (Remote Access Service) eines Drittanbieters bei RAS bewusst.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406713"
---
# <a name="ras-administration-dll-registry-setup"></a>Setup der RAS-Verwaltungs-DLL-Registrierung

Das Setupprogramm für eine RAS-Verwaltungs-DLL eines Drittanbieters muss die DLL bei RAS registrieren, indem Informationen unter dem folgenden Schlüssel in der Registrierung zur Verfügung gestellt werden.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Legen Sie zum Registrieren der DLL die folgenden Werte unter diesem Schlüssel fest.



| Wertname    | Wertdaten                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Eine **REG \_ SZ-Zeichenfolge,** die den benutzerfreundlichen Anzeigenamen der DLL enthält. |
| *DLLPath*     | Eine **REG \_ SZ-Zeichenfolge,** die den vollständigen Pfad der DLL enthält.                  |



 

Der Registrierungseintrag für eine RAS-Verwaltungs-DLL eines fiktiven Unternehmens mit dem Namen ProElecron, Inc. kann beispielsweise wie im Folgenden beschrieben sein:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **REG \_ SZ** : ProElecron RAS Admin DLL

*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll

Das Setupprogramm für eine RAS-Verwaltungs-DLL sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen. Wenn ein Benutzer die DLL entfernt, sollte das Setupprogramm die Registrierungseinträge der DLL löschen.

 

 




