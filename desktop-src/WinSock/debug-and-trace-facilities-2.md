---
description: Debug-und Ablauf Verfolgungs Funktionen und Windows Sockets 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Debug-und Ablauf Verfolgungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288c6b4d72a7a375ee16da23a25b0a04a46df91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345064"
---
# <a name="debug-and-trace-facilities"></a>Debug-und Ablauf Verfolgungs Funktionen

Entwickler von Windows Sockets 2-Anwendungen müssen Fehler in den folgenden Fenstern isolieren:

-   Die Anwendung.
-   Die *Ws2- \_32.dll* oder eine der DLLs für Kompatibilitäts-Shim.
-   Der Dienstanbieter.

Windows Sockets 2 erfüllt diese Anforderung durch mehrere Komponenten und Features:

-   Integrierte Unterstützung für die Winsock-Ablauf Verfolgung unter Windows Vista und höher.
-   Eine speziell entwickelte Debugversion des *Ws2- \_32.dll* unter Windows Vista.
-   Ein separates Primitives Debug-und Ablauf Verfolgungs Werk für die Verwendung unter Windows Server 2003 und Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Winsock-Ablauf Verfolgung mithilfe der Ereignis Ablauf Verfolgung für Windows

Integrierte Unterstützung für die Winsock-Ablauf Verfolgung mithilfe der Ereignis Ablauf Verfolgung für Windows (ETW) ist unter Windows Vista und höher enthalten. Dies ist die bevorzugte Methode für die Ablauf Verfolgung von Winsock-aufrufen unter Windows Vista und höher. Die Winsock-Ablauf Verfolgung unter Verwendung von etw ist einfach und funktioniert für Einzelhandelsversionen von Windows. Es sind keine zusätzlichen Softwarekomponenten oder Komponenten erforderlich. Diese Funktion muss nur unter Windows Vista und höher aktiviert werden. Ausführlichere Informationen finden Sie in den Themen zur [Winsock](winsock-tracing.md) -Ablauf Verfolgung.

## <a name="using-a-debug-version-of-ws2_32dll"></a>Verwenden einer Debugversion von Ws2 \_32.dll

Durch die Kombination einer Debugversion des *Ws2- \_32.dll* unter Windows Vista und der Winsock-Ablauf Verfolgung können alle Prozedur Aufrufe für die Windows Sockets 2-API oder SPI überwacht und in gewissem Umfang gesteuert werden.

Wenn eine Version des Microsoft Windows Software Development Kit (SDK) für Windows Vista am Standard Speicherort installiert ist, befinden sich die Debugversionen des *Ws2- \_32.dll* für verschiedene Architekturen unter folgendem Ordner:

**C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 6.0 \\ NoRedist**

Eine überprüfte Version des *Ws2- \_32.dll* , die mit der Version von Windows übereinstimmt, und dem Service Pack, das Sie testen, sollte verwendet werden. Beachten Sie, dass möglicherweise Sicherheitspatches angewendet wurden, die den *Ws2- \_32.dll* auf Ihrem Testsystem aktualisiert haben. Die Windows SDK für Windows Vista und frühere Platform Software Development Kit (SDK) DVD/CD-Abonnements enthalten überprüfte Builds für die verschiedenen Versionen von Windows. Sie sollten dieselbe überprüfte Version des Ws2- *\_32.dll* verwenden wie die Verkaufsversion, die auf dem getesteten System verwendet wurde. Beachten Sie auch, dass das Verhalten, das unter einem überprüften Build ausgeführt wird, nicht mit dem Ausführen eines Einzelhandels Builds identisch ist.

**Hinweis**  Der Windows SDK für Windows Server 2008 und höher enthält keine speziellen Debugversionen der *Ws2- \_32.dll*. Entwickler sollten stattdessen die Winsock-Ablauf Verfolgung mit etw verwenden, da diese Funktion keine Debugbuilds erfordert.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Winsock-Debug-und-Ablauf Verfolgungs Einrichtung unter Windows Server 2003 und Windows XP

Ältere Versionen von Windows vor Windows 8 und Windows Server 2012 unterstützen ein separates Primitives Debug-und Ablauf Verfolgungs Werk, das als Beispiel mit dem Windows SDK und dem älteren Platform SDK enthalten ist. Die Debug/Trace-Funktion sollte nur unter Windows Server 2003 und Windows XP verwendet werden, wo die Winsock-Ablauf Verfolgung nicht unterstützt wird.

Wenn die Windows SDK für Windows 7 am Standard Speicherort installiert ist, wird diese primitive Winsock-Ablauf Verfolgungs Funktion im folgenden Ordner installiert:

**C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Beispiele \\ netds \\ Winsock \\ dt \_ dll**

Die *DbgSpec.doc* -Datei in diesem Ordner enthält eine Dokumentation zu dieser primitiven Ablauf Verfolgungs Funktion. Der Beispielcode im Ordner dt \_ dll muss für die Verwendung dieser Funktion kompiliert werden. Entwickler können den Quellcode nutzen, um Versionen der Debug/Trace-dll zu entwickeln, die Ihre speziellen Anforderungen erfüllen.

Beachten Sie, dass diese primitive Winsock-Ablauf Verfolgungs Funktion nur bei installierter Debugversion von *Ws2 \_32.dll* funktioniert. Daher müssen Sie eine aktivierte Version des *Ws2- \_32.dll* erhalten, die mit der Version von Windows und dem Service Pack übereinstimmt, das Sie testen.

Eine Einschränkung dieser primitiven Ablauf \_ Verfolgungs Funktion der dt-dll besteht darin, dass im Beispielcode für jeden Winsock-Funktions aufrufeine globale Sperre (kritischer Abschnitt) verwendet wird. Diese Funktion ist daher für den Umgang mit Racebedingungen nicht nützlich. Der Beispielcode müsste erheblich umgeschrieben werden, damit diese Ablauf Verfolgungs Funktion für den Umgang mit den meisten echten Winsock-Problemen nützlich ist (ersetzt die globalen sperren). Dieser Beispielcode ermöglicht Entwicklern das Verfolgen von Prozedur aufrufen, Prozedur Rückgaben, Parameterwerten und Rückgabe Werten.

Entwickler können diesen primitiven Mechanismus verwenden, um Prozedur Aufrufe, Prozedur Rückgaben, Parameterwerte und Rückgabewerte zu verfolgen. Parameter Werte und Rückgabewerte können bei Prozedur aufrufen oder Prozedur Rücklauf geändert werden. Wenn gewünscht, kann ein Prozedur Aufrufwert verhindert oder umgeleitet werden. Durch den Zugriff auf diese Ebene von Informationen und Kontrolle kann ein Entwickler ein Problem in der Anwendung, *Ws2 \_32.dll* oder dem Dienstanbieter isolieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> </dl>

 

 



