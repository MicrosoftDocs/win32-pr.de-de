---
title: Zeitliche Steuerung von Spielen und Multi-Core-Prozessoren
description: In diesem Artikel wird eine präzisere und zuverlässigere Lösung vorgeschlagen, um CPU-Zeitvorgaben mit hoher Auflösung mithilfe der Windows-APIs QueryPerformanceCounter und QueryPerformanceFrequency zu erhalten.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5c511f558b59e94945e63c44db225f34ac2583
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341947"
---
# <a name="game-timing-and-multicore-processors"></a>Zeitliche Steuerung von Spielen und Multi-Core-Prozessoren

Da Energie Verwaltungs Technologien heutzutage in den heutigen Computern üblich werden, funktioniert eine häufig verwendete Methode zum Abrufen von CPU-Zeitvorgaben mit hoher Auflösung, die RDTSC-Anweisung, möglicherweise nicht mehr wie erwartet. In diesem Artikel wird eine präzisere und zuverlässigere Lösung vorgeschlagen, um CPU-Zeitvorgaben mit hoher Auflösung mithilfe der Windows-APIs [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)zu erhalten.

-   [Hintergrund](#background)
-   [Empfehlungen](#recommendations)
-   [Anwendungskompatibilität](#application-compatibility)

## <a name="background"></a>Hintergrund

Seit der Einführung des x86-P5-Anweisungs Satzes haben viele Spieleentwickler den Lesezeit Stempel-Leistungs Besatz verwendet, die RDTSC-Anweisung, um eine zeitgesteuerte Zeitüberschreitung zu bieten. Die Windows-Multimediatimer sind für die Audio-und Videoverarbeitung präzise genug, aber mit Frame Zeiten von einem Dutzend Millisekunden oder weniger verfügen Sie nicht über genügend Auflösung, um Delta Zeit Informationen bereitzustellen. Viele Spiele verwenden beim Start weiterhin einen Multimediatimer, um die Häufigkeit der CPU festzulegen, und Sie verwenden diesen Frequency-Wert, um Ergebnisse aus RDTSC zu skalieren, um eine genaue Zeit zu erzielen. Aufgrund der Einschränkungen von RDTSC stellt die Windows-API die korrektere Methode zum Zugreifen auf diese Funktionalität durch die Routinen von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)bereit.

Diese Verwendung von RDTSC für die zeitliche Steuerung hat folgende grundlegende Probleme:

-   Diskontinuierliche Werte. Wenn Sie RDTSC direkt verwenden, wird davon ausgegangen, dass der Thread immer auf demselben Prozessor ausgeführt wird. Multiprozessor-und Dual-Core-Systeme garantieren nicht die Synchronisierung Ihrer Zyklen von Zyklen zwischen Kernen. Dies wird verstärkt, wenn Sie mit modernen Energie Verwaltungs Technologien kombiniert werden, die verschiedene Kerne zu unterschiedlichen Zeiten im Leerlauf und wiederherstellen, was dazu führt, dass die Kerne in der Regel nicht synchronisiert werden. Bei einer Anwendung führt dies in der Regel zu einem Absturz oder zu potenziellen abstürzen, da der Thread zwischen den Prozessoren springt und Zeit Steuerungs Werte abruft, die zu großen Delta-, negativen Delta-oder Zeitüberschreitungen führen.
-   Verfügbarkeit dedizierter Hardware. RDTSC sperrt die Zeit Steuerungsinformationen, die von der Anwendung angefordert werden, an den Zyklen des Prozessor-Durchlaufs. Schon seit vielen Jahren war dies die beste Möglichkeit, Zeit Steuerungsinformationen mit hoher Genauigkeit zu erhalten, aber neuere Hauptplatinen enthalten jetzt dedizierte Zeit Steuerungsgeräte, die Informationen zur zeitlichen Steuerung ohne die Nachteile von RDTSC bereitstellen.
-   Varianz der CPU-Häufigkeit. Die Annahme ist häufig, dass die Häufigkeit der CPU für die Lebensdauer des Programms fest liegt. Bei modernen Energie Verwaltungs Technologien ist dies jedoch eine falsche Annahme. Obwohl Sie anfänglich auf Laptop Computer und andere mobile Geräte beschränkt ist, wird die Häufigkeit der CPU-Auslastung in vielen High-End-Desktop-PCs verwendet. die Deaktivierung der Funktion zur Aufrechterhaltung einer konsistenten Häufigkeit ist für Benutzer in der Regel nicht akzeptabel.

## <a name="recommendations"></a>Empfehlungen

Spiele benötigen genaue Zeit Steuerungsinformationen. Sie müssen aber auch Zeit Steuerungs Code implementieren, um die Probleme zu vermeiden, die mit der Verwendung von RDTSC einhergehen. Führen Sie die folgenden Schritte aus, wenn Sie eine Zeitüberschreitung mit hoher Auflösung implementieren:

1.  Verwenden Sie [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) anstelle von RDTSC. Diese APIs verwenden möglicherweise RDTSC, verwenden jedoch stattdessen eine Zeit Steuerungsgeräte auf der Hauptplatine oder einige andere Systemdienste, die hochwertige Zeit Steuerungsinformationen mit hoher Auflösung bereitstellen. RDTSC ist zwar viel schneller als **QueryPerformanceCounter**, da es sich hierbei um einen API-Aufruf handelt, handelt es sich hierbei um eine API, die mehrere hundert Mal pro Frame aufgerufen werden kann, ohne dass eine spürbare Auswirkung besteht. (Dennoch sollten Entwickler versuchen, den Spiel **QueryPerformanceCounter** so wenig wie möglich aufzurufen, um Leistungseinbußen zu vermeiden.)
2.  Beim Berechnen von Delta Werten sollten die Werte geklammert werden, um sicherzustellen, dass Fehler in den Zeit Steuerungs Werten keine Abstürze oder instabilen zeitbezogenen Berechnungen verursachen. Der Klammer Bereich muss zwischen 0 (um negative Delta Werte zu vermeiden) auf einen angemessenen Wert basieren, der auf dem niedrigsten erwarteten Framerate basiert. Das anspannen ist wahrscheinlich für das Debuggen Ihrer Anwendung nützlich, aber achten Sie darauf, wenn Sie eine Leistungsanalyse durchführen oder das Spiel in einem nicht optimierten Modus ausführen.
3.  Berechnen Sie alle zeitliche Steuerung in einem einzelnen Thread. Berechnung der zeitlichen Steuerung in mehreren Threads – z. b. bei jedem Thread, der einem bestimmten Prozessor zugeordnet ist – verringert die Leistung von mehr Kernsystemen erheblich.
4.  Legen Sie den einzelnen Thread mithilfe der Windows-API [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask)auf einem einzelnen Prozessor fest. In der Regel ist dies der Hauptspiel Thread. Obwohl [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) in der Regel für mehrere Prozessoren angepasst werden, können Fehler im BIOS oder in den Treibern dazu führen, dass diese Routinen andere Werte zurückgeben, wenn der Thread von einem Prozessor zu einem anderen verschoben wird. Daher ist es am besten, den Thread auf einem einzelnen Prozessor beizubehalten.

    Alle anderen Threads sollten ausgeführt werden, ohne eigene Zeit Geber Daten zu sammeln. Es wird nicht empfohlen, einen Arbeits Thread zum Berechnen der zeitlichen Steuerung zu verwenden, da dies zu einem Synchronisierungs Engpass wird. Stattdessen sollten Arbeitsthreads Zeitstempel aus dem Haupt Thread lesen, und da die Arbeitsthreads nur Zeitstempel lesen, ist es nicht erforderlich, kritische Abschnitte zu verwenden.

5.  Der Aufruf von [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) erfolgt nur einmal, da sich die Häufigkeit nicht ändert, während das System ausgeführt wird.

## <a name="application-compatibility"></a>Anwendungskompatibilität

Viele Entwickler haben über viele Jahre Annahmen über das Verhalten von RDTSC festgestellt. es ist daher sehr wahrscheinlich, dass einige vorhandene Anwendungen Probleme verursachen, wenn Sie auf einem System mit mehreren Prozessoren oder Kernen ausgeführt werden, die auf die zeitliche Implementierung zurückzuführen sind. Diese Probleme werden in der Regel als ein-oder langsamer Bewegungswechsel verwendet. Es gibt keine einfache Lösung für Anwendungen, die die Energie Verwaltung nicht kennen, aber es gibt ein vorhandenes Shim, mit dem eine Anwendung immer auf einem einzelnen Prozessor in einem Multiprozessorsystem ausgeführt werden kann.

Um dieses Shim zu erstellen, laden Sie das Microsoft Application Compatibility Toolkit von der [Windows-Anwendungs Kompatibilität](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10)herunter.

Erstellen Sie mit dem Kompatibilitäts Administrator, der Teil des Toolkits ist, eine Datenbank Ihrer Anwendung und zugehörige Korrekturen. Erstellen Sie einen neuen Kompatibilitätsmodus für diese Datenbank, und wählen Sie die Kompatibilitäts Korrektur **singleprocaffität** aus, um zu erzwingen, dass alle Threads der Anwendung auf einem einzelnen Prozessor/Kern ausgeführt werden. Mithilfe des Befehlszeilen Tools Fixpack.exe (auch Teil des-Toolkits) können Sie diese Datenbank in ein installier bares Paket konvertieren, um die Installation, das Testen und die Verteilung zu überprüfen.

Anweisungen zur Verwendung des Kompatibilitäts Administrators finden Sie in der Dokumentation des Toolkits. Syntax und Beispiele für die Verwendung von Fixpack.exe finden Sie in der Befehlszeilen Hilfe.

Kundenorientierte Informationen finden Sie in den folgenden Knowledge Base-Artikeln von Microsoft-Hilfe und-Support:

-   [Programme, die die QueryPerformanceCounter-Funktion in Windows Server 2003 und Windows XP](https://support.microsoft.com/kb/895980) (Artikel 895980) unter Umständen schlecht ausführen
-   [Die Spielleistung kann auf einem Windows XP-basierten Computer, der einen Dual-Core-Prozessor verwendet, gering sein](https://support.microsoft.com/kb/909944) (Artikel 909944).

 

 