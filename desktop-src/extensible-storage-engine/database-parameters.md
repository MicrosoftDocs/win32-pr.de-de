---
description: Weitere Informationen finden Sie unter Datenbankparameter.
title: Datenbankparameter
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13de02c7d322933f64361cfdabcb8f95ead837ad915ad69c3961a8b8874d5b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117560"
---
# <a name="database-parameters"></a>Datenbankparameter


_**Gilt für:** Windows | Windows Server_

## <a name="database-parameters"></a>Datenbankparameter

Dieses Thema enthält Parameter, die für die Datenbank verwendet werden.

*JET_paramCheckFormatWhenOpenFail*  
44  

Wenn dieser Parameter festgelegt ist, gibt [JetInit](./jetinit-function.md) einen speziellen Fehler zurück, wenn eine Datenbank oder ein Transaktionsprotokoll aus einer früheren Version der Datenbank-Engine geöffnet wird. Diese Fehler sind:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fehler</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errDatabase200Format</p></td>
<td><p>Die Datenbank- und/oder Transaktionsprotokolldateien wurden mit der Datenbank-Engine in Windows NT 3.51 erstellt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format</p></td>
<td><p>Die Datenbank- und/oder Transaktionsprotokolldateien wurden mit der Datenbank-Engine in einer Testversion vor Windows NT Server 4.0 erstellt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format</p></td>
<td><p>Die Datenbank- und/oder Transaktionsprotokolldateien wurden mit der Datenbank-Engine in Windows NT Server 4.0 erstellt.</p></td>
</tr>
</tbody>
</table>


**Windows Vista:**  Für Windows Vista und höher ist dieser Parameter veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Richtig</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramDatabasePageSize*  
64  

Dieser Parameter konfiguriert die Seitengröße für die Datenbank. Die Seitengröße ist die kleinste Einheit der Speicherplatzzuweisung, die für eine Datenbankdatei möglich ist. Die Größe der Datenbankseite ist ebenfalls sehr wichtig, da sie die Obergrenze für die Größe eines einzelnen Datensatzes in der Datenbank fest legt.

**Hinweis:** Derzeit wird pro Prozess nur eine Datenbankseitengröße unterstützt. Wenn Sie sich also in einem einzigen Prozess befinden, der verschiedene Anwendungen enthält, die die Datenbank-Engine verwenden, müssen sich alle auf eine Datenbankseitengröße einigen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>4096</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>2048, 4096, 8192</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramDbExtensionSize*  
18  

Dieser Parameter steuert den Speicherplatz, der einer Datenbankdatei jedes Mal hinzugefügt wird, wenn sie wachsen muss, um mehr Daten aufnehmen zu können. Die Größe befindet sich auf Datenbankseiten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexChecking*  
45  

Wenn dieser Parameter true ist, wird jede Datenbank zur [JetAttachDatabase-Zeit](./jetattachdatabase-function.md) auf Indizes über Unicode-Schlüsselspalten überprüft, die mit einer älteren Version der NLS-Bibliothek im Betriebssystem erstellt wurden. Dies muss erfolgen, da die Datenbank-Engine die von [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) generierten Sortierschlüssel beibehält und sich der Wert dieser Sortierschlüssel von Release zu Release ändert.

Wenn erkannt wird, dass sich ein primärer Index in diesem Zustand befindet, wird [jetAttachDatabase](./jetattachdatabase-function.md) immer mit einem Fehler JET_errPrimaryIndexCorrupted.

Wenn sekundäre Indizes in diesem Zustand erkannt werden, gibt es zwei mögliche Ergebnisse. Wenn JET_bitDbDeleteCorruptIndexes [An JetAttachDatabase](./jetattachdatabase-function.md) übergeben wurde, werden diese Indizes gelöscht und JET_wrnCorruptIndexDeleted [von JetAttachDatabase zurückgegeben.](./jetattachdatabase-function.md) Diese Indizes müssen von Ihrer Anwendung neu erstellt werden. Wenn JET_bitDbDeleteCorruptIndexes nicht an [JetAttachDatabase](./jetattachdatabase-function.md) übergeben wurde, kann der Aufruf nicht erfolgreich JET_errSecondaryIndexCorrupted.

**Hinweis:** Es wird dringend empfohlen, dass dieser Parameter von Ihrer Anwendung auf True festgelegt wird.

**Hinweis:** Es wird dringend empfohlen, dass Anwendungen die Verwendung von Unicode-Schlüsselspalten in ihren Primärschlüsselindizes (gruppiert) vermeiden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Falsch</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexCleanup*  
54  

Wenn dieser Parameter auf TRUE festgelegt ist, kann die Datenbank-Engine Indizes automatisch zur [JetInit-Zeit](./jetinit-function.md) über Unicode-Schlüsselspalten bereinigen, um Änderungen am Datenbankformat zu vermeiden, die durch Änderungen an der NLS-Bibliothek in Windows. Solche Änderungen werden routinemäßig an der NLS-Bibliothek vorgenommen, um Unterstützung für neue Sprachen hinzuzufügen, einer Sprache fehlende Zeichen hinzuzufügen, einer Sprache eine Sortierungsreihen reihenfolge hinzuzufügen oder Fehler in der Sortierungsreihen reihenfolge einer Sprache zu beheben. Diese Änderungen wirken sich auf die von [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) erzeugten Sortierschlüssel aus, die von der Datenbank-Engine als Komponenten von Indexschlüsseln beibehalten werden.

Es ist wichtig zu wissen, dass es möglich ist, dass die Änderungen am Index so groß sind, dass eine inkrementelle Bereinigung nicht möglich ist. In diesem Fall wird der Index wie von **JET_paramEnableIndexChecking.**

**Hinweis:** Es wird dringend empfohlen, diesen Parameter **und JET_paramEnableIndexChecking** Anwendung auf **True** zu setzen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Richtig</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Server 2003 und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramOneDatabasePerSession*  
102  

Wenn dieser Parameter true ist, kann nur eine Datenbank mit [JetOpenDatabase](./jetopendatabase-function.md) von einer bestimmten Sitzung gleichzeitig geöffnet werden. Die temporäre Datenbank ist von dieser Einschränkung ausgeschlossen.

**Windows XP und Windows Server 2003:**  Dieser Parameter wird nur auf Windows XP und Windows Server 2003 geschrieben.

**Windows Vista:**  Dieser Parameter verhält sich normal wie Windows Vista.

**Hinweis:**  Dieser Parameter ist nur write.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Falsch</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p>
<p><strong>Windows Vista:</strong>  Für Windows Vista und höher: Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableOnlineDefrag*  
35  

Dieser Parameter steuert das Verhalten der Onlinedefragmentierung, wenn sie mit [JetDefragment initiiert wird.](./jetdefragment-function.md) Weitere Informationen [finden Sie unter JetDefragment.](./jetdefragment-function.md)

Windows 2000: Am Windows 2000 war dieser Parameter ein einfacher boolescher Wert, der die Onlinedefragmentierung beim Initiierten durch [JetDefragment](./jetdefragment-function.md)einhing. Wenn true **festgelegt ist,** wird die Onlinedefragmentierung für die Datensätze der einzelnen Tabellen in der Datenbank ausgeführt.

**Windows XP:**  Bei Windows XP und späteren Versionen kann dieser Parameter auf eine oder mehrere der folgenden Optionen festgelegt werden:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Option</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_OnlineDefragDisable</p></td>
<td><p>Führen Sie keine Onlinedefragmentierung durch. Dies ist die binäre Entsprechung der Windows 2000-Einstellung false für diesen Parameter.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAllOBSOLETE</p></td>
<td><p>Führen Sie eine vollständige Onlinedefragmentierung durch. Dies ist die binäre Entsprechung zur Windows 2000-Einstellung true für diesen Parameter.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragDatabases</p></td>
<td><p>Führen Sie die Onlinedefragmentierung der Datensätze jeder Tabelle in der Datenbank aus.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragSpaceTrees</p></td>
<td><p>Führen Sie die Onlinedefragmentierung der Raumstrukturen jeder Tabelle in der Datenbank aus.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragStreamingFiles</p></td>
<td><p>Dieser Parameter wird zur Unterstützung der Microsoft Exchange-Infrastruktur verwendet und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAll</p></td>
<td><p>Führen Sie eine vollständige Onlinedefragmentierung durch. Dies ist die konzeptionelle Entsprechung zur Windows 2000-Einstellung true für diesen Parameter.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000:</strong>  STIMMT</p>
<p><strong>Windows XP: Für Windows XP und höher:</strong> JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p><strong>Windows 2000:</strong>  Boolean</p>
<p><strong>Windows XP und höher:</strong>  JET_GRBIT (ganze Zahl)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong>  False, True</p>
<p><strong>Windows XP und höher:</strong> 0 – JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramPageFragment*  
20  

Dieser Parameter ist der Schwellenwert, den die Datenbank-Engine verwendet, um die Fragmentierung des freien Speicherplatzes zu steuern. Die Größe wird auf Datenbankseiten angezeigt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramRecordUpgradeDirtyLevel*  
78

Dieser Parameter steuert, wie aggressiv der Datenbankseitencache-Manager eine Datenbankseite schreibt, für die eine konvertierungsseitige Formatkonvertierung durchgeführt wurde. Diese Formatkonvertierungen erfolgen während des Ladens von Seiten aus einer Datenbank, die mit der Windows 2000-Datenbank-Engine erstellt, aber von einer Windows XP oder einer späteren Version der Datenbank-Engine verwendet wurde.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-3</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und höhere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramWaypointLatency*  
153  

Die Latenzzeit (in Protokollen) hinter dem Protokoll tip/highest committed zum Zurückstellen von Datenbankseitenlöschungen. Die Aktivierung dieser Latenz kann die Datenbankwiederherstellung im Falle eines schwerwiegenden Verlusts der letzten Protokolldatei ermöglichen. Weitere Informationen finden Sie unter JET_bitReplayIgnoreLostLogs.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-1023</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTrees*  
160  

Aktivieren/Deaktivieren der automatischen sequenziellen B-Strukturdefragmentierung.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-1</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Bestimmt, wie häufig die B-Strukturdichte überprüft wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0–Max. ganze Zahl</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramIOThrottlingTimeQuanta*  
162  

Maximale Zeit in Millisekunden, die der E/A-Drosselungsmechanismus eine Aufgabe zur Ausführung zur Folge hat, damit sie als "abgeschlossen" betrachtet wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>125</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows 7</p></td>
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
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
