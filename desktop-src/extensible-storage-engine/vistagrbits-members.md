---
description: Weitere Informationen zu VistaGrbits-Membern
title: VistaGrbits-Member (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: be9908627d4351ec710fa6b1791d24779ab501b8e61bb342d96a3a0ec4afa87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978160"
---
# <a name="vistagrbits-members"></a>VistaGrbits-Member

Einschließen geschützter Member  
Einschließen geerbter Member  

Grbits, die der Vista-Version von ESENT hinzugefügt wurden.

Der [VistaGrbits-Typ](./vistagrbits-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></td>
<td>Die Momentaufnahmesitzung wird nach JetOSSnapshotThaw fortgesetzt und erfordert einen JetOSSnapshotEnd-Funktionsaufruf.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></td>
<td>Wenn Sie dieses Flag für einen Index angeben, der mehr als eine Schlüsselspalte enthält, bei der es sich um eine mehrwertige Spalte handelt, wird für jedes Ergebnis eines Kreuzprodukts aller Werte in diesen Schlüsselspalten ein Indexeintrag erstellt. Andernfalls hätte der Index nur einen Eintrag für jeden Mehrwert in der wichtigsten Schlüsselspalte, bei der es sich um eine mehrwertige Spalte handelt, und jeder dieser Indexeinträge würde den ersten Mehrwert aus allen anderen Schlüsselspalten verwenden, bei denen es sich um mehrwertige Spalten handelt. Wenn Sie z. B. dieses Flag für einen Index über Spalte A mit den Werten rot und blau und für Spalte B mit &quot; &quot; den Werten &quot; &quot; 1 und 2 angegeben &quot; &quot; &quot; &quot; haben, werden die folgenden Indexeinträge erstellt: &quot; rot , &quot; &quot; 1 &quot; ; &quot; rot &quot; , &quot; 2 &quot; ; &quot; blue &quot; , &quot; 1 &quot; ; &quot; blau, &quot; &quot; 2 &quot; . Andernfalls werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; blau, &quot; &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>Wenn Sie dieses Flag angeben, tritt bei jeder Aktualisierung des Indexes ein Fehler auf, der dazu führen würde, dass ein abgeschnittener Schlüssel mit <a href="hh564840(v=exchg.10).md">KeyTruncated fehlschlägt.</a> Andernfalls werden Schlüssel automatisch abgeschnitten.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>Index über mehrere mehrwertige Spalten, aber nur mit Werten desselben ItagSequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>Transaktionsprotokolle müssen im Protokolldateiverzeichnis vorhanden sein (d. h. ein neuer Stream kann nicht automatisch gestartet werden).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>Führen Sie die Wiederherstellung durch, aber halten Sie in der Rückgängig-Phase an. Ermöglicht die Wiedergabe aller vorhandenen Protokolle. Später können zusätzliche Protokolle kopiert und wiedergegeben werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>Fehlender Datenbankzuordnungseintrag wird standardmäßig an demselben Speicherort verwendet.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>Die Engine kann die Datenbankheader nach Bedarf markieren (z. B. eine vollständige Sicherung abgeschlossen), auch wenn der Aufruf zum Abschneiden nicht abgeschlossen wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>Kürzen Sie protokolldateien bei erfolgreicher soft recovery ab.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[VistaGrbits-Klasse](./vistagrbits-class.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
