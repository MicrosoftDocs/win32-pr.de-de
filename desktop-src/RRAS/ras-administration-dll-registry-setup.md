---
title: Informationen zur Registrierungs Einrichtung der RAS-Verwaltung
description: Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem Sie Informationen unter dem folgenden Schlüssel in der Registrierung bereitstellt.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS-Administration-RRAS, Einrichten der DLL-Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857827"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Informationen zur Registrierungs Einrichtung der RAS-Verwaltung

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



 

Da RAS mehrere RAS-Verwaltungs-DLLs unterstützt, kann der Registrierungs Wert **DllPath** eine durch Semikolons getrennte Liste von Pfaden enthalten. Beispielsweise könnte der Registrierungs Eintrag für eine RAS-Verwaltungs-dll von einem fiktiven Unternehmen mit dem Namen ProElectron, Inc. wie folgt lauten:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*Display Name*: **reg \_ SZ** : ProElectron RAS admin dll

*DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll

RAS Ruft die DLLs in der Reihenfolge auf, in der Sie in diesem Registrierungs Wert aufgelistet sind. Der Registrierungs Wert *Display Name* enthält immer noch nur einen einzigen anzeigen Amen.

Das Setup Programm für eine RAS-Verwaltungs-dll muss ebenfalls die Funktionen zum Entfernen und deinstallieren bereitstellen. Wenn ein Benutzer die dll entfernt, muss das Setup Programm die Registrierungseinträge für die dll löschen.

**Windows 2000/NT:** RAS unterstützt nur eine RAS-Verwaltungs-dll, sodass der Registrierungs Wert ' **DllPath** ' keine durch Semikolons getrennte Liste von Pfaden enthalten darf.

 

 




