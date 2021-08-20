---
description: Empfehlungen für optimale Dateisystemtransaktionen.
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: Überlegungen zur Leistung bei Transaktional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32729725ecc6ba59808eabe1fa12a5b798c9413c52d1591bd22b498e6a5856d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996714"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>Überlegungen zur Leistung bei Transaktional NTFS

Transaktionales NTFS (TxF) wurde sorgfältig auf Leistung ausgelegt und bietet in ähnlichen Szenarien in der Regel eine bessere Leistung als allgemeine Transaktionsalternativen. Dateisystemtransaktionen haben jedoch mehr Aufwand als nicht transaktive Vorgänge, und eine gewisse Verringerung der E/A-Leistung im Vergleich zu nicht transaktiven E/A-Vorgängen ist zu erwarten. Leistungskritische Anwendungen sollten einen Qualifikationszyklus für die Einführung von Technologie durchführen und die Auswirkungen von transaktionsbasierten Dateisystemvorgängen auf die Leistung auswerten.

## <a name="overview-of-txf-operations"></a>Übersicht über TxF-Vorgänge

TxF  verwendet die Rückgängig-Protokollierung, um die Änderungen zu erfassen, die erforderlich sind, um das Dateisystem im Fall eines Transaktionsabbruchs wieder in einen konsistenten Zustand zu bringen, der auch als Rollback bezeichnet wird. Diese Rückgängigprotokollierung generiert zusätzliche E/A-Vorgänge und ist die Quelle des TxF-Leistungsaufwands im Vergleich zu nicht transaktionalen Dateisystemvorgängen.

Eine zusammenfassende Zusammenfassung der Funktionsweise von TxF lautet wie folgt:

-   Im Verlauf einer Transaktion schreibt  TxF rückgängig gemachte Datensätze in die Protokolldatei für jede Änderung, die am Dateisystem vorgenommen wird. Wenn ein Abbruch auftritt, werden diese Rückgängig-Datensätze analysiert, um das Dateisystem wieder in den Zustand zu bringen, den es vor Beginn der Transaktion hatte.
-   Ein  Metadatenänderungs-Rückgängig-Datensatz beschreibt nur eine Änderung an den Metadaten des Dateisystems. Beispiele hierfür sind Verschiebe-, Umbenennungs-, Anfüge- und Attributänderungen. Beim Rückgängig machen von Metadatenänderungsdatensätzen sind alle Informationen, die zum Rückgängig machen der Änderung erforderlich sind, im Datensatz enthalten und in der Protokolldatei gespeichert.
-   Ein *Datensatz zum Rückgängig machen* überschreiben beschreibt das Überschreiben eines Teils einer Datei. Wenn eine Datei überschrieben wird, wird der ursprüngliche Inhalt der Datei in einer speziellen Rückgängigdatei in einem ausgeblendeten Verzeichnis gespeichert, und der Überschreibungs-Undo-Datensatz verweist auf diese Datei. Wenn Dateiupdates schließlich aus dem Cache auf den Datenträger geleert werden, muss auch der Inhalt der Rückgängig-Datei geleert werden, sodass eine transaktive Dateiüberschreibung bis zu zwei zusätzliche zufällige E/A-Vorgänge generieren kann: einen zum Lesen der alten Daten und einen zum Schreiben in die Rückgängigdatei. Diese zusätzlichen E/A-Vorgänge sind Leistungskosten von TxF.
-   Wenn ein Commit auftritt, leert TxF zuerst alle Rückgängiginformationen, leert dann die tatsächlichen Dateiänderungen und schreibt und leert dann einen Commitdatensatz. Wenn keine rückgängig zu leerenden Dateien enthalten sind, ist der einzige zusätzliche TxF-Mehraufwand im Vergleich zu nicht transaktiven E/A-Anweisungen die Protokoll-Leerungen selbst. Protokoll leeren führt jedoch zu effizienten großen sequenziellen Schreibvorgängen, sodass die Leistungskosten minimal sind.
-   TxF ist für commit optimiert. Es wird erwartet, dass die meisten Transaktionen erfolgreich sind und kein Rollback ausgeführt werden müssen. Daher wird erwartet, dass alle Rückgängig-Datensätze für eine Transaktion nicht verwendet werden. Aus Leistungssicht sind TxF-Commitvorgänge schnell und Rollbacks ressourcenintensiv.
-   Ein Rollback ist ressourcenintensiver als ein Commit. Während des Rollbacks müssen alle Änderungen, die in der Transaktion vorgenommen wurden, nicht durchgeführt werden. Im Allgemeinen kann die Rollbackdauer ungefähr so lange sein, wie es für die ursprünglichen Änderungen gedauert hat. Wenn es z. B. 1 Sekunde ge dauerte, bis alle Änderungen vorgenommen wurden, kann es ungefähr eine Sekunde dauern, bis sie rückgängig gemacht wurden. Bei sehr langen Transaktionen kann ein Rollback zusätzliche Auswirkungen auf die Leistung haben. Beispielsweise kann die Systemstartzeit verzögert werden, wenn das System automatisch ein Rollback für eine Transaktion ausführen muss, falls das System nicht mehr reagiert und einen ungeplanten Neustart ausführen muss.

Die zusammenfassenden Schlussfolgerungen zur Leistung, die aus der vorherigen Liste gezogen werden können, lauten wie folgt:

-   Die Leistungskosten von TxF für Transaktionen im Zusammenhang mit Dateiüberschreibung können erheblich sein.
-   Die Leistungskosten von TxF für Transaktionen, die nur Metadatenvorgänge enthalten, können relativ niedrig sein, sofern große Transaktionen verwendet werden. Bei einer großen Transaktion gibt es viele Rückgängig-Datensätze für jeden Commitdatensatz.

## <a name="recommendations-for-best-performance"></a>Empfehlungen Optimale Leistung

Amortisieren Sie den TxF-Mehraufwand gegenüber größeren Transaktionen. Wenn Sie z. B. *N* Sätze von Änderungen vornehmen müssen, bei denen jede Änderung *M-Schritte* enthält, und Sie die Möglichkeit haben, dies entweder als *N* Transaktionen von *M-Schritten* durchzuführen oder alles als einzelne Transaktion mit *M* \* *N-Schritten* durchzuführen, wäre die zweite Option effizienter.

Berücksichtigen Sie die möglichen Auswirkungen sehr großer Transaktionen auf den Start. Wie bereits erwähnt, kann ein Rollback langsam sein und die Startzeit verzögern, wenn das System automatische Rollbacks als Startzeit ausführen muss. Je größer die Transaktion, desto länger die Verzögerung.

Behalten Sie Transaktionen für hauptsächlich Metadatenvorgänge bei. Für dies ist TxF optimiert, und im Allgemeinen ist die Leistung in etwa identisch mit der nicht transaktiven Datei-E/A für große Metadatentransaktionen. Beispiele für effiziente TxF-Metadatenfunktionen sind [**MoveFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) [**SetFileAttributesTransacted,**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda) [**CopyFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda) [**DeleteFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)und angefügte Schreibvorgänge (Aufrufe der [**WriteFile-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) wenn der Dateizeiger als am Ende der Datei steht, oder *EOF*). Ein Beispiel für ressourcenintensive Vorgänge ohne Metadaten sind Aufrufe der **WriteFile-Funktion,** wenn sich der Dateizeiger nicht am EOF befindet.

## <a name="summary-of-txf-performance-expectations"></a>Zusammenfassung der TxF-Leistungserwartungen

Bei direkt durchgeführten Updates ist das Überschreiben eines Dateiabschnitts viel langsamer als bei nicht transaktiven Datei-E/A-Vorgängen, während die TxF-Leistung für Dateisystemmetadatenvorgänge (z. B. Erstellen, Verschieben und Anfügen) mit der nicht transaktiven Datei-E/A für große Transaktionen vergleichbar ist.

 

 



