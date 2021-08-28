---
description: 'Weitere Informationen finden Sie unter: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: dee8dc7850cf69957c360253b942117739fe405b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987553"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

Die **JET_ERRCAT** Gruppe von Konstanten beschreibt Klassifizierungen auf höherer Ebene oder Fehlerkategorien. Mit dieser Gruppe von Konstanten können Anwendungen eine Standardbehandlung für eine Klassifizierung von Fehlern definieren, anstatt jeden Fehlerfall einzeln zu behandeln. Außerdem wird sichergestellt, dass die Anwendung keine neuen Fehlerbedingungen verarbeiten muss, die in vorhandenen Klassifizierungen enthalten sind.

Hinweis: Diese Dokumentation basiert auf einer vorläufigen Version der Extensible Storage Engine. Diese Informationen können geändert werden.

Die **JET_ERRCAT** konstanten Werden wie folgt in einer bestimmten Hierarchie von Bedingungen und Unterbedingungen angeordnet:

|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- API |--- Usage |--- State

In der folgenden Tabelle sind die **JET_ERRCAT** konstanten Konstanten und ggf. eine Beschreibung und Wiederherstellungsinformationen aufgeführt.


| <p>Konstante/Wert</p> | <p>BESCHREIBUNG</p> | <p>Wiederherstellung</p> | 
|-----------------------|--------------------|-----------------|
| <p>JET_errcatUnknown 0</p> | <p>Eine ungültige Fehlerkategorie.</p> | <p>N/V.</p> | 
| <p>JET_errcatError 1</p> | <p>Die Kategorie der obersten Ebene (es sollten keine Fehler dieser Klasse auftreten).</p> | <p>Sehen Sie sich die spezifischen Fehlerkonst constants an.</p> | 
| <p>JET_errcatOperation 2</p> | <p>Stellt Fehler dar, die jederzeit aufgrund von unkontrollierbaren Bedingungen auftreten können und häufig temporär sind. Siehe Unterkategorien, falls angegeben.</p> | <p>Wiederholen Sie den Vorgang, und informieren Sie den Operator, wenn der Fehler weiterhin auftritt.</p> | 
| <p>JET_errcatFatal 3</p> | <p>Stellt schwerwiegende Fehler dar, die bei auftreten ein Risiko darstellen, dass ESE nicht auf sichere (häufig transaktionale) Weise fortgesetzt werden kann und Daten beschädigt werden können.</p> | <p>Starten Sie die Instanz oder den Prozess neu. Wenn das Problem weiterhin besteht, informieren Sie den Operator.</p> | 
| <p>JET_errcatIO 4</p> | <p>Stellt E/A-Fehler dar, die vom Betriebssystem stammen und nicht von ESE kontrolliert werden. Diese Art von Fehler kann temporär sein.</p> | <p>Wiederholen Sie den Vorgang, und bitten Sie den Operator, den Datenträger zu überprüfen, wenn der Fehler weiterhin auftritt.</p> | 
| <p>JET_errcatResource 5</p> | <p>Stellt eine Kategorie von Fehlern im Zusammenhang mit fehlenden Ressourcenbedingungen dar.</p> | <p>Siehe Unterkategorien.</p> | 
| <p>JET_errcatMemory 6</p> | <p>Stellt einen Fehler dar, der durch fehlenden Arbeitsspeicher verursacht wird.</p> | <p>Wiederholen Sie den Vorgang nach einem bestimmten Zeitraum, geben Sie Arbeitsspeicher frei, oder beenden Sie den Vorgang.</p> | 
| <p>JET_errcatQuota 7</p> | <p>Bestimmte "spezielle" Ressourcen befinden sich in Pools einer bestimmten Größe, wodurch es einfacher ist, Lecks dieser Ressourcen zu erkennen.</p> | <p>Die Anwendung sollte <strong>Assert() verwenden,</strong> um diese Probleme während der Entwicklung zu erkennen. Im Einzelhandelscode sollte die Anwendung dies jedoch als Speicherfehler behandeln.</p> | 
| <p>JET_errcatDisk 8</p> | <p>Stellt einen Fehler dar, der durch fehlenden Speicherplatz auf dem Datenträger verursacht wird.</p> | <p>Versuchen Sie es später erneut, um zu ermitteln, ob mehr Speicherplatz verfügbar ist, oder bitten Sie den Operator, Speicherplatz frei zu geben.</p> | 
| <p>JET_errcatData 9</p> | <p>Stellt eine Kategorie der obersten Ebene für Datenfehler dar.</p> | <p>Siehe Unterkategorien.</p> | 
| <p>JET_errcatCorruption 10</p> | <p>Stellt ein Beschädigungsproblem dar, das oft dauerhaft ohne Korrekturmaßnahmen ist.</p> | <p>Wiederherstellen aus einer Sicherung mithilfe des Reparaturvorganges der ESE-Hilfsprogramme (bei diesem Vorgang werden nur die Daten wiederhergestellt, die links oder verlustig sind). Wenn die Recovery(JetInit)-Methode verwendet wird, kann die Wiederherstellung auch durchgeführt werden, indem Datenverluste ermöglicht <a href="gg269296(v=exchg.10).md">werden (weitere</a>Informationen finden Sie unter JET_bitReplayIgnoreLostLogs .</p> | 
| <p>JET_errcatInconsistent 11</p> | <p>Stellt einen Fehler dar, bei dem sich die Datenbank- und/oder Protokolldateien in einem inkonsistenten Zustand befinden und nicht abgeglichen werden können. Dieser Fehler kann durch eine fehlgeleitete Anwendungs-/Administratorbehandlung verursacht werden.</p> | <p>Wiederherstellen aus einer Sicherung mithilfe des Reparaturvorgang für ESE-Hilfsprogramme (bei dem nur die Daten wiederhergestellt werden, die links oder verlustig sind). Im Fall des <strong>Wiederherstellungsvorgang (JetInit)</strong> kann die Wiederherstellung auch durchgeführt werden, indem Datenverluste ermöglicht <a href="gg269296(v=exchg.10).md">werden (weitere</a>Informationen finden Sie unter JET_bitReplayIgnoreLostLogs .</p> | 
| <p>JET_errcatFragmentation 12</p> | <p>Stellt eine Klasse von Fehlern dar, bei der einige persistente interne Ressourcen nicht mehr verwendet werden.</p> | <p>Bei Datenbankfehlern wird das Problem durch die Offlinedefragmentierung behoben. Stellen Sie für die Protokolldateien zunächst alle angefügten Datenbanken nach einem bereinigten Herunterfahren wieder wieder auf, und löschen Sie dann alle Protokolldateien und den Prüfpunkt.</p> | 
| <p>JET_errcatApi 13</p> | <p>Siehe Unterkategorien.</p> | <p>Siehe Unterkategorien.</p> | 
| <p>JET_errcatUsage 14</p> | <p>Stellt einen Verwendungsfehler dar. Der Clientcode hat nicht die richtigen Argumente an die <strong>JET-API</strong> übergeben. Dieser Fehler wird bei einem Wiederholungsversuch beibehalten.</p> | <p>Clientcode sollte die <strong>Assert()-Methode</strong> verwenden, um sicherzustellen, dass diese Fehlerklasse nicht zurückgegeben wird, sodass Probleme während der Entwicklung erfasst werden können. Im Einzelhandel sollte die Anwendung den Operator über den Fehler benachrichtigen.</p> | 
| <p>JET_errcatState 15</p> | <p>Stellt eine Klasse von Nachrichten dar, die die API zurückgeben kann, um den Status der Datenbank zu beschreiben. Beispielsweise gibt die <a href="gg294103(v=exchg.10).md">JetSeek()-Methode</a> möglicherweise JET_errRecordNotFound, <strong>wenn</strong> der angeforderte Datensatz nicht gefunden wurde.</p> | <p>Variiert je nach API.</p> | 
| <p>JET_errcatObsolete 16</p> | <p>Stellt Fehler aus einer früheren Version der Engine dar. Diese Fehler sollten nicht von der aktuellen Engine zurückgegeben werden.</p> | <p>Unbekannt</p> | 
| <p>JET_errcatMax 17</p> | <p>Eine Konstante, die das Ende der Enumeration angibt.</p> | <p>N/V.</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows 8 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 


