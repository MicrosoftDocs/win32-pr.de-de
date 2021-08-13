---
title: Registrierungsumleitung
description: Der Registrierungsumleitung isoliert 32-Bit- und 64-Bit-Anwendungen, indem separate logische Ansichten bestimmter Teile der Registrierung auf WOW64 zur Verfügung stellen.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- 64-Bit-Windows 64-Bit-Programmierhandbuch Windows Programmierung, Registrierungsumleitung
- 64-Bit-Registrierungsumleitung Windows Programmierung
- Umleitung von 64-Bit-Windows Programmierung
- WOW64 64-Bit-Windows Programmierung, Registrierungsumleitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac810a6ce2dba049f7b7e5b9d28386cda89712f2833eb7bf4f7892df59b34ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561506"
---
# <a name="registry-redirector"></a>Registrierungsumleitung

Der Registrierungsumleitung isoliert 32-Bit- und 64-Bit-Anwendungen, indem separate logische Ansichten bestimmter Teile der Registrierung auf WOW64 zur Verfügung stellen. Der Registrierungsumleitungs-Editor fängt 32-Bit- und 64-Bit-Registrierungsaufrufe an die entsprechenden logischen Registrierungsansichten ab und ordnet sie dem entsprechenden physischen Registrierungsspeicherort zu. Der Umleitungsprozess ist für die Anwendung transparent. Aus diesem Grund kann eine 32-Bit-Anwendung auf Registrierungsdaten zugreifen, als würde sie auf 32-Bit-Windows ausgeführt, auch wenn die Daten an einem anderen Speicherort auf 64-Bit-Windows.

**Windows 10 auf ARM:** Zusätzlich zur logischen 32-Bit-Ansicht für x86-Anwendungen enthält Windows 10 auf ARM eine separate logische Ansicht für 32-Bit-ARM-Anwendungen.

Eine Teilmenge der Schlüssel unter umgeleiteten Registrierungspfaden wird freigegeben. 32-Bit-Registrierungsaufrufe an freigegebene Schlüssel werden nicht umgeleitet. Stattdessen wird jeder logischen Ansicht der Registrierung eine physische Kopie des Schlüssels zugeordnet. Eine Liste der umgeleiteten Schlüssel und freigegebenen Schlüssel finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind.](shared-registry-keys.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Um die Anwendungsinteroperabilität über COM und andere Mechanismen zu ermöglichen, wird auch eine Teilmenge der umgeleiteten Registrierungsschlüssel *widergespiegelt.* Der Prozess der Registrierungslektion kopiert Registrierungsschlüssel und -werte zwischen zwei Registrierungssichten, um sie synchron zu halten. Die Registrierungslektion wurde ab Windows 7 und Windows Server 2008 R2 entfernt. Weitere Informationen finden Sie unter [Registry Reflection](registry-reflection.md).

Das folgende Szenario veranschaulicht die Verwendung dieser logischen Sichten:

-   Eine 32-Bit-x86-Anwendung überprüft, ob der folgende Registrierungsschlüssel vorhanden ist: **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Hello**. Wenn der Schlüssel nicht vorhanden ist, erstellt die Anwendung ihn mit dem Standardwert "Hello 32-bit x86 world"; Andernfalls wird der Wert gelesen und angezeigt.
-   Dieselbe Anwendung wird geändert, um "Hello 64-Bit World" anstelle von "Hello 32-Bit x86 World" zu schreiben und als 64-Bit-x64- oder ARM64-Anwendung neu zu kompilieren.
-   **Windows 10 auf ARM:** Dieselbe Anwendung wird so geändert, dass sie "Hello 32-Bit ARM world" schreibt und als 32-Bit-ARM-Anwendung neu kompiliert wird.
-   Wenn die 32-Bit-x86-Anwendung auf 64-Bit-Windows ausgeführt wird, wird "Hello 32-Bit x86 world" angezeigt. Wenn die 64-Bit-Anwendung ausgeführt wird, wird "Hello 64-Bit World" angezeigt. **Windows 10 auf ARM:** Wenn die 32-Bit-ARM-Anwendung auf 64-Bit-ARM64-Windows ausgeführt wird, wird "Hello 32-Bit ARM world" angezeigt. Alle Anwendungen rufen dieselben Registrierungsfunktionen mit dem gleichen vordefinierten Handle und demselben Schlüsselnamen auf. Der Unterschied besteht in dem, dass jede Anwendung ihre logische Ansicht der Registrierung verwendet und jede Ansicht einem separaten physischen Speicherort der Registrierung zugeordnet ist, wodurch alle Versionen der Zeichenfolge intakt bleiben.

Umgeleitete Schlüssel werden physischen Speicherorten unter **Wow6432Node zugeordnet.** Beispielsweise wird **HKEY \_ LOCAL MACHINE \_ \\ Software** an **HKEY LOCAL MACHINE Software \_ \_ \\ \\ Wow6432Node umgeleitet.** Der physische Speicherort der umgeleiteten Schlüssel sollte jedoch vom System als reserviert angesehen werden. Anwendungen sollten nicht direkt auf den physischen Speicherort eines Schlüssels zugreifen, da sich dieser Speicherort ändern kann. Weitere Informationen finden Sie unter [Zugreifen auf eine alternative Registrierungssicht.](accessing-an-alternate-registry-view.md)

**Windows 10 auf ARM:** Umgeleitete 32-Bit-ARM-Schlüssel werden physischen Speicherorten unter WowAA32Node zugeordnet.

Um 32-Bit-Anwendungen zu unterstützen, die **REG \_ SZ-** oder **REG EXPAND \_ \_ SZ-Daten** mit %ProgramFiles% oder %commonprogramfiles% in die Registrierung schreiben, fängt WOW64 diese Schreibvorgänge ab und ersetzt sie durch "%ProgramFiles(x86)%" und "%commonprogramfiles(x86)%". Wenn sich das Verzeichnis Programme beispielsweise auf dem Laufwerk C befindet, wird "%ProgramFiles(x86)%" zu "C: \\ Programme (x86)" erweitert. Die Ersetzung erfolgt nur, wenn die folgenden Bedingungen erfüllt sind:

-   Die Zeichenfolge muss mit %ProgramFiles% oder %commonprogramfiles% beginnen. Wenn die Zeichenfolge mit einem Leerzeichen oder einem anderen Zeichen als %beginnt, wird sie nicht ersetzt.
-   Der Fall von %ProgramFiles% oder %commonprogramfiles% muss genau wie gezeigt sein, da beim Zeichenfolgenvergleich die Schreibung beachtet wird. Wenn die Zeichenfolge beispielsweise mit %CommonProgramFiles% anstelle von %commonprogramfiles% beginnt, wird sie nicht ersetzt.
-   Die Zeichenfolge darf MAX \_ PATH \* 2+15 Zeichen nicht überschreiten. Wenn sie diese Länge überschreitet, wird sie nicht ersetzt.
-   Der Schlüssel kann nicht mit KEY \_ WOW64 \_ 64KEY geöffnet werden. Dieses Flag gibt an, dass Vorgänge für den Schlüssel für die 64-Bit-Registrierungsansicht ausgeführt werden sollen, sodass er nicht ersetzt wird. Weitere Informationen finden Sie unter [Zugreifen auf eine alternative Registrierungssicht.](accessing-an-alternate-registry-view.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Das KEY \_ WOW \_ 64 64KEY-Flag wirkt sich nicht \_ darauf aus, ob ein Schlüssel ersetzt wird. Dieses Flag wirkt sich auf die Ersetzung ab Windows 7 und Windows Server 2008 R2 aus.

Darüber hinaus werden DIE REG SZ- oder REG EXPAND SZ-Schlüssel, die \_ \_ \_ system32 enthalten, durch syswow64 ersetzt. Die Zeichenfolge muss mit dem Pfad beginnen, der auf oder unter %windir% \\ system32 zeigen soll. Beim Zeichenfolgenvergleich wird die Kleinschreibung nicht beachtet. Umgebungsvariablen werden erweitert, bevor sie mit dem Pfad übereinstimmen, sodass alle folgenden Pfade ersetzt werden: %windir% \\ system32, %SystemRoot% \\ system32 und C: \\ windows \\ system32. Dieser Patch wird nur auf die Schlüssel angewendet, die vor 7 Windows wurden.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Registrierungslektion](registry-reflection.md)
-   [Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md)
-   [Zugreifen auf eine alternative Registrierungsansicht](accessing-an-alternate-registry-view.md)
-   [Beispiel für die Registrierungsumleitung auf WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Remoteregistrierungszugriff in 64-Bit-Windows](remote-registry-access-in-64-bit-windows.md)

 

 




