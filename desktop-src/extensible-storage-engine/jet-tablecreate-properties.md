---
description: 'Weitere Informationen finden Sie hier: JET_TABLECREATE-Eigenschaften'
title: Eigenschaften von JET_TABLECREATE
TOCTitle: JET_TABLECREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_TABLECREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103995
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2c79440fa5e04acefe54ed271460d6bd11bc57fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050587"
---
# <a name="jet_tablecreate-properties"></a>Eigenschaften von JET_TABLECREATE

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [JET_TABLECREATE](./jet-tablecreate-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn351077(v=exchg.10).md">cbseparatelv</a></td>
<td>Ruft die heuristische Größe ab, um ein System internes LV vom primären Datensatz zu trennen, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351078(v=exchg.10).md">cbyp</a></td>
<td>Ruft einen Typ der Rückruffunktion ab oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351080(v=exchg.10).md">cColumns</a></td>
<td>Ruft die Anzahl der zu erstellenden Spalten ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351079(v=exchg.10).md">erstellt</a></td>
<td>Ruft die Anzahl der erstellten Objekte (Spalten + Tabelle + Indizes + Rückrufe) ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351081(v=exchg.10).md">cindexes</a></td>
<td>Ruft die Anzahl der zu erstellenden Indizes ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351082(v=exchg.10).md">grbit</a></td>
<td>Ruft die Tabellen Optionen ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351087(v=exchg.10).md">plvspacehints</a></td>
<td>Ruft Speicherplatz Zuordnung, Wartung und Verwendungs Hinweise für die getrennte LV-Struktur vom Typ " <a href="dn351095(v=exchg.10).md">JET_SPACEHINTS</a>" ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351083(v=exchg.10).md">pssqspacehints</a></td>
<td>Ruft Speicherplatz Zuordnung, Wartung und Verwendungs Hinweise für den sequenziellen Standard Index ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351086(v=exchg.10).md">rgcolumncreate</a></td>
<td>Ruft ein Array von Spalten Erstellungs Informationen vom Typ " <a href="dn335028(v=exchg.10).md">JET_COLUMNCREATE</a>" ab oder legt es fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351089(v=exchg.10).md">rgindexcreate</a></td>
<td>Ruft ein Array von zu erstellenden Indizes vom Typ <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a>ab oder legt es fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351090(v=exchg.10).md">szcallback</a></td>
<td>Ruft eine Rückruffunktion ab, die für die Tabelle verwendet wird, oder legt Sie fest. Dies liegt im Format &quot; module! functionname vor &quot; und geht von nicht verwaltetem Code aus. Eine Alternative finden Sie <strong>unter jetregistercallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</strong> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351092(v=exchg.10).md">sztablename</a></td>
<td>Ruft den Namen der zu erstellenden Tabelle ab oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351093(v=exchg.10).md">sztemplatetablename</a></td>
<td>Ruft den Namen der Tabelle ab, von der die Basis-DDL geerbt werden soll, oder legt ihn fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351099(v=exchg.10).md">TableID</a></td>
<td>Ruft die zurückgegebene tabledid ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351101(v=exchg.10).md">uldensity</a></td>
<td>Ruft die Tabellen Dichte ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351102(v=exchg.10).md">ulpages</a></td>
<td>Ruft die für die Tabelle zuzuordnenden anfangs Seiten ab oder legt diese fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_TABLECREATE-Klasse](./jet-tablecreate-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
