---
description: Zuverlässigkeit und Sicherheit
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Zuverlässigkeit und Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4704b84d09698fd6fabcf2d190050063ec3b3190904aa669fa78799c5d0158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441730"
---
# <a name="reliability-and-security"></a>Zuverlässigkeit und Sicherheit

Da Windows WIC-Codecs (Imaging Component) innerhalb der Windows-Shell und Fotogalerie aufgerufen werden, sollten Codecautoren alle Anstrengungen unternehmen, um ein hohes Maß an Zuverlässigkeit und Sicherheit in ihren WIC-Codecs sicherzustellen.

Das Schreiben von zuverlässigem Code hängt größtenteils von bewährten Codierungsmethoden, effektiven Codeüberprüfungen und gründlichen Komponententests und Szenariotests ab. Darüber hinaus tragen die folgenden Richtlinien dazu bei, sicherzustellen, dass der Codec den Windows Vista-Richtlinien in Bezug auf die Zuverlässigkeit entspricht.

-   E/A-Abbruch aktivieren.

    Codecautoren sollten dem Endbenutzer eine Möglichkeit bieten, alle Zeit-/Zeit-Ausführungen abzubricht. WIC-Codecs unterstützen dies, indem sie IWICBitmapProgressNotification implementieren. Dadurch kann eine aufrufende Anwendung eine Rückruffunktion angeben, damit der Codec in angegebenen Intervallen aufruft, um den Aufrufer über den Fortschritt des aktuellen Vorgangs zu benachrichtigen. Wenn eine Anwendung ERROR CANCELLED von der Rückruffunktion zurückgibt, muss der Codec jeden vorgang abbrechen, der in Bearbeitung ist, und das HRESULT an den \_ Aufrufer zurücksagt. Dies ist besonders wichtig für RAW-Codecs, da die Decodierung eines RAW-Images in voller Größe einige Sekunden dauern kann und Anwendungen eine Möglichkeit benötigen, diese Verarbeitung zu abbrechen.

-   Stellen Sie sicher, dass der Code im kleinsten Bereich ausgeführt wird, der zum Ausführen seiner Funktion erforderlich ist.

    Codecautoren müssen sicherstellen, dass der Codec nicht mehr Ressourcen als erforderlich verbraucht oder einen größeren Umfang als erforderlich hat. Der Bereich eines Codecs in WIC ist eine einzelne Bilddatei. der Codec wird erstellt, wenn eine Bilddatei geladen wird, und der Codec wird freigegeben, wenn das Bild geschlossen wird. Da WIC eine erweiterbare komponentenbasierte Plattform ist, haben WIC-Codecs überlappende Lasten und Entladungen sowie Starts und Stopps innerhalb desselben Prozesses. Wenn die zugrunde liegende Infrastruktur eines Codecs Start- und Stoppvorgänge in einem Bereich erfordert, der größer als ein einzelnes Image ist, wirkt sich dies auf die Zuverlässigkeit aus. WIC-fähige Codecs werden sowohl vom Windows Explorer als auch von anderen Anwendungen verwendet. Wenn ein Codec für die Lebensdauer des Prozesses geladen bleibt, wird der Arbeitsspeicher daher nicht effizient freigegeben, und ein Fehler des Codecs kann Windows Explorer hängen bleiben und möglicherweise einen Neustart des Computers erfordern. (Beachten Sie, dass der Codec jedes Mal aufgerufen wird, wenn ein Bild zum ersten Mal in Windows Explorer als Miniaturansicht angezeigt wird: Es ist wichtig, dass dies ein schlanker Vorgang ist.)

-   Verwenden Sie statische und dynamische Codeanalysetools.

    -   Statische Analysetools:

        PREfix: zum Erkennen von Fehlern zur Kompilierzeit.

        PREfast: Zum Analysieren von Code auf Fehler.

    -   Tools für die dynamische Analyse:

        AppVerifier: hilft, Anwendungen resilienter zu machen, indem häufige reale Softwareprobleme simuliert werden.

-   Überprüfen Sie alle Eingaben in Code Reviews.

    Alle Parameter für exportierte Methoden und alle Dateidaten müssen sorgfältig auf Gültigkeit überprüft und robust abgelehnt werden, wenn ein Fehler vor Pufferüberläufen und -unterläufen, arithmetischen Über- und Unterläufen sowie unerwarteten Typen schützt.

-   Verwenden Sie Dateifuzzingtechniken, um potenzielle Abstürze und Hängen zu entdecken.

    Dateifuzzing ist der Prozess, bei dem der Codec mit zufällig permutierten Eingaben getestet wird.

    Es gibt zwei Formen des Dateifuzzings: undirektionales (zufälliges) Fuzzing und gerichtetes Fuzzing. Beim undirektionalen Fuzzing wird zufälliges Bit gekippt, um zu sehen, ob zufällige Eingaben den Codec abstürzen können. Gerichtetes Fuzzing permutiert die Eingabe basierend auf einigen Kenntnissen des Dateiformats. Wenn beispielsweise eine Zyklusredundanzprüfung (Cycle Redundancy Check, CRC) beim Byteoffset 32 besteht, wird das Ändern von Bytes ohne Aktualisierung der CRC wahrscheinlich nicht die meisten Codepfade ausführen. In diesem Beispiel sollte ein gerichteter Fuzzer die CRC korrigieren, wenn Bytes geändert werden.

    Der Eingabesatz von Bildern für dateifuzzing sollte so erstellt werden, dass jede Parameterkombination, die der Decoder unterstützt, getestet wird. Wenn der Decoder beispielsweise Little- und Big-Endian-Dateien und drei Komprimierungseinstellungen unterstützt, sollte der Eingabesatz des Bilds aus Little-Endian-Dateien jeder Komprimierungseinstellung und Big-Endian-Dateien für jede Komprimierungseinstellung bestehen. Dieser Ansatz führt zu einer großen, aber sehr stabilen Reihe von Eingabebildern, die getestet werden müssen. Auch wenn keine Kamera jede der Kombinationen erzeugt, aber der Decoder diese theoretischen Kombinationen unterstützt, sollten Codecautoren diese Eingaben fuzzieren.

    Die Sicherheit kann durch regelmäßige Fuzz-Tests von Bilddateien während der Codecentwicklung stark verbessert werden. Codecs sollten immer in der Lage sein, Beschädigungen von Bilddateien zu erkennen und bei einer fehlerhaften Anforderung oder bei falsch formatierten Daten ordnungsgemäß fehlschlägt.

-   Belastung des Codes.

    Testen Sie den Codec, indem Sie ihn kontinuierlich in mehreren gleichzeitigen Prozessen ausführen und alle unterstützten Vorgänge in allen möglichen Sequenzen auf Bildern unterschiedlicher Größe (einschließlich sehr großer Bilder) von jeder unterstützten Kamera ausführen.

-   Threadsicherheit.

    Ab Windows 7 erfordert WIC, dass ROHCODECs den COM-Apartmenttyp "Both" haben. Dies bedeutet, dass Sie die entsprechende Sperre für apartmentübergreifende Aufrufer und Aufrufer in Multithreadszenarios verwenden müssen. Objekte in einem Multithread-Apartment (MTA) können gleichzeitig von einer beliebigen Anzahl von Threads innerhalb des MTA aufgerufen werden, was eine bessere Leistung auf Systemen mit mehreren Kernen und bestimmten Serverszenarien ermöglicht. Darüber hinaus können WIC-CODECs, die in einem MTA leben, andere Objekte aufrufen, die innerhalb des MTA leben, ohne die Marshallingkosten, die mit dem Aufruf zwischen Threads verbunden sind, die in verschiedenen STA-Apartments leben. In Windows 7 wurden alle In-Box-WIC-CODECs aktualisiert, um MTAs zu unterstützen, einschließlich JPEG, TIFF, PNG, GIF, ICO und BMP. CodeCs von Drittanbietern, die MTAs nicht unterstützen, verursachen erhebliche Leistungskosten in Multithreadanwendungen aufgrund von Marshalling. Die Aktivierung der MTA-Unterstützung erfordert, dass eine ordnungsgemäße Synchronisierung im CODEC eines Drittanbieters implementiert wird. Die genaue Implementierung dieser Synchronisierungstechniken geht über den Rahmen dieses Whitepapers hinaus. Eine allgemeine Referenz zum Synchronisieren von COM-Objekten finden Sie unten.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guidelines for Camera RAW Image Formats](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



