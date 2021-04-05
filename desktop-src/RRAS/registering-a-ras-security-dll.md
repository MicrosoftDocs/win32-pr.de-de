---
title: Registrieren einer RAS-Sicherheits-dll
description: Das Setup Programm für eine RAS-Sicherheits-DLL muss die dll beim Windows NT/Windows 2000-RAS-Server registrieren.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709858"
---
# <a name="registering-a-ras-security-dll"></a>Registrieren einer RAS-Sicherheits-dll

Das Setup Programm für eine RAS-Sicherheits-DLL muss die dll beim Windows NT/Windows 2000-RAS-Server registrieren. Es kann nur eine RAS-Sicherheits-DLL registriert werden, da keine Unterstützung für mehrere sicherheitsdlls bereitgestellt wird. Legen Sie zum Registrieren einer RAS-Sicherheits-DLL den *DllPath* -Wert unter dem folgenden Schlüssel in der Registrierung fest:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Wertname | Wertdaten                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Dll*  | Eine **reg \_ SZ** -Zeichenfolge, die den Pfad der dll enthält. Diese Zeichenfolge sollte den vollständigen Pfad angeben, sofern sich die dll nicht in einem Verzeichnis befindet, das im Systempfad aufgeführt ist. |



 

Das Setup Programm für eine RAS-Sicherheits-DLL muss auch die Funktion zum Entfernen/Deinstallieren bereitstellen. Wenn ein Benutzer die dll entfernt, muss das Setup Programm den *DllPath* -Wert aus der Registrierung löschen. Der RAS-Dienst wird nicht gestartet, wenn der *DllPath* -Wert eine DLL angibt, die nicht gefunden werden kann.

Eine RAS-Sicherheits-DLL muss die Funktionen " [**rassecuritydialogbegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) " und " [**rassecuritydialogend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) " exportieren.

 

 




