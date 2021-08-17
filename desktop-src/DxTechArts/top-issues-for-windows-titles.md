---
title: Top Issues for Windows Titles (Hauptprobleme bei Windows Titeln)
description: In diesem Artikel werden viele der häufigen Probleme erläutert, die wir in PC-Spielen der aktuellen Generation festgestellt haben.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89be8ad7a68c247d589f304ea77fa9b3e63e105739264e39f71794c705b66cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396505"
---
# <a name="top-issues-for-windows-titles"></a>Top Issues for Windows Titles (Hauptprobleme bei Windows Titeln)

Die Gruppe Microsoft Windows Gaming and Graphics Technologies Developer Relations führt jedes Jahr eine Leistungsanalyse für viele Windows Spiele durch. Während dieser Sitzungen erhalten wir praktische Erfahrungen, um das Feedback und die Abfragen von Entwicklern zu verknüpfen, die wir täglich erhalten. Gelegentlich helfen wir bei der Aufspürung eines zerstürzten Absturzes oder eines anderen Problems in einem Titel, der uns weitere Einblicke in Probleme bietet, auf die Entwickler stoßen.

In diesem Artikel werden viele der häufigen Probleme erläutert, die wir in PC-Spielen der aktuellen Generation festgestellt haben.

-   [CPU-eingeschränkte Leistung](#cpu-limited-performance)
-   [Schlechte Batchverwaltung](#poor-batch-management)
-   [Übermäßiges Kopieren von Arbeitsspeicher](#excessive-memory-copying)
-   [Übermäßige Verwendung der dynamischen Draw-Übermittlung](#excessive-use-of-dynamic-draw-submission)
-   [Hoher Mehraufwand bei der Dateiverarbeitung](#high-overhead-in-file-processing)
-   [Langsame und frustrierende Installation](#slow-and-frustrating-installation)
-   [Fehlende Berücksichtigung des physischen Arbeitsspeichers](#lack-of-consideration-of-physical-memory)
-   [Übermäßige Abhängigkeit von Real-Time Konvertierung der Audioabtastrate](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Fragmentierung des virtuellen Arbeitsspeichers](#fragmention-of-virtual-memory)
-   [Bearbeitung des wortgesteuerten Floating-Point-Steuerelements](#manipulation-of-the-floating-point-control-word)
-   [Optionale Installation der DirectX-Runtime](#optional-installation-of-the-directx-runtime)
-   [Übermäßige Verwendung der Threadsynchronisierung](#excessive-use-of-thread-synchronization)
-   [Verwendung von RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>CPU-Limited Leistung

Die überwiegende Mehrheit der Spiele wird durch die CPU-Leistung auf Systemen mit leistungsstarken Grafikprozessoren (GPUs) eingeschränkt. Dies liegt manchmal an der schlechten Verwendung der Batchverarbeitung für Draw-Übermittlungen, aber in der Regel liegt dies daran, dass andere Spielsysteme einen großen Teil der verfügbaren CPU-Zyklen verbrauchen. In den wenigen Fällen, in denen die GPU als Einschränkung angesehen wurde, liegt die Ursache in sehr hohen Füllraten oder der Pixel-Shader-Nachfrage, in Einstellungen mit hoher Auflösung oder in einer niedrigen Vertex-Shaderleistung durch eine Grafikkarte.

Da die meisten Titel CPU-begrenzt sind, ergeben sich die größten Leistungsgewinne aus der Optimierung CPU-intensiver Spielsysteme. In der Regel sind die KI- oder Physikalischen Systeme und die zugehörige Kollisionserkennungslogik die primären Consumer von CPU-Zyklen in gut funktionierenden Microsoft Direct3D-Anwendungen. Jede Arbeit zur Verbesserung dieser Systeme kann die Gesamtleistung des Spiels verbessern.

## <a name="poor-batch-management"></a>Schlechte Batchverwaltung

Um eine gute Parallelität mit der GPU zu erreichen, müssen Draw-Batches genügend Geometrie enthalten – und die Shader haben die richtige Komplexität –, um die Grafikkarte ausgelastet zu halten, ohne so viele Batches zu verwenden, dass der Befehlspuffer überflutet wird. Auf Hardware der aktuellen Generation empfehlen wir ungefähr 300 oder weniger Drawbatchübermittlungen pro Frame (weniger bei CPUs mit geringerer Leistung), um zu verhindern, dass die Verarbeitung des Befehlspuffers durch den Treiber zu einem Leistungsengpass wird. Einige andere API-Zustandsaufrufe und Treiberkombinationen können zu kostspieliger CPU-Verarbeitung führen (z. B. treiberkompilieren von Shadern), daher wird dringend empfohlen, routinemäßige Leistungsanalysen durchzuführen.

## <a name="excessive-memory-copying"></a>Übermäßiges Kopieren von Arbeitsspeicher

Während der Entwicklung der meisten PC-Titel verwenden Entwickler praktische Datenstrukturen und Zeichenfolgen für die Inhaltsverwaltung. Die CPU-Arbeit, die für zeichenfolgenvergleichs-, kopier- und andere Manipulationen erforderlich ist, hat häufig einen messbaren Mehraufwand, insbesondere unter Berücksichtigung der Leistungstreffer, die dem Cache- und Speichersubsystem zugeordnet sind. Bei der Entwicklung dieser Systeme sollten Pläne getroffen werden, um die Abhängigkeit von der Zeichenfolgenverarbeitung zu beseitigen oder zu minimieren, sobald das Produkt in die primären Test- und Releasephasen eintritt.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Übermäßige Verwendung der dynamischen Draw-Übermittlung

Moderne Videohardware bietet eine gute Leistung beim Umgang mit statischen Daten. High-End-Adapter verfügen häufig über eine sehr große Menge an Videospeicher, aber dieser Arbeitsspeicher kann nicht effektiv von dynamischen Daten genutzt werden.

Zwar können einigermaßen effiziente Verwendungsmuster von dynamischen Scheitelpunktpuffern/Indexpuffern für dynamischen Inhalt implementiert werden, aber viele Titel überverwenden dieses Idioma für den ansonsten statischen Inhalt. Dies wird am häufigsten bei BSP-Strukturen (Binary Space Partitioning) und portalbasierten Systemen angezeigt, die Geometrie in einer Datenstruktur speichern, die nicht der Hardware zugeordnet ist und in Puffern für jeden Frame verarbeitet werden muss. Wenn Sie so viel Inhalt wie möglich in statische Ressourcen integrieren, kann der Bandbreitenaufwand für die Übertragung von Daten auf die Grafikkarte erheblich reduziert werden, die Verwendung des integrierten VRAM verbessert und der CPU-/Cacheaufwand für die Verarbeitung dieses Inhalts reduziert werden.

## <a name="high-overhead-in-file-processing"></a>Hoher Mehraufwand bei der Dateiverarbeitung

PC-Spiele haben einen Ruf für lange Ladezeiten erlangt, insbesondere im Vergleich zu Konsolentiteln mit strengen Ladezeitanforderungen. Unsere Analyse der Art und Weise, wie viele Titel das Dateisubsystem verwenden, zeigt einige häufige Probleme.

Der Aufwand für das Öffnen einer Datei ist in der Regel viel höher als von Entwicklern erwartet. Bei bedarfsorientierten Virenscannern, die weit verbreitet sind, und der zusätzlichen Funktionalität von NTFS ist das Öffnen einer Datei ein ziemlich kostspieliger Vorgang. Das gleichzeitige Öffnen vieler Dateien oder das wiederholte Öffnen und Schließen derselben Datei ist daher eine schlechte Methode für die Dateiverwaltung. Einige Spiele haben versucht, diese Leistungskosten zu verringern, indem sie das Vorhandensein einer Datei vor dem Öffnen getestet haben. Die Realität ist, dass das Testen auf das Vorhandensein einer Datei auf NTFS das Öffnen der Datei erfordert, sodass das Testen vor dem Öffnen dazu führt, dass die Kosten zweimal bezahlt werden.

Spiele, die Add-On-Änderungen oder Mods zulassen oder noch Entwicklungsgerüste enthalten, um zu überprüfen, ob Datendateien überschrieben werden, können erhebliche Verzögerungen beim Laden des Spiels verursachen, da diese Dateien überprüft werden, auch wenn diese Dateien nicht vorhanden sind. Es wird empfohlen, dass Spiele diese Dateien nur überprüfen, wenn sie mit einem speziellen Befehlszeilenschalter oder einem anderen Modusindikator ausgeführt werden, sodass nur die Benutzer, die diese Funktionalität nutzen, tatsächlich die Leistungskosten dieser (häufig umfangreichen) Überprüfungen bezahlen.

Zusätzliche Leistung kann aus dem Dateisystem wie folgt abgerufen werden:

-   Geeignete Verwendung der Dateisystemhinweise FILE \_ FLAG RANDOM ACCESS und FILE FLAG SEQUENTIAL \_ \_ \_ \_ \_ SCAN
-   Dimensionieren von Puffern, um eine große Anzahl von Aufrufen der Lese-/Schreib-APIs des Betriebssystems zu vermeiden
-   Asynchroner Zugriff auf Dateien
-   Laden von Threads im Hintergrund

Außerdem wird dringend empfohlen, Daten offline zu konvertieren (zur Build- oder Installationszeit), anstatt sich auf die Konvertierung zu verlassen, wenn das Spiel zum ersten Mal ausgeführt wird, da dies eine erhebliche Leistungssteuer für jeden Benutzer mit sich bringt.

## <a name="slow-and-frustrating-installation"></a>Langsame und frustrierende Installation

Ein weiteres häufiges Problem, das wir gesehen haben, sind sehr lange Installationszeiten, die für viele moderne PC-Spiele erforderlich sind. Die Installationsprogramme fordern den Benutzer mehrmals auf, manchmal einfach, dem Benutzer mitzuteilen, z. B. "DirectX muss nicht installiert sein". Im Allgemeinen erfordern diese fehlerhaften Installationsprogramme, dass der Benutzer mehrmals **Weiter** oder **OK** auswählt, bevor die Installation des Spiels tatsächlich beginnt. Sobald er beginnt, haben wir gesehen, dass einige Titel eine Stunde oder mehr dauern, bevor der Benutzer die Möglichkeit erhält, das Spiel zu spielen. Wir sind der festen Meinung, dass die erste Stunde der Spielerfahrung nicht die Installation sein sollte.

Wir empfehlen eine Reihe von Ansätzen für den Umgang mit der Installation. Halten Sie zunächst die Eingabeaufforderungen einfach und auf ein Minimum. Zweitens: Entwerfen Sie Ihre Spieldaten so, dass einige oder alle Datendateien nach Möglichkeit direkt vom Verteilungsdatenträger verwendet werden können – moderne DVD-Laufwerke haben eine sehr hohe Bandbreite. Drittens: Erwägen Sie die Implementierung von Install-on-Demand in Ihren Titeln, um den Installationsprozess zu reduzieren oder zu beseitigen und Benutzern so schnell wie möglich das Spiel zu ermöglichen. (Weitere Informationen zur Bedarfsinstallation finden Sie unter [Install-on-Demand for Games](/windows/desktop/DxTechArts/install-on-demand-for-games).)

Weitere Empfehlungen zur Spieleinstallation finden Sie unter [Simplifying Game Installation](/windows/desktop/DxTechArts/simplifying-game-installation).

## <a name="lack-of-consideration-of-physical-memory"></a>Fehlende Berücksichtigung des physischen Arbeitsspeichers

Aufgrund der großen Variabilität der PC-Hardware auf dem Markt verwenden Titel in der Regel Ad-hoc-Konfigurationstests, um Standardeinstellungen für die Ebene der grafischen Details auszuwählen. Einige der Titel, die wir gesehen haben, verwenden die Videospeichergröße in diesen Tests, aber dies kann nicht mit der Größe des physischen Arbeitsspeichers korreliert werden. Um Situationen mit verlorenen Geräten zu behandeln, muss der Großteil des Videospeichers (sowohl lokales VRAM auf der Karte als auch die nicht lokale AGP-Speicherperpertur) durch physischen Speicher gesichert werden, entweder durch die Verwendung verwalteter Ressourcen oder benutzerdefinierter Datenstrukturen. Einige High-End-Grafikkarten verfügen über VRAM-Größen, die die Größe der Low-End-CPU-Speicher beanspruchen. In Situationen, in denen das System im Vergleich zur Grafikkarte nur über eingeschränkten physischen Arbeitsspeicher verfügt, kann der großteil dieser VRAM nicht effektiv genutzt werden, und es sollten niedrigere Detaileinstellungen konfiguriert werden.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Over-Reliance zur Konvertierung der Real-Time Audio sample rate

Eine weitere häufige Quelle für cpu cycle burn tritt auf, wenn das Audiosystem erforderlich ist, um die Wiedergaberate während der Mischung in den Hardwarepuffer zu konvertieren. Bei WDM-Treibern (Windows Driver Model) wird das Hardwarepufferformat nicht direkt von der Anwendung gesteuert, da es sich um eine Ressource auf Kernelebene handelt. Stattdessen wird das Format basierend auf dem Format mit der höchsten Qualität aller Quellen und den Funktionen der Hardware ausgewählt. Standardmäßig verwendet Windows XP eine qualitativ hochwertige Abtastratenkonvertierung für diesen Prozess. Wenn die Mehrheit der Audiobeispiele eine Ratenkonvertierung erfordert, wird ein erheblicher Teil der CPU-Zyklen verbraucht.

Es wird empfohlen, alle DirectSound-Puffer mit der gleichen Abtastrate zu erstellen. Wenn Sie Microsoft Win32 **WaveOut-Funktionen** verwenden, sollten Sie auch mit diesen eine konsistente Abtastrate verwenden. Bei WDM-Treibern werden die Puffer alle vom Kernel gemischt, und wenn Sie eine höhere Samplingrate für einige davon verwenden, werden die Stichprobenraten aller übrigen Werte entsprechend konvertiert. Beachten Sie, dass dies die Verwendung derselben Wiedergaberate für alle Audiobeispiele impliziert, einschließlich aller Streaming-Audiodekomprimierungspuffer. Das Festlegen der primären Pufferrate hat keine Auswirkungen, es sei denn, Sie legen Windows 98 oder Windows Edition fest.

> [!Note]  
> Auf Windows Vista und neueren Versionen des Betriebssystems verwenden DirectSound und **waveOut** die [Windows Audio Session API (WASAPI)](/windows/desktop/CoreAudio/wasapi) für alle Audioausgaben.

 

## <a name="fragmention-of-virtual-memory"></a>Fragmentierung des virtuellen Arbeitsspeichers

Wir haben eine Reihe kürzlich auftretender Probleme im Zusammenhang mit dem 32-Bit-Limit für den Prozessspeicherplatz festgestellt. Obwohl 2 GB des virtuellen Adressraums für Benutzermodusprozesse in der Vergangenheit mehr als ausreichend waren, hat die zunehmende Verwendung großer speicherzuordnungsbasierter Dateien, benutzerdefinierter Speicherbelegungen und der zunehmenden VRAM-Größe (die dem Prozessspeicher zugeordnet werden müssen) zu Situationen führt, in denen die Zuordnung des virtuellen Arbeitsspeichers fehlschlägt. Einige Nicht-Microsoft-DLLs verwenden Feste Startspeicherorte in der Mitte des virtuellen Adressraums, was zu Fragmentierung führt, die zu fehlerhaften Zuordnungen führt.

Diese Probleme treten am häufigsten auf, wenn das Spiel ein benutzerdefiniertes Speicherbelegungsschema verwendet, das versucht, einen großen fortlaufenden Teil des virtuellen Speicherplatzes zuzuordnen. Es wird empfohlen, Zuweisungen so zu schreiben, dass sie bei Bedarf einen Teil des virtuellen Adressraums mit einer angemessenen Größe anfordern. Beispielsweise können Sie 64 oder 256 MB gleichzeitig anfordern, aber nicht 1 GB. Es sollte jedoch darauf geachtet werden, dass keine weitere Fragmentierung verursacht wird. Die Einführung von 64-Bit-Betriebssystemen und -Hardware wird diesen Problemen in Zukunft sehr helfen, aber bei 32-Bit-Systemen der aktuellen Generation muss vorsichtshalber berücksichtigt werden.

## <a name="manipulation-of-the-floating-point-control-word"></a>Bearbeitung des wortgesteuerten Floating-Point-Steuerelements

Als Debughilfe haben einige Entwickler Ausnahmen für die Gleitkommaeinheit (Floating Point Unit, FPU) über Manipulationen des Gleitkommasteuerworts aktiviert. Dies ist äußerst problematisch und führt wahrscheinlich dazu, dass der Prozess abstürzt. Genau wie die Aufrufkonvention erfordert, dass das ebx-Register beibehalten wird, geht der Großteil des Systems davon aus, dass sich die FPU im Standardzustand befindet, liefert sinnvolle Ergebnisse und generiert keine Ausnahmen. Treiber und andere Systemkomponenten berechnen Ergebnisse häufig basierend auf der Annahme, dass Standardfehlerwerte in den Registern für ungültige Bedingungen angezeigt werden. Wenn jedoch Ausnahmen aktiviert sind, werden diese nicht behandelt und führen zu Abstürzen.

Direct3D legt die Gleitkommaeinheit im Rahmen der Initialisierung für den aufrufenden Thread auf "Round-to-Nearest" mit einfacher Genauigkeit fest, es sei denn, das FPU PRESERVE-Flag D3DCREATE \_ \_ wird verwendet. In diesem Fall ist das Gleitkommasteuerwort unverändert. Da es sich bei dem Steuerwort um eine Threadeinstellung handelt, kann die Leistung optimiert werden, wenn sichergestellt wird, dass alle Anwendungsthreads auf den Modus mit einmaliger Genauigkeit festgelegt sind. Denken Sie daran, dass das Aufrufen von [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) für x64-native Codierung nicht gültig ist, bei der stattdessen ausschließlich SSE verwendet wird, und dass es für die PowerPC-basierte Architektur der Xbox 360-CPU äußerst teuer ist.

> [!Note]  
> Wenn Sie das Steuerelementwort ändern, verwenden Sie [**\_ controlfp \_ s,**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) und beachten Sie, dass Sie für x64-Plattformen die Gleitkommagenauigkeit nicht über das Steuerwort ändern können.

 

In allen Bibliotheken, in denen wir unterschiedliche Rundungsregeln oder anderes Verhalten benötigen , z. B. im Umgang mit Softwarevertex-Shadern oder Kompilierung, speichern und stellen wir das Steuerwort wiederher. Wenn ein Spiel nicht standardmäßige Rundungs- oder FPU-Ausnahmen verwenden muss, sollte es das Gleitkommasteuerwort speichern und wiederherstellen, und Sie sollten sicherstellen, dass es keinen externen Code aufruft, der sich nicht als sicher vor diesen Problemen erwiesen hat, einschließlich System-APIs.

## <a name="optional-installation-of-the-directx-runtime"></a>Optionale Installation der DirectX-Runtime

Eine Reihe von Spielen fragt den Benutzer, ob DirectX installiert werden soll. Dies kann zu Problemen führen, wenn der Benutzer davon ausgegangen wird, dass auf dem System die neueste verteilbare DirectX-Version installiert ist, die Installation übersprungen wird. Anschließend wird die Installation erfolgreich fortgesetzt. Wenn das Spiel eine bestimmte Version von D3DX oder andere aktualisierte Funktionen erfordert, die nicht installiert wurden, funktioniert das Spiel nicht, und der Benutzer wird sehr frustriert.

Es wird dringend empfohlen, dass das Installationsprogramm des Spiels im Hintergrund die DirectX Redistributable installiert, für die das Spiel erstellt wurde. Der DirectX-Installationsvorgang ist so konzipiert, dass überprüft wird, ob etwas aktualisiert werden muss, und wenn dies nicht der Wert ist, wird er schnell zurückgegeben. Daher ist es nicht notwendig, den Benutzer nach der Installation von DirectX zu fragen.

Eine automatische Installation von DirectX kann durchgeführt werden, indem Sie den folgenden Befehl in Ihrem Installationspaket ausführen: **dxsetup.exe /silent**

Darüber hinaus kann die tatsächliche Größe des verteilbaren Ordners so konfiguriert werden, dass nur die Schränkdateien (.cab) enthalten sind, die tatsächlich für die Zielplattformen und die Verwendung des Spiels benötigt werden.

> [!Note]  
> Bevor Sie **dxsetup verwenden,** lesen Sie [Nicht so Direct Setup](https://walbourn.github.io/).

 

## <a name="excessive-use-of-thread-synchronization"></a>Übermäßige Verwendung der Threadsynchronisierung

Bei der Profilerstellung von Spielen stehen die wichtigsten Hotspots häufig im Zusammenhang mit dem Ein- und Verlassen kritischer Abschnitte. Mit der Einführung von CPUs mit mehreren Kernen hat sich die Verwendung von Multithreading in Spielen erheblich erhöht, und viele Implementierungen basieren auf starker Verwendung der Threadsynchronisierung. Die CPU-Zeit, einen kritischen Abschnitt auch ohne Jegliches Zueinander in Anspruch zu nehmen, ist sehr wichtig, und alle anderen Formen der Threadsynchronisierung sind noch teurer. Daher muss darauf achten, die Verwendung dieser Primitive zu minimieren.

Eine häufige Quelle für übermäßige Synchronisierung in Spielen ist die Verwendung von [D3DCREATE \_ MULTITHREADED](/windows/desktop/direct3d9/d3dcreate). Dieses Flag macht Direct3D zwar threadsicher für das Rendern aus mehreren Threads, verfolgt jedoch einen sehr konservativen Ansatz, was zu einem hohen Synchronisierungsaufwand führt. Spiele sollten dieses Flag vermeiden. Erstellen Sie stattdessen die Engine so, dass die gesamte Kommunikation mit Direct3D von einem einzelnen Thread erfolgt und die Kommunikation zwischen Threads direkt verarbeitet wird. Weitere Informationen zum Entwerfen von Multithread-Spielen finden Sie im Artikel [Coding For Multiple Cores on](/windows/desktop/DxTechArts/coding-for-multiple-cores)Xbox 360 and Microsoft Windows .

## <a name="use-of-rdtsc"></a>Verwendung von RDTSC

Die Verwendung der x86-Anweisung **RDTSC** wird nicht empfohlen. **RDTSC** kann die Zeitsteuerung für einige Energieverwaltungsschemas, die die CPU-Frequenz dynamisch ändern, und für viele CPUs mit mehreren Kernen, für die der Zykluszähler nicht zwischen Kernen synchronisiert wird, nicht ordnungsgemäß berechnen. Spiele sollten stattdessen die [**QueryPerformanceCounter-API**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) verwenden. Weitere Informationen zu Problemen mit **RDTSC** und zur Implementierung einer zeitaufge40000 auflösungsbasierten Zeitsteuerung mit **QueryPerformanceCounter** finden Sie im Artikel Game Timing and Multicore Processors (Game Timing und [Mehrkernprozessoren).](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)

 

 