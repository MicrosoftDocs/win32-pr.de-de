---
description: Empfehlungen für optimale Dateisystem Transaktionen.
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: Überlegungen zur Leistung von transaktionalen NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a71f7e100e1ddd8524932a4a259a12092bddcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960394"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>Überlegungen zur Leistung von transaktionalen NTFS

Transaktionale NTFS (TxF) wurde sorgfältig für die Leistung entwickelt und führt in der Regel eine bessere Leistung als allgemeine Transaktions Alternativen in ähnlichen Szenarien aus. Dateisystem Transaktionen haben jedoch mehr Aufwand als nicht transaktive Vorgänge, und eine gewisse Verringerung der e/a-Leistung im Vergleich zu nicht transaktionalen e/a-Vorgängen ist zu erwarten. Leistungskritische Anwendungen sollten einen Einführungs Zeitraum für die Technologie Einführung durchführen und die Auswirkungen auf die Leistung von transaktiven Dateisystem Vorgängen auswerten.

## <a name="overview-of-txf-operations"></a>Übersicht über TxF-Vorgänge

TxF verwendet die *Rückgängig* -Protokollierung zum Aufzeichnen der Änderungen, die erforderlich sind, um das Dateisystem wieder in einen konsistenten Zustand zu versetzen, der auch als Rollback bezeichnet wird, wenn ein Transaktions Abbruch auftritt. Diese rückgängig-Protokollierung generiert zusätzliche e/a-Vorgänge und ist die Quelle des TxF-Leistungs Aufwands im Vergleich zu nicht transaktionalen Dateisystem Vorgängen.

Eine allgemeine Zusammenfassung der Funktionsweise von TxF sieht wie folgt aus:

-   Im Verlauf einer Transaktion schreibt TxF *Rückgängig* -Datensätze für jede Änderung, die Sie an das Dateisystem vornimmt, in die zugehörige Protokolldatei. Wenn ein Abbruch auftritt, werden diese rückgängig-Datensätze analysiert, um das Dateisystem wieder in den Zustand zu versetzen, in dem es sich vor Beginn der Transaktion befand.
-   Ein rückgängig-Datensatz für *Metadatenänderungen* beschreibt eine Änderung nur für die Metadaten des Dateisystems. Einige Beispiele hierfür sind verschiebe-, Umbenennungs-, appends-und Attribut Änderungen. Bei der rückgängig-Datensätze für Metadatenänderungen werden alle zum Rückgängigmachen der Änderung erforderlichen Informationen im Datensatz gespeichert und in der Protokolldatei gespeichert.
-   Ein rückgängig-Datensatz über *Schreiben* beschreibt das Überschreiben eines Teils einer Datei. Wenn eine Datei überschrieben wird, werden die ursprünglichen Inhalte der Datei in einer speziellen Rückgängigdatei in einem ausgeblendeten Verzeichnis gespeichert, und das Überschreibungs Daten Satz-Datensatz verweist auf diese Datei. Wenn Datei Updates schließlich vom Cache auf den Datenträger geleert werden, muss auch der Inhalt der rückgängig-Datei geleert werden, sodass eine transaktive Datei Überschreibung bis zu zwei zusätzliche zufällige e/a-Vorgänge generieren kann: eine zum Lesen der alten Daten und eine, um Sie in die rückgängig-Datei zu schreiben. Diese zusätzlichen e/a-Vorgänge sind Leistungskosten von TxF.
-   Wenn ein Commit ausgeführt wird, leert TxF zuerst alle Rückgängig-Informationen, leert dann die eigentlichen Dateiänderungen und schreibt und leert einen Commitdatensatz. Wenn keine rückgängig-Dateien geleert werden sollen, ist der einzige zusätzliche TxF-mehr Aufwand im Verhältnis zu nicht transaktionalen e/a-Vorgängen, dass das Protokoll selbst geleert wird. Protokoll Leerungen führen jedoch zu effizienten großen sequenziellen Schreibvorgängen, sodass die Leistungskosten minimal sind.
-   TxF ist für den Commit optimiert. Es wird erwartet, dass die meisten Transaktionen erfolgreich sind und kein Rollback ausgeführt werden muss. Daher werden alle rückgängig-Datensätze für eine Transaktion nicht verwendet. Im Hinblick auf die Leistung sind TxF-Commit-Vorgänge schnell und Rollbacks sind ressourcenintensiv.
-   Ein Rollback ist ressourcenintensiver als Commit. Während des Rollbacks müssen alle Änderungen, die in der Transaktion vorgenommen wurden, nicht ausgeführt werden. Im Allgemeinen kann die Rollback-Dauer ungefähr so lange dauern, bis die Änderungen ursprünglich vorgenommen wurden. Wenn z. b. 1 Sekunde benötigt wird, um alle Änderungen vorzunehmen, kann es ungefähr 1 Sekunde dauern, bis die Änderungen rückgängig gemacht werden. Bei sehr langen Transaktionen kann das Rollback zu zusätzlichen Leistungsbeeinträchtigungen führen. Beispielsweise kann die Systemstart Zeit verzögert werden, wenn das System automatisch ein Rollback für eine Transaktion ausführen muss, falls das System nicht mehr reagiert und einen nicht geplanten Neustart ausführen muss.

Im folgenden finden Sie eine Übersicht über die Leistung, die aus der vorherigen Liste gezeichnet werden kann:

-   Die Leistungseinbußen von TxF für Transaktionen, die Datei Überschreibungen betreffen, können signifikant sein.
-   Die Leistungseinbußen von TxF für Transaktionen, die nur Metadatenvorgänge betreffen, können relativ gering sein, sofern große Transaktionen verwendet werden. Eine große Transaktion ist, wenn für jeden Commitdatensatz viele rückgängig-Datensätze vorhanden sind.

## <a name="recommendations-for-best-performance"></a>Empfehlungen für eine optimale Leistung

Amortisieren Sie den TxF-Aufwand für größere Transaktionen. Wenn Sie z. b. über *n* Gruppen von Änderungen verfügen, bei denen jede Änderung über *m* Schritte verfügt, und Sie die Möglichkeit haben, dies entweder als *N* Transaktionen von *m* Schritten auszuführen, oder alles als einzelne Transaktion mit *M* \* *N* Schritten auszuführen, wäre die zweite Option effizienter.

Beachten Sie die möglichen Auswirkungen auf das Starten von sehr großen Transaktionen. Wie bereits erwähnt, kann ein Rollback langsam sein und die Startzeit verzögern, wenn das System automatische Rollbacks als Startzeit ausführen muss. Je größer die Transaktion ist, desto länger ist die Verzögerung.

Behalten Sie Transaktionen vor allem bei metadatenvorgängen bei. Dies ist die Optimierung von TxF für und im Allgemeinen ist die Leistung ungefähr identisch mit der nicht transaktiven Datei-e/a für große metadatentransaktionen. Beispiele für effiziente metadatentxf-Funktionen sind " [**fivefiletransaktive**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)", " [**setfileattributestransagiert**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)", " [**copyfiletransktive**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)", " [**deletefiletransktive**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)", " [**kreatehardlinktransktive**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)" und "angefügte Schreibvorgänge" (Aufrufe der Funktion " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ", wenn der Dateizeiger am Ende der Datei oder " *EOF* Ein Beispiel für ressourcenintensive nicht-Metadatenvorgänge sind Aufrufe der Funktion " **Write File** ", wenn sich der Dateizeiger nicht am EOF-Element befindet.

## <a name="summary-of-txf-performance-expectations"></a>Zusammenfassung der TxF-Leistungserwartungen

Bei direkten Updates sind über Schreibungen in einen Abschnitt einer Datei viel langsamer als nicht transaktive Datei-e/a-Vorgänge, während die TxF-Leistung für Dateisystem-Metadatenvorgänge (z. b. Create, Move und Append) mit nicht transaktionalen Datei-e/a für große Transaktionen vergleichbar ist.

 

 



