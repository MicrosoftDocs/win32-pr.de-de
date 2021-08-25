---
description: Alle Funktionen, Prototypen, Strukturen und Konstanten werden in der Headerdatei Winwlx.h definiert.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Erstellen und Testen einer GINA-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31df8597ca9ad78b8c94efb5610e3c899f7834cb14c9112b15a410c72705a0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883530"
---
# <a name="building-and-testing-a-gina-dll"></a>Erstellen und Testen einer GINA-DLL

Alle Funktionen, Prototypen, Strukturen und Konstanten werden in der Headerdatei Winwlx.h definiert.

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Verwenden Sie zum Testen einer [*GINA-DLL*](/windows/desktop/SecGloss/g-gly) die Winlogon.exe einer überprüften Version des Betriebssystems, die mit dem Microsoft Windows Driver Development Kit (DDK) verfügbar ist. Die überprüfte Version von [*Winlogon unterstützt*](/windows/desktop/SecGloss/w-gly) das Debuggen von DEBUGGENAs wie folgt:

-   Sie können die folgende Syntax verwenden, um einen Abschnitt in Win.ini, um Winlogon-Debugoptionen anzugeben.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Falls angegeben, **sollte LogFile** den vollqualifizierten Namen der Datei enthalten, die zum Protokollieren von Debuginformationen verwendet wird. Wenn die Datei nicht vorhanden ist, wird sie erstellt.

    Die **DebugFlags-Optionen** geben an, welche Arten von Debuginformationen in die Protokolldatei oder den Debugger geschrieben werden. **DebugFlags** können eines oder mehrere der folgenden Flags enthalten.

    

    | Debugflag | Beschreibung                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | Die Tastenkombination STRG+ALT+UMSCHALT+TAB verursacht einen Debug-Break in Winlogon.                                                                                               |
    | Fehler          | Druckfehler.                                                                                                                                                              |
    | Init           | Drucken von Initialisierungs- und Statusmeldungen.                                                                                                                                |
    | Benachrichtigen         | Drucken von Benachrichtigungspaketmeldungen.                                                                                                                                       |
    | SAS            | Geben Sie Informationen zu [*SAS-Benachrichtigungen (Secure Attention Sequence)*](/windows/desktop/SecGloss/s-gly) aus. |
    | State          | Druckt Meldungen, wenn winlogon den Zustand ändert.                                                                                                                                |
    | Timeout        | Druckt Meldungen, wenn ein Zeitlimit festgelegt oder ein Zeitlimit erreicht wird.                                                                                                        |
    | Trace          | Geben Sie ausführliche Ablaufverfolgungsinformationen aus.                                                                                                                                           |
    | Warnung           | Druckwarnungen.                                                                                                                                                            |

    

     

-   Um die überprüfte Version von Winlogon in einem Debugger zu starten, fügen Sie der Registrierung den folgenden Eintrag hinzu:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> Sie müssen den symbolischen Windows (NTSD) verwenden, um winlogon zu debuggen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden und Ausführen einer GINA-DLL](loading-and-running-a-gina-dll.md)
</dt> <dt>

[GINA-Exportfunktionen](authentication-functions.md)
</dt> <dt>

[GINA-Strukturen](authentication-structures.md)
</dt> <dt>

[GINA-Funktionen für Terminaldienste](terminal-services-gina-functions.md)
</dt> </dl>

 

 
