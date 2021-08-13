---
description: 'Weitere Informationen zu: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bd72ecab62eeccb3ed7e586e2e793bdb9796f09a57686e70d9177eb496316760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254322"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

Die **JET_ERRCAT** Gruppe von Konstanten beschreibt Klassifizierungen auf höherer Ebene oder Fehlerkategorien. Diese Gruppe von Konstanten ermöglicht Es Anwendungen, die Standardbehandlung für eine Klassifizierung von Fehlern zu definieren, anstatt jeden Fehlerfall einzeln zu behandeln. Außerdem wird sichergestellt, dass die Anwendung keine neuen Fehlerbedingungen verarbeiten muss, die in vorhandenen Klassifizierungen enthalten sind.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage Engine. Diese Informationen können geändert werden.

Die **JET_ERRCAT** Konstanten werden wie folgt in einer bestimmten Hierarchie von Bedingungen und Unterbedingungen angeordnet:

|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- API |--- Usage |--- State

In der folgenden Tabelle werden die **JET_ERRCAT** Konstanten aufgelistet und ggf. eine Beschreibung und Wiederherstellungsinformationen angegeben.

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
<td><p>Eine ungültige Fehlerkategorie.</p></td>
<td><p>N/V.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>Die Kategorie der obersten Ebene (es sollten keine Fehler dieser Klasse auftreten).</p></td>
<td><p>Sehen Sie sich die spezifischen Fehlerkonstanten an.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>Stellt Fehler dar, die jederzeit aufgrund unkontrollierbarer Bedingungen auftreten können und häufig temporär sind. Weitere Informationen finden Sie unter Unterkategorien, sofern angegeben.</p></td>
<td><p>Wiederholen Sie den Vorgang, und informieren Sie den Operator, wenn der Fehler weiterhin auftritt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Stellt schwerwiegende Fehler dar, die bei auftreten, ein Risiko darstellen, dass ESE nicht sicher (häufig transaktional) fortgesetzt werden kann und Daten beschädigt werden können.</p></td>
<td><p>Starten Sie die Instanz oder den Prozess neu. Wenn das Problem weiterhin besteht, informieren Sie den Operator.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Stellt E/A-Fehler dar, die vom Betriebssystem stammen und außerhalb der Kontrolle von ESE liegen. Dieser Fehlertyp kann temporär sein.</p></td>
<td><p>Wiederholen Sie den Vorgang, und wenn der Fehler weiterhin auftritt, bitten Sie den Operator, den Datenträger zu überprüfen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Stellt eine Kategorie von Fehlern im Zusammenhang mit fehlenden Ressourcenbedingungen dar.</p></td>
<td><p>Weitere Informationen finden Sie unter Unterkategorien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Stellt einen Fehler dar, der durch unzureichenden Arbeitsspeicher verursacht wird.</p></td>
<td><p>Wiederholen Sie den Vorgang nach einem bestimmten Zeitraum, und stellen Sie Arbeitsspeicher frei, oder beenden Sie den Vorgang.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Bestimmte &quot; Spezielle Ressourcen befinden sich in Pools einer &quot; bestimmten Größe, wodurch es einfacher ist, Lecks dieser Ressourcen zu erkennen.</p></td>
<td><p>Die Anwendung sollte <strong>Assert()</strong> verwenden, um diese Probleme während der Entwicklung zu erkennen. Im Einzelhandelscode sollte die Anwendung dies jedoch als Speicherfehler behandeln.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Stellt einen Fehler dar, der durch fehlenden Speicherplatz verursacht wird.</p></td>
<td><p>Versuchen Sie es später noch mal, um zu ermitteln, ob mehr Speicherplatz verfügbar ist, oder bitten Sie den Operator, Speicherplatz freizubekommen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Stellt eine Kategorie der obersten Ebene für Datenfehler dar.</p></td>
<td><p>Weitere Informationen finden Sie unter Unterkategorien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Stellt ein Beschädigungsproblem dar, das oft ohne Korrekturmaßnahmen dauerhaft ist.</p></td>
<td><p>Stellen Sie die Wiederherstellung aus einer Sicherung mithilfe des Reparaturvorgangs der ESE-Hilfsprogramme her (bei diesem Vorgang werden nur die Daten wiederhergestellt, die links oder verlustbeschädigungig sind). Wenn die recovery(JetInit)-Methode verwendet wird, kann die Wiederherstellung auch durchgeführt werden, indem Datenverluste zugelassen werden (weitere Informationen finden Sie unter <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Stellt einen Fehler dar, bei dem sich die Datenbank- und/oder Protokolldateien in einem inkonsistenten Zustand befinden und nicht abgeglichen werden können. Dieser Fehler kann durch eine fehlerhafte Anwendungs-/Administratorhandling verursacht werden.</p></td>
<td><p>Wiederherstellung aus einer Sicherung mithilfe des Reparaturvorgangs der ESE-Hilfsprogramme (bei dem nur die Daten wiederhergestellt werden, die links oder verloren sind). Auch im Fall des <strong>Wiederherstellungsvorgangs (JetInit)</strong> kann die Wiederherstellung durchgeführt werden, indem Datenverlust zugelassen wird (weitere Informationen finden Sie unter <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Stellt eine Klasse von Fehlern dar, bei denen einige persistente interne Ressourcen nicht mehr vorhanden waren.</p></td>
<td><p>Bei Datenbankfehlern wird das Problem durch die Offlinedefragmentierung behoben. Stellen Sie für die Protokolldateien zunächst alle angefügten Datenbanken wieder her, um das Herunterfahren zu beenden, und löschen Sie dann alle Protokolldateien und den Prüfpunkt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Weitere Informationen finden Sie unter Unterkategorien.</p></td>
<td><p>Weitere Informationen finden Sie unter Unterkategorien.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Stellt einen Verwendungsfehler dar. Der Clientcode hat die richtigen Argumente nicht an die <strong>JET-API</strong> übergeben. Dieser Fehler wird bei wiederholungsversuchen beibehalten.</p></td>
<td><p>Clientcode sollte die <strong>Assert()-Methode</strong> verwenden, um sicherzustellen, dass diese Fehlerklasse nicht zurückgegeben wird, sodass Probleme während der Entwicklung abgefangen werden können. Im Einzelhandel sollte die Anwendung den Operator über den Fehler benachrichtigen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Stellt eine Klasse von Nachrichten dar, die die API zurückgeben kann, um den Zustand der Datenbank zu beschreiben. Beispielsweise kann die <a href="gg294103(v=exchg.10).md">JetSeek()-Methode</a> <strong>JET_errRecordNotFound</strong> zurückgeben, wenn der angeforderte Datensatz nicht gefunden wurde.</p></td>
<td><p>Variiert je nach API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Stellt Fehler dar, die aus einer früheren Version der Engine stammen. Diese Fehler sollten nicht von der aktuellen Engine zurückgegeben werden.</p></td>
<td><p>Unbekannt</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>Eine Konstante, die das Ende der Enumeration angibt.</p></td>
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
<td><p>Erfordert Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Deklariert in Esent.h.</p></td>
</tr>
</tbody>
</table>

