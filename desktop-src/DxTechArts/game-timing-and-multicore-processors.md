---
title: Zeitliche Steuerung von Spielen und Multi-Core-Prozessoren
description: In diesem Artikel wird eine genauere, zuverlässigere Lösung vorgeschlagen, um mithilfe der Windows-APIs QueryPerformanceCounter und QueryPerformanceFrequency cpu-Zeitsteuerungen mit hoher Auflösung zu erhalten.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7a6d9d65ccb79c7b496b4d02b1bed132bdc2d3f
ms.sourcegitcommit: 998a611c97d5e20ac0c45e3bda768ae67d8c2cca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "109725009"
---
# <a name="game-timing-and-multicore-processors"></a>Zeitliche Steuerung von Spielen und Multi-Core-Prozessoren

Da Energieverwaltungstechnologien auf den heutigen Computern immer häufiger verwendet werden, funktioniert die RDTSC-Anweisung, eine häufig verwendete Methode zum Abrufen von hochauflösenden CPU-Zeitsteuerungen, möglicherweise nicht mehr wie erwartet. In diesem Artikel wird eine genauere, zuverlässigere Lösung vorgeschlagen, um mithilfe der Windows-APIs [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)hohe CPU-Zeitsteuerungen zu erhalten.

-   [Hintergrund](#background)
-   [Empfehlungen](#recommendations)
-   [Anwendungskompatibilität](#application-compatibility)

## <a name="background"></a>Hintergrund

Seit der Einführung des x86 P5-Anweisungssets haben viele Spieleentwickler den Zeitstempelzähler für Lesezeit, die RDTSC-Anweisung, verwendet, um eine zeitbasierte Zeitsteuerung mit hoher Auflösung durchzuführen. Die Windows-Multimedia-Timer sind präzise genug für die Audio- und Videoverarbeitung, aber mit Framezeiten von einem Dutzend Millisekunden oder weniger haben sie nicht genügend Auflösung, um Deltazeitinformationen zu liefern. Viele Spiele verwenden immer noch einen Multimedia-Timer beim Start, um die Häufigkeit der CPU zu festlegen, und sie verwenden diesen Frequency-Wert, um Ergebnisse von RDTSC zu skalieren, um eine genaue Zeit zu erhalten. Aufgrund der Einschränkungen von RDTSC bietet die Windows-API die korrektere Möglichkeit, über die Routinen von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)auf diese Funktionalität zuzugreifen.

Diese Verwendung von RDTSC für die zeitlichen Steuerungen ist von den folgenden grundlegenden Problemen betroffen:

-   Diskontinuitätswerte. Bei der direkten Verwendung von RDTSC wird davon ausgegangen, dass der Thread immer auf demselben Prozessor ausgeführt wird. Systeme mit mehreren Prozessoren und dualen Kernen garantieren nicht die Synchronisierung ihrer Zykluszähler zwischen Kernen. Dies wird in Kombination mit modernen Energieverwaltungstechnologien verstärkt, die verschiedene Kerne zu unterschiedlichen Zeiten leeren und wiederherstellen, was dazu führt, dass die Kerne in der Regel nicht synchronisiert werden. Für eine Anwendung führt dies im Allgemeinen zu Störungen oder potenziellen Abstürzen, wenn der Thread zwischen den Prozessoren springt und Zeitsteuerungswerte erhält, die zu großen Deltas, negativen Deltas oder angehaltener Zeitsteuerung führen.
-   Verfügbarkeit dedizierter Hardware. RDTSC sperrt die Zeitsteuerungsinformationen, die die Anwendung an den Zykluszähler des Prozessors anfordert. Viele Jahre lang war dies die beste Möglichkeit, präzise Zeitsteuerungsinformationen zu erhalten, aber neuere Hauptplatinen enthalten jetzt dedizierte Zeitsteuerungsgeräte, die hochauflösende Zeitsteuerungsinformationen ohne die Nachteile von RDTSC bereitstellen.
-   Variabilität der CPU-Häufigkeit. Häufig wird davon ausgegangen, dass die Cpu-Häufigkeit für die Lebensdauer des Programms festgelegt ist. Bei modernen Energieverwaltungstechnologien ist dies jedoch eine falsche Annahme. Obwohl sie anfänglich auf Laptopcomputer und andere mobile Geräte beschränkt war, wird technologie, die die CPU-Häufigkeit ändert, auf vielen High-End-Desktop-PCs verwendet. Das Deaktivieren seiner Funktion, um eine konsistente Häufigkeit aufrechtzuerhalten, ist für Benutzer im Allgemeinen nicht akzeptabel.

## <a name="recommendations"></a>Empfehlungen

Spiele benötigen genaue Zeitsteuerungsinformationen, aber Sie müssen auch Zeitsteuerungscode so implementieren, dass die Probleme im Zusammenhang mit der Verwendung von RDTSC vermieden werden. Führen Sie beim Implementieren von Zeitsteuerung mit hoher Auflösung die folgenden Schritte aus:

1.  Verwenden Sie [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) anstelle von RDTSC. Diese APIs verwenden möglicherweise RDTSC, verwenden jedoch stattdessen Zeitsteuerungsgeräte auf der Hauptplatine oder andere Systemdienste, die qualitativ hochwertige, hochauflösende Zeitsteuerungsinformationen bereitstellen. RDTSC ist zwar viel schneller als **QueryPerformanceCounter,** da es sich bei letzterem um einen API-Aufruf handelt, aber es handelt sich um eine API, die mehrere Hundert Mal pro Frame ohne spürbare Auswirkungen aufgerufen werden kann. (Trotzdem sollten Entwickler versuchen, ihre Spiele so wenig wie möglich **QueryPerformanceCounter** aufrufen zu lassen, um Leistungseinbußen zu vermeiden.)
2.  Beim Berechnen von Deltas sollten die Werte zusammengeklammert werden, um sicherzustellen, dass Fehler in den Zeitsteuerungswerten keine Abstürze oder instabile zeitbezogene Berechnungen verursachen. Der Klammerbereich sollte von 0 (um negative Deltawerte zu verhindern) bis zu einem angemessenen Wert basierend auf der niedrigsten erwarteten Framerate liegen. Das Anschließen ist wahrscheinlich bei jedem Debuggen Ihrer Anwendung nützlich, aber denken Sie daran, wenn Sie eine Leistungsanalyse durchführen oder das Spiel in einem nicht optimierten Modus ausführen.
3.  Berechnen sie alle Zeitsteuerungen für einen einzelnen Thread. Die Berechnung der Zeitsteuerung für mehrere Threads , z. B. mit jedem Thread, der einem bestimmten Prozessor zugeordnet ist, verringert die Leistung von Systemen mit mehreren Kernen deutlich.
4.  Legen Sie mithilfe der Windows-API [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask)fest, dass dieser einzelne Thread auf einem einzelnen Prozessor verbleibt. In der Regel ist dies der Hauptspielthread. Während [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) und [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) in der Regel für mehrere Prozessoren angepasst werden, können Fehler im BIOS oder treiber dazu führen, dass diese Routinen unterschiedliche Werte zurückgeben, wenn der Thread von einem Prozessor zu einem anderen wechselt. Daher ist es am besten, den Thread auf einem einzelnen Prozessor zu halten.

    Alle anderen Threads sollten ausgeführt werden, ohne ihre eigenen Timerdaten zu sammeln. Es wird nicht empfohlen, einen Arbeitsthread zum Berechnen der Zeitsteuerung zu verwenden, da dies zu einem Synchronisierungsengpass wird. Stattdessen sollten Arbeitsthreads Zeitstempel aus dem Hauptthread lesen, und da die Arbeitsthreads nur Zeitstempel lesen, müssen keine kritischen Abschnitte verwendet werden.

5.  Rufen [**Sie QueryPerformanceFrequency nur**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) einmal auf, da sich die Häufigkeit nicht ändert, während das System ausgeführt wird.

## <a name="application-compatibility"></a>Anwendungskompatibilität

Viele Entwickler haben über viele Jahre Annahmen über das Verhalten von RDTSC getroffen, sodass es sehr wahrscheinlich ist, dass einige vorhandene Anwendungen probleme auftreten, wenn sie auf einem System mit mehreren Prozessoren oder Kernen aufgrund der zeitlichen Implementierung ausgeführt werden. Diese Probleme manifestieren sich in der Regel als Bewegungsproblemen oder Langsamkeitsbewegungen. Es gibt keine einfache Lösung für Anwendungen, die die Energieverwaltung nicht kennen, aber es gibt einen vorhandenen Shim, um zu erzwingen, dass eine Anwendung immer auf einem einzelnen Prozessor in einem Multiprozessorsystem ausgeführt wird.

Um diesen Shim zu erstellen, laden Sie das Microsoft Application Compatibility Toolkit von [Windows-Anwendungskompatibilität](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10)herunter.

Erstellen Sie mithilfe des Kompatibilitätsadministrators, der Teil des Toolkits ist, eine Datenbank Ihrer Anwendung und die zugehörigen Fehlerbehebungen. Erstellen Sie einen neuen Kompatibilitätsmodus für diese Datenbank, und wählen Sie den Kompatibilitätsfix **SingleProcAffinity** aus, um die Ausführung aller Threads der Anwendung auf einem einzelnen Prozessor/Kern zu erzwingen. Mithilfe des Befehlszeilentools Fixpack.exe (auch Teil des Toolkits) können Sie diese Datenbank in ein installierbares Paket für Installation, Tests und Verteilung konvertieren.

Anweisungen zur Verwendung des Kompatibilitätsadministrators finden Sie in der Dokumentation des Toolkits. Syntax für und Beispiele für die Verwendung von Fixpack.exe finden Sie in der Befehlszeilenhilfe.

Kundenorientierte Informationen finden Sie in den folgenden Knowledge Base-Artikeln von Microsoft Help and Support:

-   [Programme, die die QueryPerformanceCounter-Funktion verwenden, können in Windows Server 2003 und Windows XP](https://support.microsoft.com/kb/895980) eine schlechte Leistung erzielen (Artikel 895980)
-   [Die Spielleistung auf einem Windows XP-basierten Computer, der einen Dual-Core-Prozessor verwendet, ist möglicherweise schlecht](https://support.microsoft.com/kb/909944) (Artikel 909944)

 

 
