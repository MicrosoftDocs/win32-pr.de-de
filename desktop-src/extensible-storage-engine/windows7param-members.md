---
description: 'Weitere Informationen zu: Windows7Param-Member'
title: Windows7Param-Member (Microsoft.Isam.Esent.Interop.Windows7)
TOCTitle: Windows7Param members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Windows7.Windows7Param
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7param_members(v=EXCHG.10)
ms:contentKeyID: 55104286
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0d94a394eb5befffe46199dcc04a24b83c3a484fa8552a4ac5db40d1ba0d1d13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667430"
---
# <a name="windows7param-members"></a>Windows7Param-Member

Geschützte Member enthalten  
Geerbte Member enthalten  

Systemparameter, die der Version Windows 7 von ESENT hinzugefügt wurden.

Der [Windows7Param-Typ](./windows7param-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn335314(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>Maximales Intervall, damit der Datenbankscan abgeschlossen werden kann (in Sekunden).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335431(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>Minimales Intervall zum Wiederholen des Datenbankscans in Sekunden.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335316(v=exchg.10).md">DbScanThrottle</a></td>
<td>Drosselung des Datenbankscans in Millisekunden.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335434(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>Aktivieren Sie die Datenbankwartung während der Wiederherstellung.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335318(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>Dieser Parameter wird verwendet, um die Blockgröße von Long-Value-Daten (Blobdaten) abzurufen. Das Festlegen und Abrufen von Daten in Vielfachen dieser Größe erhöht die Effizienz.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335433(v=exchg.10).md">MaxCoalesceReadGapSize</a></td>
<td>Maximale Anzahl von Bytes, die für einen zusammenfingierten Lese-E/A-Vorgang gelücket werden können.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335435(v=exchg.10).md">MaxCoalesceReadSize</a></td>
<td>Maximale Anzahl von Bytes, die für einen zusammenfingierten Lesevorgang gruppiert werden können.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335322(v=exchg.10).md">MaxCoalesceWriteGapSize</a></td>
<td>Maximale Anzahl von Bytes, die für einen zusammenfingierten Schreib-E/A-Vorgang gelücket werden können.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335437(v=exchg.10).md">MaxCoalesceWriteSize</a></td>
<td>Maximale Anzahl von Bytes, die für einen zusammenfingierten Schreibvorgang gruppiert werden können.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335438(v=exchg.10).md">WaypointLatency</a></td>
<td>Dieser Parameter legt die Anzahl der Protokolle fest, für die Datenbank geleert wird. Dies kann verwendet werden, um die Wiederherstellbarkeit der Datenbank zu erhöhen, wenn Fehler dazu führen, dass Protokolldateien verloren gehen.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Windows7Param-Klasse](./windows7param-class.md)

[Microsoft.Isam.Esent.Interop.Windows7-Namespace](./microsoft.isam.esent.interop.windows7-namespace.md)
