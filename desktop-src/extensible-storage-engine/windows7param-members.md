---
description: 'Weitere Informationen finden Sie hier: Windows7Param Members'
title: Windows7Param-Member (Microsoft. ISAM. ESENT. Interop. Windows7)
TOCTitle: Windows7Param members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Windows7.Windows7Param
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7param_members(v=EXCHG.10)
ms:contentKeyID: 55104286
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a0af5c50dd702bc97a6e228cf12429cae471fab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556224"
---
# <a name="windows7param-members"></a>Windows7Param-Member

Geschützte Member einschließen  
Geerbte Member einschließen  

System Parameter, die der Windows 7-Version von ESENT hinzugefügt wurden.

Der [Windows7Param](./windows7param-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335314(v=exchg.10).md">Dbscanintervalmaxsec</a></td>
<td>Maximales Intervall zum Abschließen der Daten Bank Überprüfung (in Sekunden).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335431(v=exchg.10).md">Dbscanintervalminsec</a></td>
<td>Mindestintervall zum Wiederholen des Daten Bank Scans (in Sekunden).</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335316(v=exchg.10).md">Dbscanthrottle</a></td>
<td>Drosselung des Daten Bank Scans in Millisekunden.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335434(v=exchg.10).md">Enabledbscaninrecovery</a></td>
<td>Aktivieren der Datenbankwartung während der Wiederherstellung.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335318(v=exchg.10).md">Lvchunksizemost</a></td>
<td>Dieser Parameter wird verwendet, um die Segmentgröße von BLOB-Daten (Long-Value) abzurufen. Das Festlegen und Abrufen von Daten in Vielfachen dieser Größe erhöht die Effizienz.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335433(v=exchg.10).md">Maxcoalescereadgapsize</a></td>
<td>Maximale Anzahl von Bytes, die für einen zusammengefügten Lese-e/a-Vorgang ggetauscht werden können.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335435(v=exchg.10).md">Maxcoalescereadsize</a></td>
<td>Maximale Anzahl von Bytes, die nach einem zusammengefügten Lesevorgang gruppiert werden können.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335322(v=exchg.10).md">Maxcoalesceschreitegapsize</a></td>
<td>Maximale Anzahl von Bytes, die für einen zusammengefügten Schreib-e/a-Vorgang ggetauscht werden können.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335437(v=exchg.10).md">Maxcoalesceschreitesize</a></td>
<td>Maximale Anzahl von Bytes, die für einen zusammengefügten Schreibvorgang gruppiert werden können.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335438(v=exchg.10).md">Waypointlatency</a></td>
<td>Mit diesem Parameter wird die Anzahl der Protokolle festgelegt, für die ESENT Daten Bank Leerungen verzögert. Dies kann verwendet werden, um die Wiederherstellbarkeit der Datenbank zu erhöhen, wenn Fehler beim Verlust von Protokolldateien auftreten.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Windows7Param-Klasse](./windows7param-class.md)

[Microsoft. ISAM. ESENT. Interop. Windows7-Namespace](./microsoft.isam.esent.interop.windows7-namespace.md)
