---
description: Weitere Informationen zu JET_TABLECREATE Eigenschaften
title: JET_TABLECREATE-Eigenschaften
TOCTitle: JET_TABLECREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_TABLECREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103995
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6f5802c42bbf32548e1d42e507013fc0235eafdd1bd989b75f628b43a1b327eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252154"
---
# <a name="jet_tablecreate-properties"></a>JET_TABLECREATE-Eigenschaften

Einschließen geschützter Member  
Einschließen geerbter Member  

Der [JET_TABLECREATE-Typ](./jet-tablecreate-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn351077(v=exchg.10).md">cbSeparateLV</a></td>
<td>Ruft die heuristische Größe ab, um eine systeminterne LV vom primären Datensatz zu trennen, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351078(v=exchg.10).md">cbtyp</a></td>
<td>Ruft einen Typ der Rückruffunktion ab oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351080(v=exchg.10).md">cColumns</a></td>
<td>Ruft die Anzahl der zu erstellende Spalten ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351079(v=exchg.10).md">cCreated</a></td>
<td>Ruft die Anzahl der erstellten Objekte (columns+table+indexes+callbacks) ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351081(v=exchg.10).md">cIndexes</a></td>
<td>Ruft die Anzahl der zu erstellende Indizes ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351082(v=exchg.10).md">grbit</a></td>
<td>Ruft die Tabellenoptionen ab oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351087(v=exchg.10).md">pLVSpacehints</a></td>
<td>Ruft Platzzuweisungs-, Wartungs- und Nutzungshinweise für separate LV-Struktur vom Typ <a href="dn351095(v=exchg.10).md">JET_SPACEHINTS ab</a>oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351083(v=exchg.10).md">pSeqSpacehints</a></td>
<td>Ruft Hinweise zur Speicherplatzbelegung, Wartung und Nutzung für den sequenziellen Standardindex ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351086(v=exchg.10).md">rgcolumncreate</a></td>
<td>Ruft ein Array von Spaltenerstellungsinformationen vom Typ JET_COLUMNCREATE ab oder legt dieses <a href="dn335028(v=exchg.10).md">fest.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351089(v=exchg.10).md">rgindexcreate</a></td>
<td>Ruft ein Zu erstellendes Indexarray vom Typ JET_INDEXCREATE ab oder legt dieses <a href="dn335112(v=exchg.10).md">fest.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351090(v=exchg.10).md">szCallback</a></td>
<td>Ruft eine Rückruffunktion ab, die für die Tabelle verwendet werden soll, oder legt diese fest. Dies weist das Format &quot; module!functionName auf &quot; und geht von nicht verwaltetem Code aus. Eine Alternative finden Sie unter <strong>JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE).</strong></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351092(v=exchg.10).md">szTableName</a></td>
<td>Ruft den Namen der zu erstellende Tabelle ab oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351093(v=exchg.10).md">szTemplateTableName</a></td>
<td>Ruft den Namen der Tabelle ab, von der basis-DDL geerbt werden soll, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351099(v=exchg.10).md">tableid</a></td>
<td>Ruft die zurückgegebene "tabledid" ab oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351101(v=exchg.10).md">ulDensity</a></td>
<td>Ruft die Tabellendichte ab oder legt sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351102(v=exchg.10).md">ulPages</a></td>
<td>Ruft die anfänglichen Seiten ab, die der Tabelle zugeordnet werden sollen, oder legt sie fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_TABLECREATE-Klasse](./jet-tablecreate-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
