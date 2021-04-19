---
title: Top-Probleme bei Windows-Titeln
description: In diesem Artikel werden viele der häufigen Probleme hervorgehoben, die in den PC-Spielen der aktuellen Generation aufgetreten sind.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547c977f7d8e4895ef73ba229a9012854a7c6d27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339899"
---
# <a name="top-issues-for-windows-titles"></a>Top-Probleme bei Windows-Titeln

Die Entwickler Beziehungsgruppe Microsoft Windows Gaming and graphics Technologies führt die Leistungsanalyse für viele Windows-Spiele jedes Jahr aus. In diesen Sitzungen erhalten wir praktische Erfahrungen mit dem Feedback und den Abfragen des Entwicklers, die wir täglich erhalten. Gelegentlich ist es hilfreich, einen mysteriösen Absturz oder ein anderes Problem in einem Titel aufzuspüren, der uns einen besseren Einblick in Probleme bietet, auf die sich Entwickler stoßen.

In diesem Artikel werden viele der häufigen Probleme hervorgehoben, die in den PC-Spielen der aktuellen Generation aufgetreten sind.

-   [Eingeschränkte CPU-Leistung](#cpu-limited-performance)
-   [Schlechte Batch Verwaltung](#poor-batch-management)
-   [Übermäßige Speicher Kopiervorgänge](#excessive-memory-copying)
-   [Übermäßige Verwendung der dynamischen zeichnen-Übermittlung](#excessive-use-of-dynamic-draw-submission)
-   [Hoher Aufwand bei der Dateiverarbeitung](#high-overhead-in-file-processing)
-   [Langsame und frustrierende Installation](#slow-and-frustrating-installation)
-   [Fehlende Berücksichtigung des physischen Speichers](#lack-of-consideration-of-physical-memory)
-   [Übermäßige Abhängigkeit von Real-Time audiostichproben-Raten Konvertierung](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Fragnenangabe des virtuellen Speichers](#fragmention-of-virtual-memory)
-   [Bearbeitung des Floating-Point Steuer Worts](#manipulation-of-the-floating-point-control-word)
-   [Optionale Installation der DirectX-Laufzeit](#optional-installation-of-the-directx-runtime)
-   [Übermäßige Verwendung der Thread Synchronisierung](#excessive-use-of-thread-synchronization)
-   [Verwendung von RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>CPU-Limited Leistung

Die große Mehrheit der Spiele ist durch die CPU-Leistung auf Systemen mit hochleistungsfähigen Grafik Verarbeitungseinheiten (GPUs) beschränkt. Dies ist manchmal auf eine schlechte Verwendung der Batch Verarbeitung für zeichnen-Übermittlungen zurückzuführen, aber in der Regel ist dies auf andere Spielsysteme zurückzuführen, die einen großen Teil der verfügbaren CPU-Zyklen beanspruchen. In den wenigen Fällen, in denen die GPU als Einschränkung angesehen wurde, ist die Ursache sehr hoch Füll Raten oder Pixel-shaderbedarf, bei Einstellungen mit hoher Auflösung oder niedriger Vertex-shaderleistung durch eine Grafikkarte.

Da die meisten Titel CPU-begrenzt sind, kommt es bei der Optimierung CPU-intensiver Spielsysteme zu den größten Leistungsgewinne. In der Regel sind die KI-oder Physik Systeme und die zugehörige Kollisions Erkennungs Logik die primären Consumer von CPU-Zyklen in gut verhaltene Microsoft Direct3D-Anwendungen. Jede Arbeit, um diese Systeme zu verbessern, kann die Gesamtleistung des Spiels verbessern.

## <a name="poor-batch-management"></a>Schlechte Batch Verwaltung

Das erzielen einer guten Parallelität mit der GPU erfordert, dass Draw-Batches genügend Geometrie – und die Shader über die richtige Komplexität verfügen –, damit die Grafikkarte ausgelastet bleibt, während nicht so viele Batches verwendet werden, dass der Befehls Puffer überflutet wird. Auf der Hardware der aktuellen Generation wird empfohlen, ungefähr 300 oder weniger Zeichen für zeichnen-Batches pro Frame (weniger auf leistungsstarken CPUs) zu empfehlen, um zu verhindern, dass der Treiber die Verarbeitung des Befehls Puffers zu einem Leistungsengpass wird. Einige andere API-Zustands Aufrufe und Treiber Kombinationen können zu kostspieliger CPU-Verarbeitung führen (z. b. Treiber Kompilierung von Shadern). Daher empfehlen wir dringend eine routinemäßige Leistungsanalyse.

## <a name="excessive-memory-copying"></a>Übermäßige Speicher Kopiervorgänge

Während der Entwicklung der meisten PC-Titel verwenden Entwickler bequeme Datenstrukturen und Zeichen folgen für die Inhalts Verwaltung. Die für den Zeichen folgen Vergleich, das Kopieren und andere Manipulationen erforderliche CPU-Arbeit hat häufig einen messbaren Aufwand, insbesondere dann, wenn die Leistungs Treffer berücksichtigt werden, die mit dem Cache-und Speichersubsystem verknüpft sind. Pläne sollten bei der Entwicklung dieser Systeme zum Entfernen oder Minimieren der Abhängigkeit von der Zeichen folgen Verarbeitung erfolgen, sobald das Produkt in die primären Test-und releasephasen gelangt.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Übermäßige Verwendung der dynamischen zeichnen-Übermittlung

Moderne Video Hardware ist beim Umgang mit statischen Daten gut. High-End-Adapter verfügen häufig über eine große Menge an Video Arbeitsspeicher, aber dieser Arbeitsspeicher kann nicht effektiv von dynamischen Daten genutzt werden.

Obwohl für dynamische Inhalte in angemessener Weise effiziente Verwendungs Muster für dynamische Vertex-Puffer/Index Puffer implementiert werden können, überschreiten viele Titel diese Ausdrucksweise für den anderen statischen Inhalt. Dies wird am häufigsten mit BSP-Strukturen (Binary Space Partitionierung) und Portal basierten Systemen angezeigt, die Geometrie in einer Datenstruktur speichern, die der Hardware nicht zugeordnet ist und für jeden Frame in Puffer verarbeitet werden muss. Wenn Sie so viele Inhalte wie möglich in statische Ressourcen einfügen, kann dies den Bandbreiten Aufwand bei der Datenübertragung auf die Grafikkarte erheblich reduzieren, den VRAM im virtuellen Netzwerk besser nutzen und den CPU/Cache-Aufwand für die Verarbeitung dieser Inhalte verringern.

## <a name="high-overhead-in-file-processing"></a>Hoher Aufwand bei der Dateiverarbeitung

PC-Spiele haben einen Ruf für lange Ladezeiten erlangt, insbesondere im Vergleich zu Konsolen Titeln mit strengen Lade Zeitanforderungen. Unsere Analyse der Art und Weise, in der viele Titel das Datei Subsystem verwenden, stellt einige häufige Probleme dar.

Der Aufwand für das Öffnen einer Datei ist in der Regel viel höher als die Entwickler erwarten. Wenn on-Demand-Virenscanner häufig genutzt werden und die zusätzliche Funktionalität von NTFS, ist das Öffnen einer Datei ein ziemlich kostspieliger Vorgang. Wenn Sie viele Dateien gleichzeitig öffnen oder die gleiche Datei wiederholt öffnen und schließen, ist daher eine schlechte Methode für die Dateiverwaltung. Einige Spiele haben versucht, diese Leistungseinbußen zu verringern, indem Sie vor dem Öffnen der Datei testen, ob eine Datei vorhanden ist. Die Realität ist, dass das vorhanden sein einer Datei auf NTFS das Öffnen der Datei erfordert, sodass das Testen vor dem Öffnen die Kosten zweimal abzahlt.

Spiele, die Add-on-Änderungen oder Moden zulassen oder das Entwicklungs Gerüst zum Überprüfen auf Außerkraftsetzungs Datendateien enthalten, können beim Laden des Spiels erhebliche Verzögerungen verursachen, da diese Dateien nicht vorhanden sind. Dies ist auch dann der Fall, wenn diese Dateien nicht vorhanden sind. Es wird empfohlen, dass Spiele nur diese Dateien überprüfen, wenn Sie mit einem speziellen Befehls Zeilenschalter oder einem anderen Modusschalter ausgeführt werden, sodass nur die Benutzer, die diese Funktionalität nutzen, tatsächlich die Leistungskosten dieser (häufig umfassenden) Überprüfungen bezahlen.

Aus dem Dateisystem können folgende zusätzliche Leistung erzielt werden:

-   Angemessene Verwendung der Dateisystem Hinweise Datei Flag für den \_ \_ zufälligen \_ Zugriff und \_ Dateiflag- \_ sequenziellen \_ Scan
-   Größen Anpassungs Puffer, um eine große Anzahl von Aufrufen an die Lese-/Schreib-APIs des Betriebssystems zu vermeiden
-   Asynchrones Zugreifen auf Dateien
-   Laden von Threads im Hintergrund

Außerdem wird dringend empfohlen, Daten beim ersten Ausführen des Spiels offline zu konvertieren (zum Zeitpunkt der Erstellung oder Installation), anstatt sich auf die Konvertierung zu verlassen, da dadurch für jeden Benutzer eine beträchtliche Leistungs teuer erzwungen wird.

## <a name="slow-and-frustrating-installation"></a>Langsame und frustrierende Installation

Ein weiteres häufiges Problem, das wir gesehen haben, ist eine sehr lange Installationszeit für viele moderne PC-Spiele. Die Installer fordern den Benutzer mehrmals an, manchmal einfach den Benutzer zu benachrichtigen, z. b. "Sie benötigen DirectX nicht installiert". Im Allgemeinen ist es für diese problematischen Installer erforderlich, dass der Benutzer das **nächste** Mal oder **OK** mehrmals auswählt, bevor die Installation des Spiels tatsächlich beginnt. Sobald Sie begonnen haben, haben wir gesehen, dass einige Titel eine Stunde oder länger dauern, bis der Benutzer die Gelegenheit erhält, das Spiel zu spielen. Wir sind der Meinung, dass die erste Stunde der Spiel Wiedergabe Erfahrung nicht die Installation sein sollte.

Wir empfehlen eine Reihe von Ansätzen für den Umgang mit der-Installation. Lassen Sie die Eingabe Aufforderungen zuerst einfach und minimal. Zweitens: Entwerfen Sie Ihre Spieldaten so, dass einige oder alle Datendateien direkt vom Verteilungs Datenträger verwendet werden können, sofern möglich – moderne DVD-Laufwerke verfügen über eine sehr hohe Bandbreite. Angenommen, Sie sollten die Installation bei Bedarf in ihren Titeln implementieren, um den Installationsvorgang zu reduzieren oder zu eliminieren und Benutzern so schnell wie möglich das Spiel zu ermöglichen. (Weitere Informationen zum bedarfsgesteuerten installieren finden Sie unter [install-on-Demand for Games](/windows/desktop/DxTechArts/install-on-demand-for-games).)

Weitere Empfehlungen zur Spiele Installation finden Sie unter [vereinfachen der Spiele Installation](/windows/desktop/DxTechArts/simplifying-game-installation).

## <a name="lack-of-consideration-of-physical-memory"></a>Fehlende Berücksichtigung des physischen Speichers

Aufgrund der breiten Variabilität der PC-Hardware auf dem Markt nutzen Titel in der Regel Ad-hoc-Konfigurations Tests, um die Standardeinstellungen für die Ebene der grafischen Details auszuwählen. Einige der Titel, die wir gesehen haben, verwenden die Größe des Video Speichers in diesen Tests, aber Sie können diese nicht mit der Größe des physischen Speichers korrelieren. Um verlorene Geräte Situationen zu bewältigen, muss der Großteil des Video Speichers (sowohl lokaler VRAM auf der Karte als auch die nicht lokale AGP-Arbeitsspeicher Öffnung) durch den physischen Speicher unterstützt werden, entweder durch die Verwendung verwalteter Ressourcen oder benutzerdefinierter Datenstrukturen. Einige High-End-Videokarten weisen VRAM-Größen auf, die mit der Größe von Low-End-CPU-Erinnerungen konkurrieren. In Fällen, in denen das System im Vergleich zur Grafikkarte begrenzten physischen Speicher hat, kann der größte Teil dieses VRAM nicht effektiv genutzt werden, und es sollten Einstellungen mit niedrigerer Detail Konfiguration konfiguriert werden.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Over-Reliance Real-Time audiostichproben-Raten Konvertierung

Eine weitere häufige Quelle für den verbrauchen von CPU-Zyklen tritt auf, wenn das Audiosystem zum Konvertieren der Wiedergabe Rate während der Mischung in den Hardware Puffer benötigt wird. Bei Windows-Treibermodell-Treibern (WDM) befindet sich das Hardware Puffer Format nicht unter direkter Anwendungssteuerung, da es sich um eine Ressource auf Kernel Ebene handelt. Stattdessen wird das Format basierend auf dem Format der höchsten Qualität aller Quellen und der Funktionen der Hardware ausgewählt. Standardmäßig verwendet Windows XP eine qualitativ hochwertige Stichprobenrate für diesen Prozess, und wenn für die Mehrzahl der Audiobeispiele eine Raten Konvertierung erforderlich ist, wird ein erheblicher Teil der CPU-Zyklen verbraucht.

Es wird empfohlen, alle Ihre DirectSound-Puffer mit der gleichen Stichprobenrate zu erstellen. Wenn Sie Microsoft Win32- **Wellen** Funktionen verwenden, sollten Sie auch eine konsistente Samplingrate verwenden. Mit WDM-Treibern werden die Puffer alle durch den Kernel gemischt, und wenn Sie eine höhere Samplingrate für einige davon verwenden, werden die Stichproben Raten aller übrigen Rest-Werte entsprechend konvertiert. Beachten Sie, dass dies die Verwendung der gleichen Wiedergabe Rate für alle Audiobeispiele bedeutet, einschließlich aller streamingaudiokomprimierungspuffer. Das Festlegen der primären Puffer Rate hat keine Auswirkung, es sei denn, Sie legen Windows 98 oder Windows Millennium Edition als Ziel fest.

> [!Note]  
> Unter Windows Vista und höheren Versionen des Betriebssystems verwenden DirectSound und **waveout** die [Windows-audiositzungs-API (WASAPI)](/windows/desktop/CoreAudio/wasapi) für die gesamte Audioausgabe.

 

## <a name="fragmention-of-virtual-memory"></a>Fragnenangabe des virtuellen Speichers

Wir haben eine Reihe aktueller Probleme im Zusammenhang mit dem 32-Bit-Limit für den Prozess Speicherbereich erkannt. 2 GB virtueller Adressraum für Benutzermodusprozesse waren in der Vergangenheit mehr als ausreichend. die zunehmende Verwendung von großen Speicher Abbild Dateien, benutzerdefinierten Speicher Belegungen und der Vergrößerung der VRAM-Größe (die im Prozessbereich zugeordnet werden muss) hat jedoch begonnen, wenn Speicherplatz Zuordnungen des virtuellen Speicherplatzes fehlschlagen. Einige DLLs, die nicht von Microsoft stammen, verwenden festgelegte Start Orte in der Mitte des virtuellen Adressraums. Dies führt zu einer Fragmentierung, die zu Fehlern bei der Zuweisung führt.

Diese Probleme treten am häufigsten auf, wenn das Spiel ein benutzerdefiniertes Speicher Belegungs Schema verwendet, mit dem versucht wird, einen großen kontinuierlichen Anteil des virtuellen Speicherplatzes zuzuordnen. Unsere Empfehlung besteht darin, Zuweisungen so zu schreiben, dass Sie je nach Bedarf größere Teile des virtuellen Adressraums anfordern. Beispiel: Anfordern von 64 oder 256 MB gleichzeitig, aber nicht 1 GB. Allerdings sollte darauf geachtet werden, dass keine weitere Fragmentierung durchgeführt wird. Durch die Einführung von 64-Bit-Betriebssystemen und-Hardware werden diese Probleme in Zukunft stark unterstützt, aber es ist wichtig, dass Sie sich auf 32-Bit-Systemen der aktuellen Generation kümmern müssen.

## <a name="manipulation-of-the-floating-point-control-word"></a>Bearbeitung des Floating-Point Steuer Worts

Als Hilfe beim Debuggen haben einige Entwickler durch Manipulationen des Gleit Komma Steuer Worts Ausnahmen für die Gleit Komma Einheit (SPU) aktiviert. Dies ist sehr problematisch und führt wahrscheinlich zu einem Absturz des Prozesses. Ebenso wie die Aufruf Konvention erfordert, dass das EBX-Register beibehalten wird, geht der Großteil des Systems davon aus, dass die FPU in einem Standardzustand ist, gibt sinnvolle Ergebnisse und generiert keine Ausnahmen. Treiber und andere Systemkomponenten berechnen häufig Ergebnisse basierend auf der Annahme, dass Standardfehler Werte in den Registern für fehlerhafte Bedingungen angezeigt werden. Wenn jedoch Ausnahmen aktiviert sind, werden diese nicht behandelt und führen zu Abstürzen.

Direct3D legt fest, dass die Gleit Komma Einheit im Rahmen der Initialisierung für den aufrufenden Thread mit einfacher Genauigkeit gerundet wird, es sei denn, das D3DCREATE \_ FPU \_ Preserve-Flag wird verwendet. in diesem Fall ist das Gleit Komma Steuerwort unverändert. Da das Steuerwort eine Thread spezifische Einstellung ist, kann sichergestellt werden, dass alle Anwendungsthreads auf den Modus mit einfacher Genauigkeit festgelegt sind, um die Leistung zu optimieren. Beachten Sie, dass das Aufrufen von [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) nicht für die x64-native Codierung gültig ist, die SSE stattdessen exklusiv verwendet, und die auf der PowerPC-basierte Architektur der Xbox 360-CPU sehr teuer ist.

> [!Note]  
> Wenn Sie das Steuerwort ändern, verwenden Sie [**\_ controlfp \_ s**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) . Beachten Sie, dass Sie für x64-Plattformen die Gleit Komma Genauigkeit nicht über das Steuerwort ändern können.

 

In Bibliotheken, in denen wir unterschiedliche Rundungsregeln oder andere Verhaltensweisen benötigen – z. b. den Umgang mit Software Scheitel Punkten oder der Kompilierung – speichern und Wiederherstellen wir das Steuerwort. Wenn ein Spiel von nicht standardmäßigen Rundungs-oder FPU-Ausnahmen Gebrauch machen muss, sollte es das Gleit Komma Steuerwort speichern und wiederherstellen, und Sie sollten darauf achten, dass kein externer Code aufgerufen wird, der aufgrund dieser Probleme nicht sicher ist, einschließlich System-APIs.

## <a name="optional-installation-of-the-directx-runtime"></a>Optionale Installation der DirectX-Laufzeit

Eine Reihe von spielen fragt den Benutzer, ob DirectX installiert werden muss. Dies kann zu Problemen führen, wenn der Benutzer annimmt, dass das aktuelle DirectX Redistributable-System installiert ist und die Installation überspringt. Anschließend wird die Installation erfolgreich fortgesetzt. Wenn das Spiel eine bestimmte Version von D3DX oder andere aktualisierte Funktionen erfordert, die nicht installiert wurden, funktioniert das Spiel nicht, und der Benutzer wird sehr frustriert.

Es wird dringend empfohlen, dass das Installationsprogramm des Spiels die DirectX Redistributable automatisch installiert, für die das Spiel erstellt wurde. Der DirectX-Installationsvorgang ist so konzipiert, dass überprüft wird, ob etwas aktualisiert werden muss, und gibt es schnell zurück, wenn dies nicht der Fall ist. Daher ist es nicht erforderlich, den Benutzer über die Installation von DirectX zu Fragen.

Sie können eine unbeaufsichtigte Installation von DirectX ausführen, indem Sie den folgenden Befehl aus dem Installationspaket ausführen: **dxsetup.exe/Silent**

Außerdem kann die tatsächliche Größe des verteilbaren Ordners so konfiguriert werden, dass nur die CAB-Dateien (CAB-Dateien) enthalten sind, die für die Zielplattformen und die Verwendung des Spiels tatsächlich benötigt werden.

> [!Note]  
> Bevor Sie **dxsetup** verwenden, lesen Sie [nicht so direktes Setup](https://walbourn.github.io/).

 

## <a name="excessive-use-of-thread-synchronization"></a>Übermäßige Verwendung der Thread Synchronisierung

Bei der Profilerstellung sind die wichtigsten Hotspots häufig mit der Eingabe und dem belassen kritischer Abschnitte zu tun. Mit der Verbreitung von Multikern-CPUs hat sich die Verwendung von Multithreading in spielen erheblich erhöht, und viele Implementierungen basieren auf einer hohen Verwendung der Thread Synchronisierung. Die CPU-Zeit für die Übernahme eines kritischen Abschnitts, auch ohne Konflikte, ist sehr wichtig, und alle anderen Formen der Thread Synchronisierung sind noch teurer. Daher muss darauf geachtet werden, dass die Verwendung dieser primitiven minimiert wird.

Eine häufige Quelle der übermäßigen Synchronisierung in spielen ist die Verwendung von [D3DCREATE \_ Multithreaded](/windows/desktop/direct3d9/d3dcreate). Dieses Flag ist, während Direct3D Thread sicher für das Rendering aus mehreren Threads ist, ein sehr konservativer Ansatz, was zu einem hohen Synchronisierungs Aufwand führt. Spiele sollten dieses Flag vermeiden. Stattdessen wird die-Engine so konzipiert, dass die gesamte Kommunikation mit Direct3D von einem einzelnen Thread aus erfolgt, und jede Kommunikation zwischen Threads wird direkt behandelt. Weitere Informationen zum Entwerfen von multithreadspielen finden Sie im Artikel [Codieren mehrerer Kerne auf Xbox 360 und Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores).

## <a name="use-of-rdtsc"></a>Verwendung von RDTSC

Die Verwendung der x86-Anweisung **RDTSC** ist nicht empfehlenswert. **RDTSC** kann die zeitliche Steuerung für einige Energie Verwaltungs Schemas nicht ordnungsgemäß berechnen, die die CPU-Frequenz dynamisch und für viele Multikern-CPUs ändern, für die der Zyklen nicht zwischen Kernen synchronisiert wird. Spiele sollten stattdessen die [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) -API verwenden. Weitere Informationen zu Problemen mit **RDTSC** und zur Implementierung des Zeitpunkts für die hohe Auflösung mit **QueryPerformanceCounter** finden Sie im Artikel [Spiel Zeitsteuerung und multikernenprozessoren](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).

 

 