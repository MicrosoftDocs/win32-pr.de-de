---
description: Beschreibt die opportunistischen Sperren auf Ebene 1, Ebene 2, Batch und Filter.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Typen von opportunistischen Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a755a6ff766f5d19e13d4b269c1ba4bb9803e934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867691"
---
# <a name="types-of-opportunistic-locks"></a>Typen von opportunistischen Sperren

Die opportunistischen Lock-Vorgänge funktionieren mit vier Typen von opportunistischen Sperren: Ebene 1, Ebene 2, Batch und Filter. *Exklusive opportunistische Sperren* sind Ebene 1, Batch und Filter sperren. Wenn ein Thread eine beliebige Art von exklusiver Sperre für eine Datei hat, kann er nicht auch über eine Sperre der Ebene 2 für dieselbe Datei verfügen.

## <a name="level-1-opportunistic-locks"></a>Opportunistische Sperren der Ebene 1

Eine opportunistische Sperre der Ebene 1 in einer Datei ermöglicht einem Client, in der Datei zu lesen und sowohl Lese-als auch Schreib Daten aus der Datei lokal zu speichern. Solange der Client ausschließlich auf eine Datei zugreifen kann, besteht keine Gefahr, dass die Daten Zusammenstellung eine opportunistische Sperre der Ebene 1 darstellt.

Der Client kann eine opportunistische Sperre der Ebene 1 nach dem Öffnen einer Datei anfordern. Wenn die Datei nicht von einem anderen Client (oder keinem anderen Thread auf demselben Client) geöffnet ist, kann der Server die opportunistische Sperre erteilen. Der Client kann dann Lese-und Schreib Daten lokal aus der Datei Zwischenspeichern. Wenn die Datei von einem anderen Client geöffnet wurde, lehnt der Server die opportunistische Sperre ab, und der Client hat keine lokale Zwischenspeicherung. (Der Server kann die opportunistische Sperre auch aus anderen Gründen ablehnen, wie z. b. das unterstützen von opportunistischen Sperren.)

Wenn der Server eine Datei öffnet, die bereits über eine opportunistische Sperre der Ebene 1 verfügt, wird der Freigabe Status der Datei vom Server überprüft, bevor die opportunistische Sperre der Ebene 1 unterbrochen wird. Wenn der Server die Sperre nach dieser Prüfung unterbrochen hat, ist die Zeit, die der Client mit der früheren Sperre verbringt, den Schreib Cache zu leeren, die Zeit, die der Client zum Anfordern der Datei benötigt. Dieses Zeitaufwand bedeutet, dass opportunistische Sperren der Ebene 1 für Dateien vermieden werden sollten, die von vielen Clients geöffnet werden.

Da der Server jedoch den Freigabe Zustand überprüft, bevor die Sperre unterbrochen wird, wird der Server in dem Fall, in dem der Server eine offene Anforderung aufgrund eines Freigabe Konflikts ablehnt, nicht unterbrochen. Wenn Sie z. b. eine Datei geöffnet, die Freigabe für Schreibvorgänge verweigert und eine Sperre der Ebene 1 erhalten haben, verweigert der Server die Anforderung eines anderen Clients zum Öffnen der Datei zum Schreiben, bevor Sie die Sperre für die Datei sogar prüft. In dieser Instanz wird die opportunistische Sperre nicht abgebrochen.

Ein Beispiel für die Funktionsweise einer opportunistischen Sperre der Stufe 1 finden Sie unter Beispiel für eine opportunistische Sperre der Ebene 1. Weitere Informationen zum unterbrechen opportunistischer Sperren finden Sie unter unter [brechen von opportunistischen Sperren](breaking-opportunistic-locks.md).

## <a name="level-2-opportunistic-locks"></a>Opportunistische Sperren der Ebene 2

Eine opportunistische Sperre der Ebene 2 teilt einem Client mit, dass es mehrere gleichzeitige Clients einer Datei gibt, die er noch nicht geändert hat. Diese Sperre ermöglicht dem Client das Ausführen von Lesevorgängen und das Abrufen von Dateiattributen mithilfe von zwischengespeicherten oder Lesevorgängen für lokale Informationen, aber der Client muss alle anderen Anforderungen (z. b. für Schreibvorgänge) an den Server senden. Die Anwendung sollte die opportunistische Sperre der Ebene 2 verwenden, wenn Sie davon ausgehen, dass andere Anwendungen nach dem Zufallsprinzip in die Datei schreiben oder die Datei nach dem Zufallsprinzip oder sequenziell lesen möchten.

Eine opportunistische Sperre der Ebene 2 ähnelt einer opportunistischen Filter-Sperre. In den meisten Fällen sollte Ihre Anwendung die opportunistische Sperre der Ebene 2 verwenden. Verwenden Sie nur die Filter Sperre, wenn Sie keine Lesevorgänge für Lesevorgänge durchführen möchten, um Verstöße gegen den Freigabe Modus in der Zeitspanne zwischen dem Öffnen der Datei und dem Empfang der Sperre durch die Anwendung zu verursachen. Weitere Informationen finden Sie unter Filtern von opportunistischen Sperren und [Server Antwort zum Öffnen von Anforderungen für gesperrte Dateien](server-response-to-open-requests-on-locked-files.md).

Weitere Informationen zum unterbrechen opportunistischer Sperren finden Sie unter unter [brechen von opportunistischen Sperren](breaking-opportunistic-locks.md).

## <a name="batch-opportunistic-locks"></a>Opportunistische Sperren in Batches

Eine opportunistische Batch-Sperre bearbeitet Datei Öffnungen und-sperren. Beispielsweise kann die Batchdatei bei der Ausführung einer Batchdatei für jede Zeile der Datei geöffnet und geschlossen werden. Eine opportunistische Batch-Sperre öffnet die Batchdatei auf dem Server und hält Sie offen. Wenn der Befehlsprozessor die Batchdatei "öffnet" und "schließt", fängt der Netzwerk-Redirector die Befehle "Öffnen" und "Schließen" ab. Alle Server Empfangs Befehle sind die Befehle zum Suchen und lesen. Wenn der Client ebenfalls liest, empfängt der Server höchstens einmal eine bestimmte Lese Anforderung.

Beim Öffnen einer Datei, die bereits eine opportunistische Batch Sperre aufweist, wird der Freigabe Status der Datei vom Server überprüft, nachdem die Sperre unterbrochen wurde. Durch diese Überprüfung erhält der Inhaber der Sperre die Möglichkeit, den Cache zu leeren und das Datei Handle zu schließen. Bei einem während der Freigabe Überprüfung versuchten Öffnungsvorgang führt dies nicht zu einem Fehler bei der Freigabe Überprüfung, wenn der sperreninhaber die Sperre freigibt.

Ein Beispiel für die Funktionsweise einer Batch-opportunistischen Sperre finden Sie unter Beispiel für eine Batch-opportunistische Sperre. Weitere Informationen zum unterbrechen opportunistischer Sperren finden Sie unter unter [brechen von opportunistischen Sperren](breaking-opportunistic-locks.md).

## <a name="filter-opportunistic-locks"></a>Filtern von opportunistischen Sperren

Eine durch einen Filter opportunistische Sperre sperrt eine Datei, sodass Sie nicht für den Schreib-oder Lösch Zugriff geöffnet werden kann. Alle Clients müssen in der Lage sein, die Datei freizugeben. Filter sperren ermöglichen es Anwendungen, nicht eindringliche Filter Vorgänge für Datei Daten auszuführen (z. b. einen Compiler, der Quellcode oder ein Katalogisierungs Programm öffnet).

Eine opportunistische Filter-Sperre unterscheidet sich von einer opportunistischen Sperre der Ebene 2 darin, dass das Lesen von Lesevorgängen für Lesevorgänge ohne Freigabe Modus in der Zeitspanne zwischen dem Öffnen der Datei und dem Empfang der Sperre ermöglicht wird. Die opportunistische Filter-Sperre ist die beste Sperre, wenn es wichtig ist, anderen Clients Lesezugriff zu gewähren. In anderen Fällen sollte Ihre Anwendung eine opportunistische Sperre der Ebene 2 verwenden. Die opportunistische Sperre eines Filters unterscheidet sich von einer opportunistischen Batch-Sperre darin, dass es nicht zulässt, dass mehrere Öffnungen und Verarbeitungen vom Netzwerkredirector auf die Art und Weise durchgeführt werden, in der eine Batch opportunistische Sperre erfolgt

Die Anwendung sollte in drei Schritten eine opportunistische Filter Sperre für eine Datei anfordern:

1.  Verwenden Sie [**die Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Funktion", um ein Handle für die Datei zu öffnen, bei der der *desiredAccess* -Parameter auf NULL festgelegt ist, sodass kein Zugriff angegeben ist, und der *dwsharemode* -Parameter auf das **\_ \_ leseflag für die Dateifreigabe** festgelegt ist, um die Freigabe Das an dieser Stelle erhaltene Handle wird als Sperr Handle bezeichnet.
2.  Fordern Sie eine Sperre für dieses Handle mit dem Code für den Code der Code- [**\_ \_ \_ Oplock-Anforderung**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock) an.
3.  Wenn die Sperre erteilt wurde, öffnen Sie die Datei mit " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " erneut, wobei " *desiredAccess* " auf das **generische \_ leseflag** festgelegt ist. Legen Sie *dwsharemode* auf **das \_ \_ leseflag für die Dateifreigabe** fest, damit andere Benutzer die Datei lesen können, während Sie geöffnet ist. das Flag zum **Löschen der Datei \_ Freigabe \_** ermöglicht anderen Benutzern, die Datei zu löschen, während Sie geöffnet ist, oder beides. Das an dieser Stelle erhaltene Handle wird als Lese Handle bezeichnet.

Verwenden Sie das Lese handle, um aus dem Inhalt der Datei zu lesen oder in diesen zu schreiben.

Beim Öffnen einer Datei, die bereits eine opportunistische Filter Sperre aufweist, unterbricht der Server die Sperre und überprüft dann den Freigabe Zustand der Datei. Durch diese Überprüfung erhält der Client, der die frühere opportunistische Sperre aufrecht erhält, die Möglichkeit, alle zwischengespeicherten Daten abzubrechen und die Unterbrechung zu bestätigen. Bei einem während dieser Freigabe Überprüfung versuchten Öffnungsvorgang führt dies nicht dazu, dass die Freigabe Überprüfung fehlschlägt, wenn der frühere Sperr Inhaber die Sperre freigibt. Das Dateisystem hält den Öffnungsvorgang in Abeyance, bis der Besitzer der Sperre sowohl das Lese Handle als auch das Sperr handle schließt. Nachdem dies geschehen ist, kann die Anforderung des anderen Clients fortgesetzt werden.

Weitere Informationen zum unterbrechen opportunistischer Sperren finden Sie unter unter [brechen von opportunistischen Sperren](breaking-opportunistic-locks.md).

 

 
