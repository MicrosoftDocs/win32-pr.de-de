---
description: Das Erstellen von DLLs stellt Entwicklern eine Reihe von Herausforderungen dar.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Bewährte Methoden für Dynamic-Link Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88aba0999f3d0825c6d2f4df3afe09d766a82232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373306"
---
# <a name="dynamic-link-library-best-practices"></a>Bewährte Methoden für Dynamic-Link Bibliothek

* * Aktualisiert: * *

-   17. Mai 2006

**Wichtige APIs**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Das Erstellen von DLLs stellt Entwicklern eine Reihe von Herausforderungen dar. DLLs verfügen nicht über eine vom System erzwungene Versionierung. Wenn mehrere Versionen einer DLL auf einem System vorhanden sind, werden durch die einfache Übersetzung mit dem fehlenden Schema der Versionsverwaltung Abhängigkeiten und API-Konflikte erzeugt. Die Komplexität in der Entwicklungsumgebung, der Lade Lade Implementierung und den DLL-Abhängigkeiten hat eine Anfälligkeit in der Lade Reihenfolge und dem Anwendungsverhalten verursacht. Schließlich basieren viele Anwendungen auf DLLs und verfügen über komplexe Sätze von Abhängigkeiten, die berücksichtigt werden müssen, damit die Anwendungen ordnungsgemäß funktionieren. Dieses Dokument enthält Richtlinien für dll-Entwickler, die beim Aufbau stabiler, portabler und erweiterbarer DLLs helfen.

Eine nicht ordnungsgemäße Synchronisierung in [**DllMain**](dllmain.md) kann dazu führen, dass eine Anwendung in einer nicht initialisierten dll Deadlocks oder auf Daten oder Code zugreift. Durch das Aufrufen bestimmter Funktionen innerhalb von **DllMain** werden solche Probleme verursacht.

![Was geschieht, wenn eine Bibliothek geladen wird](images/fig1.png)

## <a name="general-best-practices"></a>Allgemeine bewährte Methoden

[**DllMain**](dllmain.md) wird aufgerufen, während die Loadersperre aufrechterhalten wird. Daher gelten für die Funktionen, die innerhalb von **DllMain** aufgerufen werden können, bedeutende Einschränkungen. **DllMain** ist daher für die Durchführung minimaler Initialisierungs Aufgaben konzipiert, indem eine kleine Teilmenge der Microsoft® Windows®-API verwendet wird. Sie können keine Funktion in **DllMain** aufgerufen werden, die direkt oder indirekt versucht, die Loadersperre abzurufen. Andernfalls wird die Möglichkeit eingeführt, dass Ihre Anwendung Deadlocks oder abstürzt. Ein Fehler in einer **DllMain** -Implementierung kann den gesamten Prozess und alle zugehörigen Threads gefährden.

Der ideale [**DllMain**](dllmain.md) -Wert ist nur ein leerer Stub. Aufgrund der Komplexität vieler Anwendungen ist dies jedoch im Allgemeinen zu restriktiv. Eine gute Faustregel für **DllMain** besteht darin, so viele Initialisierungen wie möglich zu verschieben. Die verzögerte Initialisierung erhöht die Stabilität der Anwendung, da diese Initialisierung nicht durchgeführt wird, während die Loadersperre aufrechterhalten wird. Außerdem können Sie mit der verzögerten Initialisierung viel mehr von der Windows-API verwenden.

Einige Initialisierungs Tasks können nicht verschoben werden. Beispielsweise sollte eine DLL, die von einer Konfigurationsdatei abhängt, nicht geladen werden, wenn die Datei falsch formatiert ist oder eine Garbage Collection enthält. Bei dieser Art der Initialisierung sollte die dll die Aktion durchführen und schnell einen Fehler erzeugen, anstatt Ressourcen durch Abschließen anderer Aufgaben zu verschwenden.

Sie sollten die folgenden Aufgaben niemals innerhalb von [**DllMain**](dllmain.md)ausführen:

-   Aufrufen von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (entweder direkt oder indirekt). Dies kann zu einem Deadlock oder einem Absturz führen.
-   Aufrufen von [**getstringtypea**](/windows/desktop/api/winnls/nf-winnls-getstringtypea), [**getstringtypeex**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)oder [**getstringtypew**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) (entweder direkt oder indirekt). Dies kann zu einem Deadlock oder einem Absturz führen.
-   Mit anderen Threads synchronisieren. Dies kann zu einem Deadlock führen.
-   Rufen Sie ein Synchronisierungs Objekt ab, das im Besitz von Code ist, der darauf wartet, die Loadersperre abzurufen. Dies kann zu einem Deadlock führen.
-   Initialisieren Sie com-Threads mithilfe von [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Unter bestimmten Bedingungen kann diese Funktion [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)aufrufen.
-   Aufrufe der Registrierungsfunktionen. Diese Funktionen werden in Advapi32.dll implementiert. Wenn Advapi32.dll nicht vor der DLL initialisiert wird, kann die dll auf nicht initialisierten Speicher zugreifen und den Prozess abstürzen.
-   Aufrufen von " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)". Beim Erstellen eines Prozesses kann eine andere DLL geladen werden.
-   [**ExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)aufzurufen. Wenn Sie einen Thread beim Trennen der dll beenden, kann dies dazu führen, dass die Loadersperre erneut abgerufen wird, was zu einem Deadlock oder einem Absturz führt.
-   Aufrufen von " [**foratethread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)". Das Erstellen eines Threads kann funktionieren, wenn Sie nicht mit anderen Threads synchronisieren, aber es ist riskant.
-   Erstellen Sie eine Named Pipe oder ein anderes benanntes Objekt (nur Windows 2000). In Windows 2000 werden benannte Objekte von der Terminal Dienste-dll bereitgestellt. Wenn diese DLL nicht initialisiert ist, können Aufrufe der dll zu einem Absturz des Prozesses führen.
-   Verwenden Sie die Speicher Verwaltungsfunktion aus dem dynamischen C-Run-Time (CRT). Wenn die CRT-DLL nicht initialisiert ist, können Aufrufe dieser Funktionen dazu führen, dass der Prozess abstürzt.
-   Aufrufe von Funktionen in User32.dll oder Gdi32.dll. Einige Funktionen laden eine andere dll, die möglicherweise nicht initialisiert wird.
-   Verwenden Sie verwalteten Code.

Die folgenden Aufgaben können in **DllMain** sicher ausgeführt werden:

-   Initialisieren statischer Datenstrukturen und Member zum Zeitpunkt der Kompilierung.
-   Hiermit werden Synchronisierungs Objekte erstellt und initialisiert.
-   Zuweisen von Speicher und initialisieren dynamischer Datenstrukturen (vermeiden der oben aufgeführten Funktionen)
-   Einrichten von lokalem Thread Speicher (TLS).
-   Öffnen, Lesen von und Schreiben in Dateien.
-   Aufrufe von Funktionen in Kernel32.dll (außer den oben aufgeführten Funktionen).
-   Legen Sie globale Zeiger auf NULL fest, und legen Sie die Initialisierung dynamischer Member ab. In der™ von Microsoft Windows Vista können Sie die einmaligen Initialisierungs Funktionen verwenden, um sicherzustellen, dass ein Codeblock nur einmal in einer Multithread-Umgebung ausgeführt wird.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Deadlocks, die durch eine Sperr Reihenfolge verursacht werden

Wenn Sie Code implementieren, der mehrere Synchronisierungs Objekte verwendet, z. b. sperren, ist es wichtig, die Sperr Reihenfolge zu berücksichtigen. Wenn mehr als eine Sperre gleichzeitig abgerufen werden muss, müssen Sie eine explizite Rangfolge definieren, die als Sperr Hierarchie oder Sperr Reihenfolge bezeichnet wird. Wenn z. b. Sperre a vor Sperre an einer beliebigen Stelle im Code abgerufen wird und Lock b vor der Sperre C an anderer Stelle im Code abgerufen wird, ist die Sperr Reihenfolge a, B, C, und diese Reihenfolge sollte im gesamten Code befolgt werden. Die Inversion der Sperre tritt auf, wenn die Sperr Reihenfolge nicht eingehalten wird, z. –. Wenn Sperre B vor Sperre a abgerufen wird. die Sperr Reihenfolge Inversion kann Deadlocks verursachen, die schwer zu Debuggen sind Um solche Probleme zu vermeiden, müssen alle Threads Sperren in derselben Reihenfolge erhalten.

Beachten Sie, dass das Lade Modul [**DllMain**](dllmain.md) mit der bereits erworbenen Lade Lade Sperre aufruft, sodass die Loadersperre in der Sperr Hierarchie die höchste Priorität haben sollte. Beachten Sie außerdem, dass Code nur die Sperren abrufen muss, die für die ordnungsgemäße Synchronisierung erforderlich sind. Es muss nicht jede einzelne Sperre abgerufen werden, die in der Hierarchie definiert ist. Wenn z. b. für einen Code Abschnitt nur die Sperren a und c für die ordnungsgemäße Synchronisierung erforderlich sind, sollte der Code lock a abrufen, bevor er die Sperre C übernimmt. Es ist nicht erforderlich, dass der Code auch Lock B erhält. Außerdem kann der DLL-Code die Loadersperre nicht explizit abrufen. Wenn der Code eine API wie z. b. [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) aufrufen muss, die indirekt die Loadersperre abrufen kann, und der Code außerdem eine private Sperre erhalten muss, sollte der Code **GetModuleFileName** aufrufen, bevor er Lock P erhält. Dadurch wird sichergestellt, dass die Lade Reihenfolge eingehalten wird.

Abbildung 2 zeigt ein Beispiel, das die Inversion der Sperr Reihenfolge veranschaulicht. Ziehen Sie eine DLL in Erwägung, deren Hauptthread [**DllMain**](dllmain.md)enthält. Das Bibliotheks Lade Modul erhält die Loadersperre L und ruft dann **DllMain** auf. Der Haupt Thread erstellt die Synchronisierungs Objekte A, B und G, um den Zugriff auf seine Datenstrukturen zu serialisieren, und versucht dann, Lock G abzurufen. Ein Arbeits Thread, der Lock G bereits erfolgreich abgerufen hat, ruft dann eine Funktion wie z. b. GetModuleHandle auf, die versucht, die Loadersperre zu erhalten. Daher wird der Arbeits Thread in L blockiert, und der Haupt Thread wird auf G blockiert, was zu einem Deadlock führt.

![Deadlocks aufgrund von Sperr Reihenfolge-Inversion](images/fig2.png)

Um Deadlocks zu verhindern, die durch die Inversion der Sperr Reihenfolge verursacht werden, sollten alle Threads jederzeit versuchen, Synchronisierungs Objekte in der definierten Lade Reihenfolge zu erhalten.

## <a name="best-practices-for-synchronization"></a>Bewährte Methoden für die Synchronisierung

Angenommen, eine DLL erstellt Arbeitsthreads im Rahmen der Initialisierung. Bei der dll-Bereinigung ist es erforderlich, eine Synchronisierung mit allen Arbeitsthreads durchzusetzen, um sicherzustellen, dass sich die Datenstrukturen in einem konsistenten Zustand befinden, und dann die Arbeitsthreads zu beenden. Heute gibt es keine einfache Möglichkeit, das Problem der ordnungsgemäßen Synchronisierung und des herunter Fahrens von DLLs in einer Multithread-Umgebung vollständig zu lösen. In diesem Abschnitt werden die aktuellen bewährten Methoden für die Synchronisierung von Threads beim Herunterfahren der dll beschrieben.

Thread Synchronisierung in [**DllMain**](dllmain.md) beim Prozess beenden

-   Wenn [**DllMain**](dllmain.md) beim Prozess beenden aufgerufen wird, wurden alle Threads des Prozesses zwangsweise bereinigt, und es besteht die Möglichkeit, dass der Adressraum inkonsistent ist. Die Synchronisierung ist in diesem Fall nicht erforderlich. Das heißt, der ideale dll- \_ Prozess Trennungs \_ Handler ist leer.
-   Windows Vista stellt sicher, dass die Kern Datenstrukturen (Umgebungsvariablen, Aktuelles Verzeichnis, Prozess Heap usw.) in einem konsistenten Zustand sind. Allerdings können andere Datenstrukturen beschädigt werden, sodass das Bereinigen des Speichers nicht sicher ist.
-   Der persistente Zustand, der gespeichert werden muss, muss in einen permanenten Speicher geleert werden.

Thread Synchronisierung in **DllMain** für DLL- \_ Thread Trennung \_ beim Entladen der dll

-   Wenn die DLL entladen wird, wird der Adressraum nicht entfernt. Daher wird erwartet, dass die dll ein sauberes Herunterfahren durchführt. Dies umfasst die Thread Synchronisierung, geöffnete Handles, den persistenten Zustand und zugeordnete Ressourcen.
-   Die Thread Synchronisierung ist schwierig, da das warten auf Threads zum Beenden in [**DllMain**](dllmain.md) einen Deadlock verursachen kann. Beispielsweise enthält dll A die Loadersperre. Es signalisiert Thread T, zu beenden und zu warten, bis der Thread beendet wird. Thread T wird beendet, und das Lade Modul versucht, die Loadersperre zu erhalten, um den **DllMain** von dll A mit dll-Thread Trennung aufzurufen \_ \_ . Dies führt zu einem Deadlock. So minimieren Sie das Risiko eines Deadlocks:
    -   Dll a Ruft eine DLL \_ -Thread Trennungs \_ Nachricht in seiner [**DllMain**](dllmain.md) -Datei ab und legt ein Ereignis für Thread T fest, das den Vorgang zum Beenden signalisiert.
    -   Thread T schließt seinen aktuellen Task ab, bringt ihn in einen konsistenten Zustand, signalisiert dll a und wartet unendlich. Beachten Sie, dass die Konsistenz Prüfungsroutinen dieselben Einschränkungen wie [**DllMain**](dllmain.md) einhalten müssen, um Deadlocks zu vermeiden.
    -   DLL A beendet T und weiß, dass es sich in einem konsistenten Zustand befindet.

Wenn eine DLL entladen wird, nachdem alle Threads erstellt wurden, aber bevor Sie mit der Ausführung beginnen, stürzt der Thread möglicherweise ab. Wenn die dll im Rahmen der Initialisierung Threads im zugehörigen **DllMain** -Element erstellt hat, ist die Initialisierung einiger Threads möglicherweise nicht abgeschlossen, und die zugehörige DLL- \_ Thread \_ Anfüge Nachricht wartet immer noch auf die Übermittlung an die dll. Wenn die dll in dieser Situation entladen wird, beginnt Sie mit dem Beenden von Threads. Einige Threads werden jedoch möglicherweise hinter der Loadersperre blockiert. Ihre DLL- \_ Thread \_ Anfüge Nachrichten werden verarbeitet, nachdem die Zuordnung der dll aufgehoben wurde, wodurch der Prozess abstürzt.

## <a name="recommendations"></a>Empfehlungen

Folgende Richtlinien werden empfohlen:

-   Verwenden Sie Application Verifier, um die häufigsten Fehler in [**DllMain**](dllmain.md)abzufangen.
-   Wenn Sie in [**DllMain**](dllmain.md)eine private Sperre verwenden, definieren Sie eine Sperr Hierarchie, und verwenden Sie sie einheitlich. Die Loadersperre muss sich am Ende der Hierarchie befinden.
-   Vergewissern Sie sich, dass keine Aufrufe von einer anderen dll abhängen, die möglicherweise noch nicht vollständig geladen wurde.
-   Führen Sie einfache Initialisierungen statisch zum Zeitpunkt der Kompilierung anstelle von [**DllMain**](dllmain.md)aus.
-   Stellen Sie alle Aufrufe in [**DllMain**](dllmain.md) zurück, die bis zu einem späteren Zeitpunkt warten können.
-   Verzögert Initialisierungs Tasks, die bis zu einem späteren Zeitpunkt warten können. Bestimmte Fehlerbedingungen müssen früh erkannt werden, damit die Anwendung Fehler ordnungsgemäß behandeln kann. Es gibt jedoch Kompromisse zwischen dieser frühen Erkennung und dem Verlust der Stabilität, die daraus resultieren können. Das Verzögern der Initialisierung ist häufig am besten geeignet.

 

 
