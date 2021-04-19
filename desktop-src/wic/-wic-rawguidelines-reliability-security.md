---
description: Zuverlässigkeit und Sicherheit
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Zuverlässigkeit und Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0f0e4a244de2c1463cdadb76162c18b041812b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349595"
---
# <a name="reliability-and-security"></a>Zuverlässigkeit und Sicherheit

Da in der Windows-Shell und der Fotogalerie Windows Imaging Component (WIC)-Codecs aufgerufen werden, sollten Codec-Autoren alle Anstrengungen Unternehmen, um ein hohes Maß an Zuverlässigkeit und Sicherheit in ihren WIC-Codecs sicherzustellen.

Das Schreiben von zuverlässigem Code hängt größtenteils von guten Codierungs Methoden, effektiven Code Überprüfungen und umfassenden Komponententests und Szenariotests ab. Außerdem wird anhand der folgenden Richtlinien sichergestellt, dass der Codec den Windows Vista-Richtlinien bezüglich der Zuverlässigkeit entspricht.

-   E/a-Abbruch aktivieren.

    Die Codec-Autoren sollten eine Möglichkeit für den Endbenutzer bieten, einen Vorgang mit langer Laufzeit abzubrechen. WIC-Codecs unterstützen dies durch Implementieren von iwicbitmapprogressnotification. Dadurch kann eine aufrufende Anwendung eine Rückruffunktion angeben, die der Codec in angegebenen Intervallen aufruft, um den Aufrufer über den Fortschritt des aktuellen Vorgangs zu benachrichtigen. Wenn eine Anwendung einen Fehler zurückgibt \_ , der von der Rückruffunktion abgebrochen wurde, muss der Codec den Vorgang abbrechen, der ausgeführt wird, und das HRESULT an den Aufrufer zurückgeben. Dies ist insbesondere bei unformatierten Codecs wichtig, da es einige Sekunden dauern kann, bis ein rohimage in voller Größe decodiert wird, und Anwendungen benötigen eine Möglichkeit, diese Verarbeitung abzubrechen.

-   Stellen Sie sicher, dass der Code im kleinsten Bereich ausgeführt wird, der für die Ausführung seiner Funktion erforderlich ist.

    Die Codec-Autoren müssen sicherstellen, dass der Codec nicht mehr Ressourcen als notwendig beansprucht oder einen größeren Bereich hat, als erforderlich ist. Der Bereich eines Codecs in WIC ist eine einzelne Bilddatei. der Codec wird erstellt, wenn eine Bilddatei geladen wird, und der Codec wird freigegeben, wenn das Bild geschlossen wird. Da WIC eine erweiterbare komponentenbasierte Plattform ist, haben WIC-Codecs überlappende Lasten und entladen und werden alle innerhalb desselben Prozesses gestartet und beendet. Wenn die zugrunde liegende Infrastruktur eines Codecs Start-und Stoppvorgänge in einem Bereich erfordert, der größer als ein einzelnes Image ist, wird die Zuverlässigkeit beeinträchtigt. WIC-fähige Codecs werden sowohl vom Windows-Explorer als auch von anderen Anwendungen verwendet. Wenn ein Codec für die Lebensdauer des Prozesses geladen wird, wird der Arbeitsspeicher daher nicht effizient freigegeben, und ein Fehler des Codecs könnte den Windows-Explorer beeinträchtigen und möglicherweise erfordern, dass der Computer neu gestartet wird. (Beachten Sie, dass der Codec jedes Mal aufgerufen wird, wenn ein Bild zum ersten Mal in Windows-Explorer als Fingerabdruck verwendet wird: Es ist von entscheidender Bedeutung, dass es sich hierbei um einen leichten Vorgang handelt.)

-   Verwenden Sie statische und dynamische Code Analysetools.

    -   Statische Analysetools:

        Präfix: zum Erkennen von Fehlern zum Zeitpunkt der Kompilierung.

        Vorfast: für die Analyse von Code auf Fehler.

    -   Dynamische Analysetools:

        AppVerifier: Dadurch können Anwendungen stabiler werden, da häufige Probleme mit der realen Software simuliert werden.

-   Überprüfen Sie alle Eingaben in Code Reviews.

    Alle Parameter für exportierte Methoden und alle Datei Daten müssen sorgfältig überprüft werden, wenn Sie fehlerhaft sind, um Sie vor Pufferüberläufen und unter Läufen, arithmetischen Überläufen und unter Läufen, arithmetischen Überläufen und Unterläufen und unerwarteten Typen zu schützen.

-   Verwenden Sie Datei-fuzzingtechniken, um mögliche Abstürze und Abstürze zu erkennen.

    Beim Durchlaufen von Dateien wird der Codec mit zufällig permusigen Eingaben getestet.

    Es gibt zwei Arten von Datei fuzzingverfahren: ungesteuerte (zufällige) fuzzingaktionen und gesteuerte fuzzingaktionen. Bei einem ungerichteten fuzzingvorgang wird ein zufälliges biflipping durchgeführt, um festzustellen, ob die zufällige Eingabe den Codec abstürzen Ein gerichteter fuzzingvorgang führt dazu, dass die Eingabe basierend auf einigen Kenntnissen des Datei Formats durchgeführt wird. Wenn z. b. eine Cycle redundant Check (CRC) bei Byte Offset 32 vorhanden ist, wird das Ändern von Bytes ohne die Aktualisierung des CRC wahrscheinlich nicht die meisten Codepath-Methoden ausführen. In diesem Beispiel sollte ein gerichteter Fuzzer den CRC beheben, wenn alle Bytes geändert werden.

    Der Eingabe Satz von Bildern für das Datei-fuzzingverfahren sollte so erstellt werden, dass jede vom Decoder unterstützte Parameter Kombination getestet wird. Wenn der Decoder beispielsweise Little-und Big-Endian-Dateien und drei Komprimierungs Einstellungen unterstützt, sollte der Eingabe Satz von Image aus Little-Endian-Dateien jeder Komprimierungs Einstellung und Big-Endian-Dateien für jede Komprimierungs Einstellung bestehen. Diese Vorgehensweise führt zu einem großen, aber sehr robusten Satz von Eingabe Bildern, die getestet werden sollen. Auch wenn keine Kamera die einzelnen Kombinationen erzeugt, aber der Decoder diese theoretischen Kombinationen unterstützt, sollten die Codec-Autoren diese Eingaben übermitteln.

    Die Sicherheit kann durch regelmäßiges Testen von Bilddateien während der Codec-Entwicklung erheblich verbessert werden. Codecs sollten immer in der Lage sein, Bilddatei Beschädigungen zu erkennen und bei falsch formatierten Anforderungen oder falsch formatierten Daten ordnungsgemäß fehlschlagen zu lassen.

-   Belastungs Code.

    Belastung: Testen Sie den Codec, indem Sie ihn kontinuierlich in mehreren gleichzeitigen Prozessen ausführen und alle unterstützten Vorgänge in allen möglichen Sequenzen auf Abbildern unterschiedlicher Größe (einschließlich sehr großer Bilder) von jeder unterstützten Kamera ausführen.

-   Thread Sicherheit.

    Ab Windows 7 erfordert WIC, dass unformatierte Codecs den com-Apartment-Typ "beide" aufweisen. Dies bedeutet, dass Sie die entsprechende Sperre durchführen müssen, um Apartment übergreifende Aufrufer und Aufrufer in Szenarios mit mehreren Threads zu verarbeiten. Objekte innerhalb eines Multithread-Apartment (MTA) können gleichzeitig durch eine beliebige Anzahl von Threads innerhalb des MTA aufgerufen werden, was eine bessere Leistung für Multikernsysteme und bestimmte Server Szenarien ermöglicht. Darüber hinaus können WIC-Codecs, die innerhalb eines MTA Leben, andere Objekte aufrufen, die innerhalb des MTA Leben, ohne die Marshallingkosten im Zusammenhang mit dem Aufruf zwischen Threads, die in unterschiedlichen STA-Wohnungen leben. In Windows 7 wurden alle in-Box-WIC-Codecs aktualisiert, um MTAs zu unterstützen, einschließlich JPEG, TIFF, PNG, GIF, ICO und BMP. Drittanbieter-Codecs, die MTAs nicht unterstützen, führen aufgrund von Marshalling zu erheblichen Leistungseinbußen in Multithreadanwendungen. Zum Aktivieren der MTA-Unterstützung muss die ordnungsgemäße Synchronisierung im Drittanbieter-Codec implementiert werden. Die genaue Implementierung dieser Synchronisierungs Verfahren geht über den Rahmen dieses Artikels hinaus. Eine allgemeine Referenz zum Synchronisieren von COM-Objekten finden Sie unten.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



