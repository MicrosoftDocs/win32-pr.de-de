---
title: Registrierungs Redirector
description: Der Registrierungs Redirector isoliert 32-Bit-und 64-Bit-Anwendungen, indem er separate logische Sichten bestimmter Teile der Registrierung auf WOW64 bereitstellt.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Registry Redirector
- Registry Redirector 64-Bit-Windows-Programmierung
- Umleitung 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows-Programmierung, Registry Redirector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c11e68f307aa014adb7cae8415f1baba155678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388405"
---
# <a name="registry-redirector"></a>Registrierungs Redirector

Der Registrierungs Redirector isoliert 32-Bit-und 64-Bit-Anwendungen, indem er separate logische Sichten bestimmter Teile der Registrierung auf WOW64 bereitstellt. Der Registrierungs-Redirector fängt 32-Bit-und 64-Bit-Registrierungs Aufrufe an die entsprechenden logischen Registrierungs Sichten ab und ordnet diese dem entsprechenden physischen Registrierungs Speicherort zu. Der Umleitungs Vorgang ist für die Anwendung transparent. Aus diesem Grund kann eine 32-Bit-Anwendung auf Registrierungsdaten zugreifen, als ob Sie auf 32-Bit-Fenstern ausgeführt würde, auch wenn die Daten an einem anderen Speicherort unter 64-Bit-Windows gespeichert werden.

**Windows 10 auf ARM:** Zusätzlich zur logischen 32-Bit-Ansicht für x86-Anwendungen enthält Windows 10 auf Arm eine separate logische Ansicht für 32-Bit-ARM-Anwendungen.

Eine Teilmenge der Schlüssel unter umgeleiteten Registrierungs Pfaden wird freigegeben. 32-Bit-Registrierungs Aufrufe von freigegebenen Schlüsseln werden nicht umgeleitet. Stattdessen wird jeder logischen Ansicht der Registrierung eine physische Kopie des Schlüssels zugeordnet. Eine Liste der umgeleiteten Schlüssel und der gemeinsam genutzten Schlüssel finden Sie unter [von WOW64 betroffene Registrierungsschlüssel](shared-registry-keys.md).

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Zum Aktivieren der Anwendungs Interoperabilität durch com und andere Mechanismen wird auch eine Teilmenge der umgeleiteten Registrierungsschlüssel *reflektiert*. Der Prozess der Registrierungs Reflektion kopiert Registrierungsschlüssel und-Werte zwischen zwei Registrierungs Sichten, um sie synchron zu halten. Die Registrierungs Reflektion wurde ab Windows 7 und Windows Server 2008 R2 entfernt. Weitere Informationen finden Sie unter [Registry Reflection](registry-reflection.md).

Das folgende Szenario veranschaulicht die Verwendung dieser logischen Sichten:

-   Eine 32-Bit-x86-Anwendung prüft, ob der folgende Registrierungsschlüssel vorhanden ist: **HKEY \_ local \_ Machine \\ Software \\ Hello**. Wenn der Schlüssel nicht vorhanden ist, wird er von der Anwendung mit dem Standardwert "Hello 32-Bit x86 World" erstellt; Andernfalls wird der Wert gelesen und angezeigt.
-   Dieselbe Anwendung wird so geändert, dass Sie "Hello 64-Bit World" anstelle von "Hello 32-Bit x86 World" schreibt und als 64-Bit x64-oder ARM64-Anwendung neu kompiliert wird.
-   **Windows 10 auf ARM:** Dieselbe Anwendung wird so geändert, dass Sie "Hello 32-Bit ARM World" schreibt und als 32-Bit-ARM-Anwendung neu kompiliert wird.
-   Wenn die 32-Bit-x86-Anwendung auf 64-Bit-Windows ausgeführt wird, wird "Hello 32-Bit x86 World" angezeigt. Wenn die 64-Bit-Anwendung ausgeführt wird, wird "Hello 64-Bit World" angezeigt. **Windows 10 auf ARM:** Wenn die 32-Bit-ARM-Anwendung unter 64-Bit ARM64 Windows ausgeführt wird, wird "Hello 32-Bit ARM World" angezeigt. Alle Anwendungen nennen dieselben Registrierungsfunktionen mit demselben vordefinierten Handle und demselben Schlüsselnamen. der Unterschied besteht darin, dass jede Anwendung mit ihrer logischen Ansicht der Registrierung arbeitet und jede Ansicht einem separaten physischen Speicherort der Registrierung zugeordnet ist. Dadurch bleiben alle Versionen der Zeichenfolge intakt.

Umgeleitete Schlüssel werden physischen Standorten unter **Wow6432Node** zugeordnet. Beispielsweise wird die **Software HKEY \_ local \_ Machine \\** an **HKEY \_ local \_ Machine \\ Software \\ Wow6432Node** umgeleitet. Der physische Speicherort umgeleiteter Schlüssel sollte jedoch vom System als reserviert betrachtet werden. Anwendungen sollten nicht direkt auf den physischen Speicherort eines Schlüssels zugreifen, da sich dieser Speicherort möglicherweise ändert. Weitere Informationen finden Sie unter [zugreifen auf eine Alternative Registrierungs Ansicht](accessing-an-alternate-registry-view.md).

**Windows 10 auf ARM:** Umgeleitete 32-Bit-ARM-Schlüssel werden physischen Standorten unter WowAA32Node zugeordnet.

Um 32-Bit-Anwendungen zu unterstützen, die **reg \_ SZ** oder reg schreiben, erweitern Sie die **\_ \_ SZ** -Daten, die% Program Files% oder% COMMONPROGRAMFILES% enthalten, in die Registrierung. WOW64 fängt diese Schreibvorgänge ab und ersetzt Sie durch "% Program Files (x86)%" und "% COMMONPROGRAMFILES (x86)%". Wenn sich beispielsweise das Verzeichnis "Programme" auf Laufwerk c befindet, wird "% Program Files (x86)%" zu "C: \\ Programme (x86)" erweitert. Der Austausch tritt nur auf, wenn die folgenden Bedingungen erfüllt sind:

-   Die Zeichenfolge muss mit% Program Files% oder% COMMONPROGRAMFILES% beginnen. Wenn die Zeichenfolge mit einem Leerzeichen oder einem anderen Zeichen als% beginnt, wird es nicht ersetzt.
-   Die Groß-/Kleinschreibung von% Program Files% oder% COMMONPROGRAMFILES% muss genau wie gezeigt lauten, da beim Zeichen folgen Vergleich die Groß-/Kleinschreibung beachtet wird Wenn die Zeichenfolge z. b. mit% COMMONPROGRAMFILES% anstelle von% COMMONPROGRAMFILES% beginnt, wird Sie nicht ersetzt.
-   Die Zeichenfolge darf den maximalen \_ Pfad von \* 2 + 15 Zeichen nicht überschreiten. Wenn Sie diese Länge überschreitet, wird Sie nicht ersetzt.
-   Der Schlüssel kann nicht mit dem Schlüssel \_ WOW64 \_ 64key geöffnet werden. Dieses Flag gibt an, dass Vorgänge für den Schlüssel in der 64-Bit-Registrierungs Ansicht ausgeführt werden sollen, sodass es nicht ersetzt wird. Weitere Informationen finden Sie unter [zugreifen auf eine Alternative Registrierungs Ansicht](accessing-an-alternate-registry-view.md).

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Das Key \_ Wow \_ 64 \_ 64key-Flag wirkt sich nicht darauf aus, ob ein Schlüssel ersetzt wird. Dieses Flag wirkt sich auf die Ersetzung ab, beginnend mit Windows 7 und Windows Server 2008 R2.

Darüber hinaus werden die Registrierungsschlüssel "REG SZ" oder "reg" mit "System32" durch " \_ \_ syswow64" \_ ersetzt. Die Zeichenfolge muss mit dem Pfad beginnen, der auf oder unter% windir% \\ system32 zeigt. Beim Zeichen folgen Vergleich wird die Groß-/Kleinschreibung nicht beachtet. Umgebungsvariablen werden vor der Übereinstimmung mit dem Pfad erweitert. Daher werden alle folgenden Pfade ersetzt:% windir% \\ system32,% systemroot% \\ system32 und C: \\ Windows \\ system32. Dieser Patch wird nur auf die Schlüssel angewendet, die vor Windows 7 reflektiert wurden.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Registrierungs Reflektion](registry-reflection.md)
-   [Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md)
-   [Zugreifen auf eine Alternative Registrierungs Ansicht](accessing-an-alternate-registry-view.md)
-   [Beispiel für Registrierungs Umleitung auf WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Remote Registrierungs Zugriff in 64-Bit-Windows](remote-registry-access-in-64-bit-windows.md)

 

 




