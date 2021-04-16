---
description: 'Weitere Informationen finden Sie hier: vistagrbits-Member'
title: Vistagrbits-Member (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551812"
---
# <a name="vistagrbits-members"></a>Vistagrbits-Member

Geschützte Member einschließen  
Geerbte Member einschließen  

Grbits, die der Vista-Version von ESENT hinzugefügt wurden.

Der [vistagrbits](./vistagrbits-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn351283(v=exchg.10).md">Continueafterthaw</a></td>
<td>Die Momentaufnahme Sitzung wird nach jedessnapshotthaw fortgesetzt, und es wird ein jedessnapshotend-Funktions aufrufbedarf benötigt.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">Indexcrossproduct</a></td>
<td>Wenn dieses Flag für einen Index angegeben wird, der mehr als eine Schlüssel Spalte aufweist, die eine mehrwertige Spalte ist, führt dies dazu, dass für jedes Ergebnis eines Kreuz Produkts aller Werte in diesen Schlüssel Spalten ein Index Eintrag erstellt wird. Andernfalls würde der Index nur einen Eintrag für jeden multiwert in der signifikantesten Schlüssel Spalte enthalten, bei der es sich um eine mehrwertige Spalte handelt, und jede dieser Indexeinträge würde den ersten mehrwertigen Wert aus anderen Schlüssel Spalten verwenden, die mehrwertige Spalten sind. Wenn Sie z. B. dieses Flag für einen Index über Spalte a mit den Werten &quot; rot &quot; und &quot; blau &quot; und over column B mit den Werten 1 und 2 angegeben haben, &quot; &quot; &quot; &quot; werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; rot &quot; , &quot; 2 &quot; ; &quot; blau &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 2 &quot; . Andernfalls werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">Indexdisallowtrunation</a></td>
<td>Die Angabe dieses Flags führt dazu, dass ein Update des Indexes, das zu einem abgeschnittene Schlüssel führt, mit <a href="hh564840(v=exchg.10).md">keytruncated</a>fehlschlägt. Andernfalls werden Schlüssel automatisch abgeschnitten.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">Indexnetstedtable</a></td>
<td>Indizieren Sie mehr als mehrere mehrwertige Spalten, aber nur mit Werten derselben itagsequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">Logstreammustexist</a></td>
<td>Transaktionsprotokolle müssen im Protokoll Dateiverzeichnis vorhanden sein (d. h., ein neuer Stream kann nicht automatisch gestartet werden).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">Wiederherstellenrückgängigmachen</a></td>
<td>Führen Sie die Wiederherstellung aus, aber stoppen Sie die Roll Back Phase. Ermöglicht, dass die Protokolle wiedergegeben werden können. später können zusätzliche Protokolle kopiert und wiedergegeben werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">Replaymissingmapentrydb</a></td>
<td>Fehlender Daten Bank Zuordnungs Eintrag ist standardmäßig derselbe Speicherort.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">Trunalisiedone</a></td>
<td>Die Engine kann die Daten Bank Header nach Bedarf markieren (z. b. eine vollständige Sicherung abgeschlossen), obwohl der Abschneidevorgang nicht abgeschlossen wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">Trungatelogsafterrecovery</a></td>
<td>Bei erfolgreicher Soft-Wiederherstellung kürzen Sie die Protokolldateien.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistagrbits-Klasse](./vistagrbits-class.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
