---
description: Beschreibt die sperrenden Sperre für Ebene 1, Ebene 2, Batch und Filter.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Typen von deterministischen Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dc450b038013454ea2d0ddd9c78a701dc8f977b4fa3b0aca7cdda076e8b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047850"
---
# <a name="types-of-opportunistic-locks"></a>Typen von deterministischen Sperren

Die deterministischen Sperrenvorgänge funktionieren mit vier Typen von deterministischen Sperren: Ebene 1, Ebene 2, Batch und Filter. *Exklusive deterministische Sperren sind* Sperren auf Ebene 1, Batch und Filter. Wenn ein Thread über eine art exklusive Sperre für eine Datei verfügt, kann er nicht auch eine Sperre der Ebene 2 für dieselbe Datei haben.

## <a name="level-1-opportunistic-locks"></a>Level 1– ( (1) – "Deterministische Sperren"

Mit einer Sperre der Ebene 1 für eine Datei kann ein Client in der Datei vorlesen und Sowohl Read-Ahead- als auch Schreibdaten aus der Datei lokal zwischenspeichern. Solange der Client den alleinigen Zugriff auf eine Datei hat, besteht keine Gefahr für die Datenkoherenz bei der Bereitstellung einer deterministischen Sperre der Ebene 1.

Der Client kann nach dem Öffnen einer Datei eine Sperre der Ebene 1 anfordern. Wenn die Datei von keinem anderen Client (oder keinem anderen Thread auf demselben Client) geöffnet ist, kann der Server die Sperre gewähren. Der Client kann dann Lese- und Schreibdaten aus der Datei lokal zwischenspeichern. Wenn die Datei von einem anderen Client geöffnet wurde, verweigert der Server die Sperre, und der Client führt keine lokale Zwischenspeicherung durch. (Der Server kann die deterministische Sperre auch aus anderen Gründen ablehnen, z. B. wenn er keine deterministischen Sperren unterstützt.)

Wenn der Server eine Datei öffnet, für die bereits eine deterministische Sperre der Ebene 1 vorhanden ist, überprüft der Server den Freigabezustand der Datei, bevor sie die Sperre auf Ebene 1 unterbricht. Wenn der Server die Sperre nach dieser Untersuchung unterbricht, ist die Zeit, die der Client mit der früheren Sperre damit verbringt, seinen Schreibcache zu leeren, die Zeit, die der Client, der die Datei anfing, warten muss. Dieser Zeitaufwand bedeutet, dass level 1-bare Sperren für Dateien vermieden werden sollten, die von vielen Clients geöffnet werden.

Da der Server jedoch den Freigabezustand überprüft, bevor er die Sperre aufbricht, wird die Sperre nicht durch den Server bricht, wenn der Server eine offene Anforderung aufgrund eines Freigabekonflikts verweigert. Wenn Sie z. B. eine Datei geöffnet, die Freigabe für Schreibvorgänge verweigert und eine Sperre der Ebene 1 erhalten haben, verweigert der Server die Anforderung eines anderen Clients, die Datei zum Schreiben zu öffnen, bevor er ihre Sperre für die Datei untersucht. In diesem Fall wird ihre deterministische Sperre nicht unterbrochen.

Ein Beispiel für die Funktionsweise einer deterministischen Sperre der Ebene 1 finden Sie unter Level 1 – Beispiel für eine deterministische Sperre. Weitere Informationen zum Aufbrechen von deterministischen Sperren finden Sie unter [Breaking Deterministic Locks](breaking-opportunistic-locks.md).

## <a name="level-2-opportunistic-locks"></a>Level 2 – Deterministische Sperren

Eine Sperre der Ebene 2 informiert einen Client darüber, dass es mehrere gleichzeitige Clients einer Datei gibt und dass sie noch nicht geändert wurde. Diese Sperre ermöglicht es dem Client, Lesevorgänge durchzuführen und Dateiattribute mithilfe von zwischengespeicherten oder read-ahead-lokalen Informationen zu erhalten. Der Client muss jedoch alle anderen Anforderungen (z. B. für Schreibvorgänge) an den Server senden. Ihre Anwendung sollte die Sperre der Ebene 2 verwenden, wenn Sie erwarten, dass andere Anwendungen nach dem Zufallsprinzip in die Datei schreiben oder die Datei nach dem Zufallsprinzip oder sequenziell lesen.

Eine deterministische Sperre der Ebene 2 ähnelt stark einer filterkantistischen Sperre. In den meisten Fällen sollte Ihre Anwendung die deterministische Sperre der Ebene 2 verwenden. Verwenden Sie die Filtersperre nur, wenn Sie nicht möchten, dass geöffnete Vorgänge zum Lesen verstöße gegen den Freigabemodus in der Zeitspanne zwischen dem Öffnen der Datei und dem Empfang der Sperre durch Ihre Anwendung verursachen. Weitere Informationen finden Sie unter Filtern von sperrbaren Sperren und [Serverantwort auf offene Anforderungen für gesperrte Dateien.](server-response-to-open-requests-on-locked-files.md)

Weitere Informationen zum Aufbrechen von deterministischen Sperren finden Sie unter [Breaking Deterministic Locks](breaking-opportunistic-locks.md).

## <a name="batch-opportunistic-locks"></a>Batch-Sperre

Eine batch-sperre bearbeitet Datei öffnen und schließende Dateien. Bei der Ausführung einer Batchdatei kann die Batchdatei beispielsweise einmal für jede Zeile der Datei geöffnet und geschlossen werden. Eine batch-sperre öffnet die Batchdatei auf dem Server und hält sie geöffnet. Wenn der Befehlsprozessor die Batchdatei "öffnet" und "schließt", fängt der Netzwerkumleitung die Befehle zum Öffnen und Schließen ab. Alle Server empfangen die Such- und Lesebefehle. Wenn der Client auch weiter liest, empfängt der Server mindestens einmal eine bestimmte Leseanforderung.

Beim Öffnen einer Datei, die bereits über eine batch-sperre verfügt, überprüft der Server den Freigabestatus der Datei, nachdem die Sperre bricht. Diese Überprüfung gibt dem Besitzer der Sperre die Möglichkeit, das Leeren des Caches und das Schließen des Dateihandlings abgeschlossen zu haben. Ein während der Freigabeüberprüfung versuchter Vorgang zum Öffnen führt nicht dazu, dass die Freigabeprüfung fehlschlägt, wenn der Sperreninhaber die Sperre auflässt.

Ein Beispiel für die Funktionsweise einer batch-deterministischen Sperre finden Sie unter Batch-Beispiel für die deterministische Sperre. Weitere Informationen zum Aufbrechen von deterministischen Sperren finden Sie unter [Breaking Deterministic Locks](breaking-opportunistic-locks.md).

## <a name="filter-opportunistic-locks"></a>Filtern von symbolistischen Sperren

Eine filternististische Sperre sperrt eine Datei, sodass sie weder für Schreib- noch für Löschzugriff geöffnet werden kann. Die Datei muss von allen Clients gemeinsam verwendet werden können. Filtersperren ermöglichen Es Anwendungen, nicht inintrusive Filtervorgänge für Dateidaten durchzuführen (z. B. einen Compiler, der Quellcode öffnet, oder ein Katalogisierungsprogramm).

Eine filterbasierte Sperre unterscheidet sich von einer deterministischen Sperre der Ebene 2, da sie das Öffnen von Lesevorgängen ohne Freigabemodusverletzungen in der Zeitspanne zwischen dem Öffnen der Datei und dem Empfang der Sperre durch Ihre Anwendung ermöglicht. Die filteroptistische Sperre ist die beste Sperre, wenn es wichtig ist, anderen Clients Lesezugriff zu ermöglichen. In anderen Fällen sollte Ihre Anwendung eine deterministische Sperre der Ebene 2 verwenden. Eine filteroptistische Sperre unterscheidet sich von einer batch-deterministischen Sperre, da sie nicht zu lässt, dass mehrere Öffnungen und Schließungen vom Netzwerkumleitungsor wie eine batch-sperre behandelt werden.

Ihre Anwendung sollte in drei Schritten eine filteroptistische Sperre für eine Datei anfordern:

1.  Verwenden Sie die [**CreateFile-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um ein Handle für die Datei zu öffnen, bei dem der *DesiredAccess-Parameter* auf 0 (null) festgelegt ist und der *dwShareMode-Parameter* auf das **FILE SHARE \_ \_ READ-Flag** festgelegt ist, um die Freigabe zum Lesen zu ermöglichen. Das an diesem Punkt erhaltene Handle wird als Sperrhand handle bezeichnet.
2.  Fordern Sie mit dem [**FSCTL \_ REQUEST \_ FILTER \_ OPLOCK-Steuerungscode**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock) eine Sperre für dieses Handle an.
3.  Wenn die Sperre gewährt wird, verwenden Sie [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um die Datei erneut zu öffnen, während *DesiredAccess* auf das **GENERIC \_ READ-Flag festgelegt** ist. Legen *Sie dwShareMode* auf das **FILE SHARE \_ \_ READ-Flag** fest, damit andere Benutzer die Datei lesen können, während Sie sie geöffnet haben, das **FILE SHARE \_ \_ DELETE-Flag,** damit andere Personen die Datei zum Löschen markieren können, während Sie sie geöffnet haben, oder beides. Das an diesem Punkt erhaltene Handle wird als Lesehandles bezeichnet.

Verwenden Sie das Lesehandles, um den Inhalt der Datei zu lesen oder in diesen zu schreiben.

Wenn Sie eine Datei öffnen, die bereits über eine filteroptistische Sperre verfügt, unterbricht der Server die Sperre und überprüft dann den Freigabezustand der Datei. Diese Überprüfung gibt dem Client, der die frühere, nicht zufällige Sperre gehalten hat, die Möglichkeit, alle zwischengespeicherten Daten zu verabbrechen und die Unterbrechung zu bestätigen. Ein während dieser Freigabeüberprüfung versuchter Öffnen-Vorgang führt nicht dazu, dass die Freigabeprüfung fehlschlägt, wenn der frühere Sperreninhaber die Sperre auflässt. Das Dateisystem hält den Geöffnetvorgang an, bis der Besitzer der Sperre sowohl das Lesehandles als auch das Sperrhandles schließt. Danach kann die offene Anforderung des anderen Clients fortgesetzt werden.

Weitere Informationen zum Aufbrechen von deterministischen Sperren finden Sie unter [Breaking Deterministic Locks](breaking-opportunistic-locks.md).

 

 
