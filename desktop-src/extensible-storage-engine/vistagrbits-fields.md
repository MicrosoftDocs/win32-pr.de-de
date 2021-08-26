---
description: Weitere Informationen finden Sie unter VistaGrbits-Felder.
title: VistaGrbits-Felder (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaGrbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104318
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d81a176d04911f2c76767838a62e5202f9e80c059112c703a3673644fddb76f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967570"
---
# <a name="vistagrbits-fields"></a>VistaGrbits-Felder

Geschützte Member enthalten  
Geerbte Member enthalten  

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
<td>Wenn Sie dieses Flag für einen Index angeben, der über mehrere Schlüsselspalten verfügt, bei denen es sich um eine mehrwertige Spalte handelt, wird für jedes Ergebnis eines Kreuzprodukts aller Werte in diesen Schlüsselspalten ein Indexeintrag erstellt. Andernfalls würde der Index nur einen Eintrag für jeden Mehrwert in der wichtigsten Schlüsselspalte enthalten, bei der es sich um eine mehrwertige Spalte handelt, und jeder dieser Indexeinträge würde den ersten Mehrwert aus allen anderen Schlüsselspalten verwenden, bei denen es sich um mehrwertige Spalten handelt. Wenn Sie beispielsweise dieses Flag für einen Index über Spalte A mit den Werten rot und blau und über Spalte B mit den Werten 1 und 2 angegeben haben, werden die folgenden Indexeinträge &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; erstellt: &quot; &quot; rot, &quot; 1 &quot; ; &quot; red, &quot; &quot; 2 &quot; ; &quot; blue, &quot; &quot; 1 &quot; ; &quot; blue, &quot; &quot; 2 &quot; . Andernfalls werden die folgenden Indexeinträge erstellt: &quot; &quot; rot, &quot; 1 &quot; ; &quot; blue, &quot; &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>Die Angabe dieses Flags führt dazu, dass alle Aktualisierungen des Indexes, die zu einem abgeschnittenen Schlüssel führen würden, mit <a href="hh564840(v=exchg.10).md">KeyTruncated fehlschlagen.</a> Andernfalls werden Schlüssel automatisch abgeschnitten.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>Index über mehrere mehrwertige Spalten, aber nur mit Werten der gleichen itagSequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>Transaktionsprotokolle müssen im Protokolldateiverzeichnis vorhanden sein (d. h., ein neuer Stream kann nicht automatisch gestartet werden).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>Führen Sie die Wiederherstellung aus, halten Sie jedoch in der Phase Rückgängig an. Ermöglicht die Wiedergabe von Protokollen. Später können zusätzliche Protokolle kopiert und wiedergegeben werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>Fehlender Datenbankzuordnungseintrag wird standardmäßig auf denselben Speicherort festgelegt.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>Die Engine kann die Datenbankheader entsprechend markieren (z. B. eine vollständige Sicherung wurde abgeschlossen), obwohl der Aufruf zum Abschneiden nicht abgeschlossen wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>Bei erfolgreicher soft recovery können Sie Protokolldateien abschneiden.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[VistaGrbits-Klasse](./vistagrbits-class.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
