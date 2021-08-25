---
title: Informationen zum Setup der RAS-Verwaltungs-DLL-Registrierung
description: Machen Sie sich mit den Anforderungen für die Registrierung einer RAS-Verwaltungs-DLL (Remote Access Service) eines Drittanbieters bei RAS bewusst. RAS unterstützt mehrere RAS-Verwaltungs-DLLs.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS-Administration RRAS , DLL-Registrierungseinrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dbabc7a667455bce2cffbd3d04591076f820efa755c0f512f27130a82fde4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909910"
---
# <a name="about-ras-administration-dll-registry-setup"></a>Informationen zum Setup der RAS-Verwaltungs-DLL-Registrierung

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



 

Da RAS mehrere RAS-Verwaltungs-DLLs unterstützt, kann der Registrierungswert **DLLPath** eine durch Semikolons getrennte Liste von Pfaden enthalten. Der Registrierungseintrag für eine RAS-Verwaltungs-DLL eines fiktiven Unternehmens namens ProElecaku, Inc. kann beispielsweise wie folgt sein:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **REG \_ SZ** : ProElecron RAS Admin DLL

*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll

RAS ruft die DLLs in der Reihenfolge auf, in der sie in diesem Registrierungswert aufgeführt sind. Der Registrierungswert *DisplayName* enthält immer noch nur einen einzigen Anzeigenamen.

Das Setupprogramm für eine RAS-Verwaltungs-DLL muss auch Funktionen zum Entfernen und Deinstallieren bereitstellen. Wenn ein Benutzer die DLL entfernt, muss das Setupprogramm die Registrierungseinträge für die DLL löschen.

**Windows 2000/NT:** RAS unterstützt nur eine RAS-Verwaltungs-DLL, sodass der Registrierungswert **DLLPath** keine durch Semikolons getrennte Liste von Pfaden enthalten kann.

 

 




