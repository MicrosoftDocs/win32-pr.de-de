---
description: Alle Funktionen, Prototypen, Strukturen und Konstanten werden in der Header Datei winwlx. h definiert.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Entwickeln und Testen einer Gina-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352048"
---
# <a name="building-and-testing-a-gina-dll"></a>Entwickeln und Testen einer Gina-dll

Alle Funktionen, Prototypen, Strukturen und Konstanten werden in der Header Datei winwlx. h definiert.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Verwenden Sie zum Testen einer [*Gina*](/windows/desktop/SecGloss/g-gly) -dll den Winlogon.exe aus einer überprüften Version des Betriebssystems, die mit dem Microsoft Windows Driver Development Kit (DDK) verfügbar ist. Die aktivierte Version von [*Winlogon*](/windows/desktop/SecGloss/w-gly) unterstützt das Debuggen von Ginas wie folgt:

-   Sie können die folgende Syntax verwenden, um einen Abschnitt in Win.ini zu erstellen, um Winlogon-Debugoptionen anzugeben.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Wenn angegeben, sollte **logfile** den voll qualifizierten Namen der Datei enthalten, die zum Protokollieren von Debuginformationen verwendet wird. Wenn die Datei nicht vorhanden ist, wird sie erstellt.

    Die **DebugFlags** -Optionen geben an, welche Arten von Debuginformationen in die Protokolldatei oder den Debugger geschrieben werden sollen. Debug- **Flags** können eines oder mehrere der folgenden Flags enthalten.

    

    | Debugflag | BESCHREIBUNG                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Coolswitch     | Die Tastenkombination STRG + ALT + UMSCHALT + TAB bewirkt eine debugpause in Winlogon.                                                                                               |
    | Fehler          | Fehler drucken.                                                                                                                                                              |
    | Init           | Druck Initialisierungs-und Fortschrittsmeldungen.                                                                                                                                |
    | Benachrichtigen         | Meldungen zum Druck Benachrichtigungs Paket.                                                                                                                                       |
    | SAS            | Druckt Informationen über SAS-Benachrichtigungen ( [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) ). |
    | State          | Meldungen drucken, wenn sich der Zustand von Winlogon ändert.                                                                                                                                |
    | Timeout        | Drucken von Nachrichten, wenn ein Zeitlimit festgelegt ist oder ein Zeitlimit erreicht wird.                                                                                                        |
    | Trace          | Ausführliche Ablauf Verfolgungs Informationen drucken.                                                                                                                                           |
    | Warnung           | Druck Warnungen.                                                                                                                                                            |

    

     

-   Fügen Sie den folgenden Eintrag in die Registrierung ein, um die überprüfte Version von Winlogon in einem Debugger zu starten:

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
> Zum Debuggen von Winlogon müssen Sie den symbolischen Debugger (NNS) von Windows verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden und Ausführen einer Gina-dll](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Gina-Export Funktionen](authentication-functions.md)
</dt> <dt>

[Gina-Strukturen](authentication-structures.md)
</dt> <dt>

[Terminal Dienste-Gina-Funktionen](terminal-services-gina-functions.md)
</dt> </dl>

 

 
