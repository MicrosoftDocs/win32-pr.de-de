---
description: 'Weitere Informationen finden Sie unter: JET_TblInfo Enumeration'
title: JET_TblInfo Enumeration
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b2af9bfd69f81b518eba42f435a457c9baaa0d0ce8ddbac1424b997329a3ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832680"
---
# <a name="jet_tblinfo-enumeration"></a>JET_TblInfo Enumeration

Infoebenen zum Abrufen von Tabelleninformationen mit JetGetTableInfo.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a>Member

<table>
<thead>
<tr class="header">
<th></th>
<th>Membername</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Standard</td>
<td>Standardoption Ruft einen <a href="dn335219(v=exchg.10).md">-JET_OBJECTINFO,</a> der Informationen über die Tabelle enthält. Verwenden Sie diese Option <a href="dn292198(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>Name</td>
<td>Ruft den Namen der Tabelle ab. Verwenden Sie diese Option <a href="dn292204(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo).</a></td>
</tr>
<tr class="odd">
<td></td>
<td>Dbid</td>
<td>Ruft die <a href="hh596176(v=exchg.10).md">JET_DBID</a> der Datenbank ab, die die Tabelle enthält. Verwenden Sie diese Option <a href="dn292197(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>SpaceUsage</td>
<td>Das Verhalten der -Methode hängt davon ab, wie groß das Array ist, das an die -Methode übergeben wird. Das Array muss mindestens zwei Einträge enthalten. Der erste Eintrag enthält die Anzahl der eigenen Extents in der Tabelle. Der zweite Eintrag enthält die Anzahl der verfügbaren Extents in der Tabelle. Wenn das Array mehr als zwei Einträge enthält, bestehen die verbleibenden Bytes des Puffers aus einem Array von -Strukturen, die eine Liste von Extents darstellen. Diese Struktur enthält zwei Elemente: die letzte Seitenzahl im -Bereich und die Anzahl der Seiten im -Bereich. Verwenden Sie diese Option <a href="dn292202(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo).</a></td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAlloc</td>
<td>Das an JetGetTableInfo übergebene Array muss zwei Einträge enthalten. Der erste Eintrag wird auf die Anzahl der Seiten in der Tabelle festgelegt. Der zweite Eintrag wird auf die Zieldichte der Seiten für die Tabelle festgelegt. Verwenden Sie diese Option <a href="dn292202(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>SpaceOwned</td>
<td>Ruft die Anzahl der eigenen Seiten in der Tabelle ab. Verwenden Sie diese Option <a href="dn292201(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo).</a></td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAvailable</td>
<td>Ruft die Anzahl der verfügbaren Seiten in der Tabelle ab. Verwenden Sie diese Option <a href="dn292201(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo).</a></td>
</tr>
<tr class="even">
<td></td>
<td>TemplateTableName</td>
<td>Wenn die Tabelle eine abgeleitete Tabelle ist, wird das Ergebnis mit dem Namen der Tabelle gefüllt, von der die abgeleitete Tabelle ihre DDL geerbt hat. Wenn die Tabelle keine abgeleitete Tabelle ist, ist der Puffer eine leere Zeichenfolge. Verwenden Sie diese Option <a href="dn292204(v=exchg.10).md">mit JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo).</a></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
