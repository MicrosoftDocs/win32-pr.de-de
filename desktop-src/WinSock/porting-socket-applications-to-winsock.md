---
description: In diesem Abschnitt werden die Aspekte der Winsock-Portierung beschrieben.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portieren von Socketanwendungen auf Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356753"
---
# <a name="porting-socket-applications-to-winsock"></a>Portieren von Socketanwendungen auf Winsock

In diesem Abschnitt werden die Aspekte der Winsock-Portierung beschrieben.

Es gibt eine begrenzte Anzahl von Instanzen, bei denen Windows Sockets von der strikten Einhaltung der Berkeley-Konventionen umgeleitet wurde, in der Regel aufgrund von Implementierungs Problemen in der Microsoft Windows-Umgebung.

Wenn eine Abweichung von Berkeley-Konventionen in Windows Sockets auftritt, wird die Abweichung ausdrücklich und eindeutig vermerkt. Wenn eine Funktion z. b. für Windows Sockets spezifisch ist, wird diese Abweichung mit einem Ausdruck in der Funktionsbeschreibung wie folgt angegeben:

Die **\[ Funktion "Function \] -Name** " ist eine Microsoft-spezifische Erweiterung der Windows Sockets 2-API.

Dieser Abschnitt enthält Informationen zum Portieren von UNIX-Socketanwendungen (BSD) in Winsock:

-   [Socket-Datentyp](socket-data-type-2.md)
-   [Makros für Auswahl, FD \_ -Satz und FD \_ xxx](select-and-fd---2.md)
-   [Fehler Codes: errno, h \_ errno und WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [Zeiger](pointers-2.md)
-   [Umbenannte Funktionen](renamed-functions-2.md)
-   [Maximale Anzahl unterstützter Sockets](maximum-number-of-sockets-supported-2.md)
-   [Includedateien](include-files-2.md)
-   [Rückgabewerte bei Funktions Fehlern](return-values-on-function-failure-2.md)
-   [Rohdaten Sockets](service-provided-raw-sockets-2.md)
-   [Byte Reihenfolge](byte-ordering-2.md)
-   [Erweiterte Byte-Order Konvertierungs Routinen](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Behandeln von Winsock-Fehlern](handling-winsock-errors.md)
</dt> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Sockets-Fehler Codes](windows-sockets-error-codes-2.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 



