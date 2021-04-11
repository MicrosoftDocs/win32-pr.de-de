---
description: 'Weitere Informationen finden Sie hier: JET_INDEXCREATE Member'
title: Mitglieder JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217861"
---
# <a name="jet_indexcreate-members"></a>Mitglieder JET_INDEXCREATE

Geschützte Member einschließen  
Geerbte Member einschließen  

Enthält die Informationen, die erforderlich sind, um einen Index über Daten in einer ESE-Datenbank zu erstellen. Enthält die Informationen, die erforderlich sind, um einen Index über Daten in einer ESE-Datenbank zu erstellen.

Der [JET_INDEXCREATE](./jet-indexcreate-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="constructors"></a>Konstruktoren

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></td>
<td></td>
</tr>
</tbody>
</table>


Oben

## <a name="properties"></a>Eigenschaften

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Ruft die Länge von szkey (in Zeichen) ab, einschließlich der beiden abschließenden Nullen, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbkeymost</a></td>
<td>Ruft die maximal zulässige Größe (in Bytes) für Schlüssel im Index ab oder legt diese fest. Die unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255). Dies ist die maximale maximale Schlüsselgröße. Die maximale Schlüsselgröße hängt von der Datenbankseiten Größe <a href="hh596135(v=exchg.10).md">databasepagesize</a>ab. Die maximale Schlüsselgröße kann mit <a href="dn351156(v=exchg.10).md">keymost</a>abgerufen werden. Dieser Parameter wird unter Windows XP und Windows Server 2003 ignoriert. Anders als bei der nicht verwalteten API ist <strong>indexkeymost ()</strong> (JET_bitIndexKeyMost) nicht erforderlich, sondern wird automatisch hinzugefügt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbvarsegmac</a></td>
<td>Ruft die maximale Länge (in Byte) der einzelnen Spalten ab, die im Index gespeichert werden sollen, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cconditionalcolumn</a></td>
<td>Ruft die Anzahl der bedingten Spalten ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">irre</a></td>
<td>Ruft den Fehlercode ab, der den Index erstellt, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Ruft Index Erstellungs Optionen ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxunicode</a></td>
<td>Ruft die optionalen Unicode-Vergleichs Optionen ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pspacehints</a></td>
<td>Ruft Speicherplatz Zuordnung, Wartung und Verwendungs Hinweise ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>Ruft die optionalen bedingten Spalten ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szindexname</a></td>
<td>Ruft den Namen des zu erstellenden Indexes ab oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szkey</a></td>
<td>Ruft die Beschreibung des Index Schlüssels ab oder legt Sie fest. Dies ist eine Double-NULL-terminierte Zeichenfolge mit durch Null getrennten Token. Jedes Token hat das Format [Direction-specifier] [Spaltenname], wobei Direction-Specification entweder &quot; + &quot; oder ist &quot; - &quot; . Beispielsweise wird ein szkey von &quot; + abc\0-def\0 + ghi\0 &quot; über die drei Spalten &quot; ABC &quot; (in aufsteigender Reihenfolge), &quot; DEF &quot; (in absteigender Reihenfolge) und &quot; ghi &quot; (in aufsteigender Reihenfolge) indiziert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">uldensity</a></td>
<td>Ruft die Dichte des Indexes ab oder legt Sie fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="methods"></a>Methoden

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335116(v=exchg.10).md">Contentequals</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335153(v=exchg.10).md">Deepclone</a></td>
<td>Gibt eine tiefe Kopie des-Objekts zurück.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335154(v=exchg.10).md">ToString</a></td>
<td>Generiert eine Zeichen folgen Darstellung der-Instanz. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXCREATE-Klasse](./jet-indexcreate-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
