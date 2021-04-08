---
description: 'Weitere Informationen finden Sie hier: vistaparam-Member'
title: Vistaparam-Member (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaParam members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_members(v=EXCHG.10)
ms:contentKeyID: 55104333
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c56c8ad3a64eb08654ee893e86683e95e32af443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861928"
---
# <a name="vistaparam-members"></a>Vistaparam-Member

Geschützte Member einschließen  
Geerbte Member einschließen  

System Parameter, die der Vista-Version von ESENT hinzugefügt wurden.

Der [vistaparam](./vistaparam-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="fields"></a>Felder

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335379(v=exchg.10).md">Cachedclosedtables</a></td>
<td>Dieser Parameter steuert die Anzahl der B +-strukturressourcen, die von der-Instanz zwischengespeichert wurden, nachdem die Tabellen, die Sie darstellen, von der Anwendung geschlossen wurden. Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, aber die Geschwindigkeit erhöht, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann. Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335289(v=exchg.10).md">Configuration</a></td>
<td>Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar. Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt. Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt. Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert. Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335380(v=exchg.10).md">Enableadvanced</a></td>
<td>Dieser Parameter wird verwendet, um zu steuern, wann die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt. Dieser Parameter wird zusammen mit der <a href="dn335289(v=exchg.10).md">Konfiguration</a> verwendet, um zu verhindern, dass einige Systemparameter aus den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335291(v=exchg.10).md">Enablefilecache</a></td>
<td>Aktivieren Sie die Verwendung des Betriebssystem-Datei Caches für alle verwalteten Dateien.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335381(v=exchg.10).md">Enableviewcache</a></td>
<td>Aktivieren Sie die Verwendung von Datei-e/a mit Speicher Abbild für Datenbankdateien.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335292(v=exchg.10).md">Keymost</a></td>
<td>Dieser schreibgeschützte Parameter gibt die maximal zulässige Länge des Index Schlüssels an, die für die aktuelle Datenbankseiten Größe (wie von <a href="hh596135(v=exchg.10).md">databasepagesize</a>konfiguriert) ausgewählt werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335384(v=exchg.10).md">Legacyfile-Namen</a></td>
<td>Dieser Parameter stellt Abwärtskompatibilität mit den Datei Benennungs Konventionen früherer Versionen der Datenbank-Engine bereit.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335294(v=exchg.10).md">TableClass10Name</a></td>
<td>Legen Sie den mit TABLE class 10 verknüpften Namen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335385(v=exchg.10).md">TableClass11Name</a></td>
<td>Legen Sie den Namen der Tabellen Klasse 11 fest.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335387(v=exchg.10).md">TableClass12Name</a></td>
<td>Legen Sie den der Table-Klasse 12 zugeordneten Namen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335388(v=exchg.10).md">TableClass13Name</a></td>
<td>Legen Sie den der Table-Klasse 13 zugeordneten Namen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335295(v=exchg.10).md">TableClass14Name</a></td>
<td>Legen Sie den der Table-Klasse 14 zugeordneten Namen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335390(v=exchg.10).md">TableClass15Name</a></td>
<td>Legen Sie den der Tabellen Klasse 15 zugeordneten Namen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335297(v=exchg.10).md">TableClass1Name</a></td>
<td>Legen Sie den mit Table Class 1 verknüpften Namen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335389(v=exchg.10).md">TableClass2Name</a></td>
<td>Legen Sie den der Table-Klasse 2 zugeordneten Namen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335296(v=exchg.10).md">TableClass3Name</a></td>
<td>Legen Sie den Namen der Tabelle Class 3 fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335395(v=exchg.10).md">TableClass4Name</a></td>
<td>Legen Sie den der Table-Klasse 4 zugeordneten Namen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335401(v=exchg.10).md">TableClass5Name</a></td>
<td>Legen Sie den der Table-Klasse 5 zugeordneten Namen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335298(v=exchg.10).md">TableClass6Name</a></td>
<td>Legen Sie den der Tabellen Klasse 6 zugeordneten Namen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335402(v=exchg.10).md">TableClass7Name</a></td>
<td>Legen Sie den der Tabelle Class 7 zugeordneten Namen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335299(v=exchg.10).md">TableClass8Name</a></td>
<td>Legen Sie den der Tabellen Klasse 8 zugeordneten Namen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335404(v=exchg.10).md">TableClass9Name</a></td>
<td>Legen Sie den mit TABLE class 9 verknüpften Namen fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistaparam-Klasse](./vistaparam-class.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
