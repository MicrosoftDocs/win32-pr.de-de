---
description: Das Erstellen von DLLs stellt Entwickler vor eine Reihe von Herausforderungen.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Dynamic-Link Bibliothek – Bewährte Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d02314b15a13de7658c0b87ba7cd998f48a0a3d9f2f2682b36539bd9f5bde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696580"
---
# <a name="dynamic-link-library-best-practices"></a>Dynamic-Link Bibliothek – Bewährte Methoden

**Aktualisiert: **

-   17. Mai 2006

**Wichtige APIs**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Das Erstellen von DLLs stellt Entwickler vor eine Reihe von Herausforderungen. DLLs verfügen nicht über eine vom System erzwungene Versionsvererbung. Wenn mehrere Versionen einer DLL auf einem System vorhanden sind, führt die einfache Überschreiben von in Verbindung mit dem Fehlen eines Versionsschemas zu Abhängigkeits- und API-Konflikten. Die Komplexität in der Entwicklungsumgebung, der Loaderimplementierung und den DLL-Abhängigkeiten hat zu einer Zerbrechlichkeit in der Lade reihenfolge und im Anwendungsverhalten geführt. Schließlich verwenden viele Anwendungen DLLs und verfügen über komplexe Sätze von Abhängigkeiten, die für eine ordnungsgemäße Funktionsweise der Anwendungen zu berücksichtigen sind. Dieses Dokument enthält Richtlinien für DLL-Entwickler, die Sie beim Erstellen robuster, portabler und erweiterbarer DLLs unterstützen.

Eine nicht ordnungsgemäße [**Synchronisierung in DllMain**](dllmain.md) kann dazu führen, dass eine Anwendung deadlockt oder auf Daten oder Code in einer nicht initialisierten DLL zu zugreifen kann. Das Aufrufen bestimmter Funktionen innerhalb **von DllMain** verursacht solche Probleme.

![Was geschieht, wenn eine Bibliothek geladen wird?](images/fig1.png)

## <a name="general-best-practices"></a>Allgemeine bewährte Methoden

[**DllMain**](dllmain.md) wird aufgerufen, während die Loadersperre gehalten wird. Daher gelten erhebliche Einschränkungen für die Funktionen, die in **DllMain aufgerufen werden können.** Daher ist **DllMain** so konzipiert, dass minimale Initialisierungsaufgaben mithilfe einer kleinen Teilmenge der Microsoft® Windows®-API ® Windows® werden. Sie können keine Funktion in **DllMain** aufrufen, die direkt oder indirekt versucht, die Ladesperre zu erhalten. Andernfalls besteht die Möglichkeit, dass Ihre Anwendung deadlocks oder abstürzt. Ein Fehler in einer **DllMain-Implementierung** kann den gesamten Prozess und alle seine Threads gefährden.

Die ideale [**DllMain wäre**](dllmain.md) nur ein leerer Stub. Angesichts der Komplexität vieler Anwendungen ist dies jedoch im Allgemeinen zu restriktiv. Eine gute Faustregel für **DllMain ist** die möglichst lange Initialisierung. Die verzögerte Initialisierung erhöht die Stabilität der Anwendung, da diese Initialisierung nicht ausgeführt wird, während die Ladesperre gehalten wird. Außerdem können Sie mithilfe der verzögerten Initialisierung einen größeren Teil der API sicher Windows verwenden.

Einige Initialisierungsaufgaben können nicht zurückgestellt werden. Beispielsweise sollte eine DLL, die von einer Konfigurationsdatei abhängt, nicht geladen werden, wenn die Datei falsch formatiert ist oder eine Garbage Collection enthält. Bei dieser Art der Initialisierung sollte die DLL die Aktion schnell versuchen und schnell fehlschlagen, anstatt Ressourcen zu verschwenden, indem andere Aufgaben abgeschlossen werden.

Sie sollten niemals die folgenden Aufgaben in [**DllMain ausführen:**](dllmain.md)

-   Rufen [**Sie LoadLibrary oder**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) auf (entweder direkt oder indirekt). Dies kann zu einem Deadlock oder abstürzen.
-   Rufen [**Sie GetStringTypeA,**](/windows/desktop/api/winnls/nf-winnls-getstringtypea) [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)oder [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) (entweder direkt oder indirekt) auf. Dies kann zu einem Deadlock oder abstürzen.
-   Synchronisieren mit anderen Threads. Dies kann zu einem Deadlock führen.
-   Erwerben Sie ein Synchronisierungsobjekt, das sich im Besitz von Code befindet, der darauf wartet, die Ladesperre zu erhalten. Dies kann zu einem Deadlock führen.
-   Initialisieren Sie COM-Threads [**mithilfe von CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Unter bestimmten Bedingungen kann diese Funktion [**LoadLibraryEx aufrufen.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   Rufen Sie die Registrierungsfunktionen auf. Diese Funktionen werden in der Advapi32.dll. Wenn Advapi32.dll dll nicht initialisiert wird, kann die DLL auf nicht initialisierten Arbeitsspeicher zugreifen und den Prozess zum Absturz führen.
-   Rufen Sie [**CreateProcess auf.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Beim Erstellen eines Prozesses kann eine andere DLL geladen werden.
-   Rufen Sie [**ExitThread auf.**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) Das Beenden eines Threads während der DLL-Trennung kann dazu führen, dass die Ladesperre erneut aufgerufen wird, was zu einem Deadlock oder einem Absturz führt.
-   Rufen Sie [**CreateThread auf.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) Das Erstellen eines Threads kann funktionieren, wenn Sie keine Synchronisierung mit anderen Threads ausführen, aber es ist riskant.
-   Erstellen Sie eine Named Pipe oder ein anderes benanntes Objekt (nur Windows 2000). In Windows 2000 werden benannte Objekte von der Terminaldienste-DLL bereitgestellt. Wenn diese DLL nicht initialisiert ist, können Aufrufe der DLL zum Absturz des Prozesses führen.
-   Verwenden Sie die Speicherverwaltungsfunktion aus der dynamischen C Run-Time (CRT). Wenn die CRT-DLL nicht initialisiert ist, können Aufrufe dieser Funktionen zum Absturz des Prozesses führen.
-   Aufrufen von Funktionen in User32.dll oder Gdi32.dll. Einige Funktionen laden eine andere DLL, die möglicherweise nicht initialisiert wird.
-   Verwenden Sie verwalteten Code.

Die folgenden Aufgaben sind in **DllMain sicher** auszuführen:

-   Initialisieren Sie statische Datenstrukturen und Member zur Kompilierzeit.
-   Erstellen und Initialisieren von Synchronisierungsobjekten.
-   Zuordnen von Arbeitsspeicher und Initialisieren dynamischer Datenstrukturen (Vermeiden der oben aufgeführten Funktionen)
-   Einrichten des lokalen Threadspeichers (TLS).
-   Öffnen, Lesen aus und Schreiben in Dateien.
-   Rufen Sie Funktionen in Kernel32.dll auf (mit Ausnahme der oben aufgeführten Funktionen).
-   Legen Sie globale Zeiger auf NULL fest, um die Initialisierung dynamischer Member zu deaktivieren. In Microsoft Windows Vista™ können Sie die einmaligen Initialisierungsfunktionen verwenden, um sicherzustellen, dass ein Codeblock nur einmal in einer Multithreadumgebung ausgeführt wird.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Deadlocks, die durch die Umkehrung der Sperr reihenfolge verursacht werden

Wenn Sie Code implementieren, der mehrere Synchronisierungsobjekte wie Sperren verwendet, ist es wichtig, die Reihenfolge der Sperren zu achten. Wenn es erforderlich ist, mehr als eine Sperre gleichzeitig zu erhalten, müssen Sie eine explizite Rangfolge definieren, die als Sperrhierarchie oder Sperrfolge bezeichnet wird. Wenn z. B. Sperre A vor Sperre B im Code und Sperre B an anderer Stelle im Code vor Sperre C erhalten wird, ist die Sperr reihenfolge A, B, C, und diese Reihenfolge sollte im gesamten Code befolgt werden. Die Umkehrung der Sperr reihenfolge tritt auf, wenn die Sperr reihenfolge nicht eingehalten wird, z. B. wenn Sperre B vor Sperre A übernommen wird. Die Umkehrung der Sperr reihenfolge kann Deadlocks verursachen, die schwer zu debuggen sind. Um solche Probleme zu vermeiden, müssen alle Threads Sperren in der gleichen Reihenfolge erhalten.

Beachten Sie, dass das Lader [**DllMain**](dllmain.md) mit der bereits erworbenen Loadersperre aufruft, sodass die Ladersperre in der Sperrhierarchie die höchste Priorität haben sollte. Beachten Sie außerdem, dass Code nur die Sperren erhalten muss, die für eine ordnungsgemäße Synchronisierung erforderlich sind. Er muss nicht jede einzelne Sperre erhalten, die in der Hierarchie definiert ist. Wenn ein Codeabschnitt z. B. nur A und C für eine ordnungsgemäße Synchronisierung sperrt, sollte der Code Sperre A erhalten, bevor er Sperre C erhält. Es ist nicht erforderlich, dass der Code auch Sperre B erhält. Darüber hinaus kann dll-Code die Ladesperre nicht explizit erhalten. Wenn der Code eine API wie [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) aufrufen muss, die indirekt die Ladesperre abrufen kann, und der Code auch eine private Sperre abrufen muss, sollte der Code **GetModuleFileName** aufrufen, bevor er die Sperre P abruft, um sicherzustellen, dass die Lade reihenfolge eingehalten wird.

Abbildung 2 ist ein Beispiel, das die Umkehrung der Sperr reihenfolge veranschaulicht. Stellen Sie sich eine DLL vor, deren Hauptthread [**DllMain enthält.**](dllmain.md) Das Bibliotheklader ruft die Loadersperre L ab und ruft dann **dllMain auf.** Der Hauptthread erstellt die Synchronisierungsobjekte A, B und G, um den Zugriff auf seine Datenstrukturen zu serialisieren, und versucht dann, Sperre G zu erhalten. Ein Arbeitsthread, der die Sperre G bereits erfolgreich erhalten hat, ruft dann eine Funktion wie GetModuleHandle auf, die versucht, die Loadersperre L zu erhalten. Daher wird der Arbeitsthread auf L und der Hauptthread auf G blockiert, was zu einem Deadlock führt.

![Deadlock, der durch eine Umkehrung der Sperr reihenfolge verursacht wird](images/fig2.png)

Um Deadlocks zu verhindern, die durch die Umkehrung der Sperr reihenfolge verursacht werden, sollten alle Threads jederzeit versuchen, Synchronisierungsobjekte in der definierten Lade reihenfolge zu erhalten.

## <a name="best-practices-for-synchronization"></a>Bewährte Methoden für die Synchronisierung

Stellen Sie sich eine DLL vor, die Arbeitsthreads als Teil der Initialisierung erstellt. Bei der DLL-Bereinigung ist es erforderlich, mit allen Arbeitsthreads zu synchronisieren, um sicherzustellen, dass sich die Datenstrukturen in einem konsistenten Zustand befinden, und dann die Arbeitsthreads zu beenden. Heutzutage gibt es keine einfache Möglichkeit, das Problem der sauberen Synchronisierung und des Herunterfahrens von DLLs in einer Multithreadumgebung vollständig zu lösen. In diesem Abschnitt werden die aktuellen bewährten Methoden für die Threadsynchronisierung beim Herunterfahren der DLL beschrieben.

Threadsynchronisierung in [**DllMain beim**](dllmain.md) Beenden des Prozesses

-   Wenn [**DllMain**](dllmain.md) beim Beenden des Prozesses aufgerufen wird, wurden alle Threads des Prozesses erzürnt bereinigt, und es besteht die Möglichkeit, dass der Adressraum inkonsistent ist. In diesem Fall ist keine Synchronisierung erforderlich. Anders ausgedrückt: Der ideale DLL \_ PROCESS \_ DETACH-Handler ist leer.
-   Windows Vista stellt sicher, dass sich Kerndatenstrukturen (Umgebungsvariablen, aktuelles Verzeichnis, Prozesshap und so weiter) in einem konsistenten Zustand befinden. Andere Datenstrukturen können jedoch beschädigt werden, sodass das Bereinigen des Speichers nicht sicher ist.
-   Der persistente Zustand, der gespeichert werden muss, muss in den permanenten Speicher geleert werden.

Threadsynchronisierung in **DllMain für** DLL \_ THREAD DETACH während des \_ DLL-Entladens

-   Wenn die DLL entladen wird, wird der Adressraum nicht verworfen. Daher wird von der DLL erwartet, dass sie ein sauberes Herunterfahren durchführen kann. Dazu gehören Threadsynchronisierung, offene Handles, persistenter Zustand und zugeordnete Ressourcen.
-   Die Threadsynchronisierung ist schwierig, da das Warten auf Threads, die in [**DllMain**](dllmain.md) beendet werden, zu einem Deadlock führen kann. Dll A enthält z. B. die Ladesperre. Sie signalisiert Thread T zum Beenden und wartet, bis der Thread beendet wird. Thread T wird beendet, und das Lader versucht, die Ladesperre zum Aufrufen von **DllMain** von DLL A mit DLL \_ THREAD DETACH zu \_ erhalten. Dies führt zu einem Deadlock. So minimieren Sie das Risiko eines Deadlocks:
    -   DLL A ruft eine \_ DLL-THREAD \_ DETACH-Meldung in ihrer [**DllMain**](dllmain.md) ab und legt ein Ereignis für Thread T fest, das das Beenden signalisiert.
    -   Thread T beendet seine aktuelle Aufgabe, bringt sich in einen konsistenten Zustand, signalisiert DLL A und wartet unendlich. Beachten Sie, dass die Konsistenzprüfungsroutinen dieselben Einschränkungen wie [**DllMain**](dllmain.md) befolgen sollten, um Deadlocks zu vermeiden.
    -   DLL A beendet T in dem Wissen, dass sie sich in einem konsistenten Zustand befindet.

Wenn eine DLL entladen wird, nachdem alle Threads erstellt wurden, aber bevor sie mit der Ausführung beginnen, können die Threads abstürzen. Wenn die DLL threads in ihrer **DllMain** im Rahmen ihrer Initialisierung erstellt hat, sind einige Threads möglicherweise nicht abgeschlossen, und ihre \_ DLL-THREAD ATTACH-Nachricht wartet weiterhin darauf, an die DLL übermittelt zu \_ werden. Wenn die DLL in diesem Fall entladen wird, beginnt sie mit dem Beenden von Threads. Einige Threads können jedoch hinter der Ladesperre blockiert werden. Ihre DLL \_ THREAD ATTACH-Meldungen werden verarbeitet, nachdem die DLL nicht zugeordnet wurde, was \_ zum Absturz des Prozesses führt.

## <a name="recommendations"></a>Empfehlungen

Die folgenden Richtlinien werden empfohlen:

-   Verwenden Application Verifier, um die häufigsten Fehler in [**DllMain zu erkennen.**](dllmain.md)
-   Wenn Sie eine private Sperre in [**DllMain verwenden,**](dllmain.md)definieren Sie eine Sperrhierarchie, und verwenden Sie sie konsistent. Die Loadersperre muss sich am unteren Rand dieser Hierarchie befinden.
-   Stellen Sie sicher, dass keine Aufrufe von einer anderen DLL abhängen, die möglicherweise noch nicht vollständig geladen wurde.
-   Führen Sie einfache Initialisierungen statisch zur Kompilierzeit und nicht in [**DllMain aus.**](dllmain.md)
-   Verzögerung von Aufrufen in [**DllMain,**](dllmain.md) die bis zu einem späteren Zeitpunkt warten können.
-   Verzögerung von Initialisierungsaufgaben, die bis zu einem späteren Zeitpunkt warten können. Bestimmte Fehlerbedingungen müssen frühzeitig erkannt werden, damit die Anwendung Fehler ordnungsgemäß behandeln kann. Es gibt jedoch Vor- und Abeinbußen zwischen dieser frühen Erkennung und dem Verlust der Stabilität, die sich daraus ergeben können. Das Zurückverenden der Initialisierung ist häufig am besten.

 

 
