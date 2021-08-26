---
title: Registrieren einer RAS-Sicherheits-DLL
description: Das Setupprogramm für eine RAS-Sicherheits-DLL muss die DLL beim Windows NT/Windows 2000-RAS-Server registrieren.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5ca32aa687649c80917f9a072b9d4cbeb0f1f4e8ba61ce090e7781bb04cdefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028413"
---
# <a name="registering-a-ras-security-dll"></a>Registrieren einer RAS-Sicherheits-DLL

Das Setupprogramm für eine RAS-Sicherheits-DLL muss die DLL beim Windows NT/Windows 2000-RAS-Server registrieren. Es kann nur eine RAS-Sicherheits-DLL registriert werden, da keine Unterstützung für mehrere Sicherheits-DLLs bereitgestellt wird. Um eine RAS-Sicherheits-DLL zu registrieren, legen Sie den *DLLPath-Wert* unter dem folgenden Schlüssel in der Registrierung fest:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Wertname | Wertdaten                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | Eine **REG \_ SZ-Zeichenfolge,** die den Pfad der DLL enthält. Diese Zeichenfolge sollte den vollständigen Pfad angeben, es sei denn, die DLL befindet sich in einem Verzeichnis, das im Systempfad aufgeführt ist. |



 

Das Setupprogramm für eine RAS-Sicherheits-DLL muss auch Funktionen zum Entfernen/Deinstallieren bereitstellen. Wenn ein Benutzer die DLL entfernt, muss das Setupprogramm den *DLLPath-Wert* aus der Registrierung löschen. Der RAS-Dienst wird nicht gestartet, wenn der *DLLPath-Wert* eine DLL angibt, die nicht gefunden werden kann.

Eine RAS-Sicherheits-DLL muss die [**Funktionen RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) und [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) exportieren.

 

 




