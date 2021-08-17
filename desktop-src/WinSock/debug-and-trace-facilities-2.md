---
description: Debuggen und Verfolgen von Funktionen und Windows Sockets 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Debug- und Ablaufverfolgungs-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0617aa8fc18e90b0c3e366a7ab14f1457cb26471865bfcc97682801a858565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741367"
---
# <a name="debug-and-trace-facilities"></a>Debug- und Ablaufverfolgungs-Funktionen

Windows Sockets 2-Anwendungsentwickler müssen Fehler in:

-   Die Anwendung.
-   *Ws232.dll\_* oder eine der Kompatibilitäts-Shim-DLLs.
-   Der Dienstanbieter.

Windows Sockets 2 löst diese Notwendigkeit mit mehreren Komponenten und Features:

-   Integrierte Unterstützung für die Winsock-Ablaufverfolgung Windows Vista und höher.
-   Eine speziell entwickelte Debugversion des *Ws2-32.dll\_* unter Windows Vista.
-   Eine separate primitive Debug- und Ablaufverfolgungseinrichtung zur Verwendung auf Windows Server 2003 und Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Winsock-Ablaufverfolgung mit ereignisablaufverfolgung für Windows

Integrierte Unterstützung für die Winsock-Ablaufverfolgung mithilfe der Ereignisablaufverfolgung für Windows (ETW) ist in Windows Vista und höher enthalten. Dies ist die bevorzugte Methode zum Nachverfolgen von Winsock-Aufrufen auf Windows Vista und höher. Die Winsock-Ablaufverfolgung mit ETW ist einfach und funktioniert mit Verkaufsversionen Windows. Es sind keine zusätzliche Software oder Komponenten erforderlich. Dieses Feature muss nur auf Windows Vista und höher aktiviert werden. Ausführlichere Informationen finden Sie in den [Themen zur Winsock-Ablaufverfolgung.](winsock-tracing.md)

## <a name="using-a-debug-version-of-ws2_32dll"></a>Verwenden einer Debugversion von Ws2 \_32.dll

Die Kombination einer Debugversion von *Ws2 \_32.dll* unter Windows Vista und Winsock-Ablaufverfolgung ermöglicht es, alle Prozeduraufrufe über die Windows Sockets 2-API oder SPI hinweg zu überwachen und in gewissem Umfang zu steuern.

Wenn eine Version des Microsoft Windows Software Development Kit (SDK) für Windows Vista am Standardspeicherort installiert ist, befinden sich Debugversionen von *Ws2 \_32.dll* für verschiedene Architekturen im folgenden Ordner:

**C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v6.0 \\ NoRedist**

Es sollte eine überprüfte Version des *\_ Ws2-32.dll* verwendet werden, die der Version von Windows und dem Service Pack entspricht, für das Sie testen. Beachten Sie, dass möglicherweise Sicherheitspatches angewendet wurden, die die *Ws2-32.dll\_* auf Ihrem Testsystem aktualisiert haben. Das Windows SDK für Windows Vista und die früheren DVD/CD-Abonnements des Platform Software Development Kit (SDK) enthalten überprüfte Builds für die verschiedenen Versionen Windows. Sie sollten die gleiche überprüfte Version des *\_ Ws2-32.dll* wie die Verkaufsversion verwenden, die auf dem getesteten System verwendet wurde. Beachten Sie auch, dass das Verhalten, das unter einem überprüften Build ausgeführt wird, nicht mit dem Ausführen mit einem Einzelhandels-Build identisch ist.

**Hinweis:**  Das Windows SDK für Windows Server 2008 und höher enthält keine speziellen Debugversionen der *Ws2-32.dll. \_* Entwickler sollten stattdessen die Winsock-Ablaufverfolgung mit ETW verwenden, da diese Funktion keine Debugbuilds erfordert.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Winsock Debug and Trace Facility on Windows Server 2003 and Windows XP

Ältere Versionen von Windows vor Windows 8 und Windows Server 2012 unterstützen eine separate primitive Debug- und Ablaufverfolgungseinrichtung, die als Beispiel mit dem Windows SDK und dem älteren Platform SDK enthalten ist. Die Debug-/Ablaufverfolgungseinrichtung sollte nur auf Windows Server 2003 und Windows XP verwendet werden, wobei die Winsock-Ablaufverfolgung nicht unterstützt wird.

Wenn das Windows SDK für Windows 7 am Standardspeicherort installiert ist, wird dieses primitive Winsock-Ablaufverfolgungsfeature im folgenden Ordner installiert:

**C: \\ Programme \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ NetDs \\ winsock dt \\ \_ dll**

Die *DbgSpec.doc* in diesem Ordner enthält Dokumentation zu dieser primitiven Ablaufverfolgungseinrichtung. Der Beispielcode im Ordner dt \_ dll muss kompiliert werden, um diese Einrichtung verwenden zu können. Entwickler können den Quellcode verwenden, um Versionen der Debug-/Ablaufverfolgungs-DLL zu entwickeln, die ihre spezifischen Anforderungen erfüllen.

Beachten Sie, dass dieses primitive Winsock-Ablaufverfolgungsfeature nur mit der Installierten Debugversion von *Ws2 \_32.dll* funktioniert. Sie müssen also eine überprüfte Version des *Ws2-32.dll\_ erhalten,* die der Version von Windows und dem Service Pack entspricht, für das Sie testen.

Eine Einschränkung dieser primitiven DT DLL-Ablaufverfolgungsfunktion besteht in der Verwendung einer globalen Sperre (kritischer Abschnitt) für jeden \_ Winsock-Funktionsaufruf. Daher ist diese Einrichtung für den Umgang mit Racebedingungen nicht nützlich. Der Beispielcode muss erheblich umgeschrieben werden, damit diese Ablaufverfolgungseinrichtung für den Umgang mit den meisten tatsächlichen Winsock-Problemen (ersetzen der globalen Sperren) nützlich ist. Mit diesem Beispielcode können Entwickler die Prozeduraufrufe, Prozedurrückrufe, Parameterwerte und Rückgabewerte nachverfolgen.

Entwickler können diesen primitiven Mechanismus verwenden, um Prozeduraufrufe, Prozedurrückrufe, Parameterwerte und Rückgabewerte zu verfolgen. Parameterwerte und Rückgabewerte können beim Prozeduraufruf oder bei der Prozedur-Rückgabe geändert werden. Bei Wunsch kann ein Prozeduraufruf verhindert oder umgeleitet werden. Mit dem Zugriff auf diese Ebene von Informationen und Kontrolle ist ein Entwickler besser in der Lage, ein Problem in der Anwendung, *Ws2 \_* 32.dlloder Dienstanbieter zu isolieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> </dl>

 

 



