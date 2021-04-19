---
description: 'Weitere Informationen finden Sie hier: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350267"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

Die **JET_ERRCAT** Gruppe von Konstanten beschreibt Klassifizierungen oder Kategorien von Fehlern auf höherer Ebene. Diese Gruppe von Konstanten ermöglicht Anwendungen, die Standardbehandlung für eine Klassifizierung von Fehlern zu definieren, anstatt jeden einzelnen Fehlerfall einzeln zu behandeln. Außerdem wird sichergestellt, dass die Anwendung keine neuen Fehlerbedingungen behandelt, die in vorhandenen Klassifizierungen enthalten sind.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage-Engine. Diese Informationen können geändert werden.

Die **JET_ERRCAT** Konstanten werden wie folgt in einer bestimmten Hierarchie von Bedingungen und unter Bedingungen angeordnet:

|---Fehler |---Vorgang (Al) | |---schwerwiegend | |---IO | |---Ressource | |---Speicher | |---Kontingent | |---Datenträger | |---Daten | |---Beschädigung | |---inkonsistent | |---Fragmentierung | |---API |---Verwendung |---Status

In der folgenden Tabelle sind die **JET_ERRCAT** Konstanten aufgelistet, und es werden ggf. eine Beschreibung und Wiederherstellungs Informationen bereitstellt.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante/Wert</p></th>
<th><p>BESCHREIBUNG</p></th>
<th><p>Wiederherstellung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errcatUnknown 0</p></td>
<td><p>Ungültige Fehler Kategorie.</p></td>
<td><p>N/V.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>Die Kategorie der obersten Ebene (keine Fehler sollten dieser Klasse unterliegen).</p></td>
<td><p>Weitere Informationen finden Sie unter den spezifischen Fehler Konstanten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>Stellt Fehler dar, die zu einem beliebigen Zeitpunkt aufgrund von unkontrollierbaren Bedingungen auftreten können und oft temporär sind. Siehe Unterkategorien, falls angegeben.</p></td>
<td><p>Versuchen Sie es erneut, und informieren Sie den Operator, wenn der Fehler weiterhin auftritt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Stellt schwerwiegende Fehler dar, die auftreten, wenn Sie auftreten, riskieren, dass ESE nicht in einer sicheren (häufig transaktionalen) Weise fortgesetzt werden kann und dass die Daten beschädigt werden können.</p></td>
<td><p>Starten Sie die Instanz oder den Prozess neu. Wenn das Problem weiterhin besteht, informieren Sie den Operator.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Stellt e/a-Fehler dar, die vom Betriebssystem stammen und aus der ESE-Kontrolle bestehen. Diese Art von Fehler kann temporär sein.</p></td>
<td><p>Versuchen Sie es erneut. wenn der Fehler weiterhin auftritt, bitten Sie den Operator, den Datenträger zu überprüfen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Stellt eine Kategorie von Fehlern im Zusammenhang mit dem Mangel an Ressourcen Bedingungen dar.</p></td>
<td><p>Siehe Unterkategorien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Stellt einen Fehler dar, der durch unzureichenden Arbeitsspeicher verursacht wird.</p></td>
<td><p>Wiederholen Sie den Vorgang nach einer gewissen Zeit, geben Sie Arbeitsspeicher frei, oder beenden Sie den Vorgang.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Bestimmte &quot; spezialisierte &quot; Ressourcen befinden sich in Pools mit einer bestimmten Größe, sodass Sie Verluste dieser Ressourcen leichter erkennen können.</p></td>
<td><p>Die Anwendung sollte <strong>()</strong> bestätigen, um diese Probleme während der Entwicklung zu erkennen. Im Einzelhandels Code sollte die Anwendung dies jedoch als Speicherfehler behandeln.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Stellt einen Fehler dar, der durch unzureichenden Speicherplatz verursacht wurde.</p></td>
<td><p>Versuchen Sie es später erneut, um zu ermitteln, ob mehr Speicherplatz verfügbar ist, oder bitten Sie den Operator, Speicherplatz freizugeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Stellt eine Kategorie der obersten Ebene für Fehler im Zusammenhang mit Daten dar.</p></td>
<td><p>Siehe Unterkategorien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Stellt ein Beschädigungs Problem dar, das häufig ohne Korrekturmaßnahmen permanent ist.</p></td>
<td><p>Stellen Sie die Sicherung mithilfe des Reparatur Vorgangs für ESE-Hilfsprogramme wieder her (mit diesem Vorgang werden nur die Daten wieder hergestellt, die nach links/Verlust liegen). Außerdem kann die Wiederherstellung durchgeführt werden, wenn die Wiederherstellungsmethode (jetinit) verwendet wird, um Datenverluste zuzulassen (Weitere Informationen finden Sie unter <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Stellt einen Fehler dar, in dem sich die Datenbank und/oder die Protokolldateien in einem inkonsistenten Zustand befinden und nicht abgeglichen werden können. Dieser Fehler kann durch eine Anwendungs-/administratormishandelung verursacht werden.</p></td>
<td><p>Stellen Sie eine Wiederherstellung von einer Sicherung mit dem ESE-Hilfsprogramm-Reparaturvorgang durch Im Fall des <strong>Wiederherstellungs Vorgangs (jetinit)</strong> kann die Wiederherstellung durchgeführt werden, indem Datenverluste zugelassen werden. (Weitere Informationen finden Sie unter <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Stellt eine Klasse von Fehlern dar, in denen einige beibehaltene interne Ressourcen aufgetreten sind.</p></td>
<td><p>Bei Daten Bank Fehlern kann das Problem durch die Offline Defragmentierung behoben werden. Stellen Sie für die Protokolldateien zunächst alle angefügten Datenbanken in einem sauberen Herunterfahren wieder her, und löschen Sie dann alle Protokolldateien und den Prüfpunkt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Siehe Unterkategorien.</p></td>
<td><p>Siehe Unterkategorien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Stellt einen Verwendungs Fehler dar. Der Client Code hat nicht die richtigen Argumente an die <strong>Jet</strong> -API übergeben. Dieser Fehler wird bei einem Wiederholungsversuch beibehalten.</p></td>
<td><p>Der Client Code sollte die <strong>Assert ()</strong> -Methode verwenden, um sicherzustellen, dass diese Fehler Klasse nicht zurückgegeben wird, sodass Probleme während der Entwicklung abgefangen werden können. Im Einzelhandel sollte die Anwendung den Operator über den Fehler benachrichtigen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Stellt eine Klasse von Nachrichten dar, die von der API zurückgegeben werden können, um den Status der Datenbank zu beschreiben. Beispielsweise kann die <a href="gg294103(v=exchg.10).md">JetSeek ()</a> -Methode <strong>JET_errRecordNotFound</strong> zurückgeben, wenn der angeforderte Datensatz nicht gefunden wurde.</p></td>
<td><p>Variiert je nach API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Stellt Fehler dar, die von einer früheren Version der-Engine stammen. Diese Fehler sollten nicht von der aktuellen Engine zurückgegeben werden.</p></td>
<td><p>Unbekannt</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>Eine-Konstante, die das Ende der-Enumeration angibt.</p></td>
<td><p>N/V.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows 8-Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>

