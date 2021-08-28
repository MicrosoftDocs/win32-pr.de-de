---
description: Weitere Informationen finden Sie unter VistaParam-Felder.
title: VistaParam-Felder (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaParam fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_fields(v=EXCHG.10)
ms:contentKeyID: 55104336
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3684f6d50ba0ca107614276776e375bc90b32a0d0e3e0112dded07b6e9e5bcdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718850"
---
# <a name="vistaparam-fields"></a>VistaParam-Felder

Geschützte Member enthalten  
Geerbte Member enthalten  

Der [VistaParam-Typ](./vistaparam-class.md) macht die folgenden Member verfügbar.

## <a name="fields"></a>Felder

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></td>
<td>Dieser Parameter steuert die Anzahl der B+-Strukturressourcen, die von der -Instanz zwischengespeichert werden, nachdem die tabellen, die sie darstellen, von der Anwendung geschlossen wurden. Große Werte für diesen Parameter führen dazu, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, erhöht jedoch die Geschwindigkeit, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann. Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335289(v=exchg.10).md">Configuration</a></td>
<td>Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar. Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameterwerte auf ihre Standardwerte für diese Konfiguration zurückgesetzt. Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden globale Systemparameter nicht auf ihre Standardwerte zurückgesetzt. Kleine Konfiguration (0): Die Datenbank-Engine ist für die Speichernutzung optimiert. Legacykonfiguration (1): Die Datenbank-Engine hat ihre herkömmlichen Standardwerte.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></td>
<td>Dieser Parameter wird verwendet, um zu steuern, wann die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder zurückgibt. Dieser Parameter wird in Verbindung mit <a href="dn335289(v=exchg.10).md">Configuration</a> verwendet, um zu verhindern, dass einige Systemparameter von den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335291(v=exchg.10).md">EnableFileCache</a></td>
<td>Aktivieren Sie die Verwendung des Betriebssystemdateicaches für alle verwalteten Dateien.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335381(v=exchg.10).md">EnableViewCache</a></td>
<td>Aktivieren Sie die Verwendung von Speicherzuordnungsdatei-E/A für Datenbankdateien.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335292(v=exchg.10).md">KeyMost</a></td>
<td>Dieser schreibgeschützte Parameter gibt die maximal zulässige Indexschlüssellänge an, die für die aktuelle Datenbankseitengröße ausgewählt werden kann (wie von <a href="hh596135(v=exchg.10).md">DatabasePageSize konfiguriert).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></td>
<td>Dieser Parameter bietet Abwärtskompatibilität mit den Dateinamenskonventionen früherer Versionen der Datenbank-Engine.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335294(v=exchg.10).md">TableClass10Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 10 zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335385(v=exchg.10).md">TableClass11Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 11 zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335387(v=exchg.10).md">TableClass12Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 12 zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335388(v=exchg.10).md">TableClass13Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 13 zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335295(v=exchg.10).md">TableClass14Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 14 zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335390(v=exchg.10).md">TableClass15Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 15 zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335297(v=exchg.10).md">TableClass1Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 1 zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335389(v=exchg.10).md">TableClass2Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 2 zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335296(v=exchg.10).md">TableClass3Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 3 zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335395(v=exchg.10).md">TableClass4Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 4 zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335401(v=exchg.10).md">TableClass5Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 5 zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335298(v=exchg.10).md">TableClass6Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 6 zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335402(v=exchg.10).md">TableClass7Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 7 zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335299(v=exchg.10).md">TableClass8Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 8 zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335404(v=exchg.10).md">TableClass9Name</a></td>
<td>Legen Sie den Namen fest, der der Tabellenklasse 9 zugeordnet ist.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[VistaParam-Klasse](./vistaparam-class.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
