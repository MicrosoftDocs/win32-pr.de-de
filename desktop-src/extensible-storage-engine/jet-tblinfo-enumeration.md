---
description: 'Weitere Informationen finden Sie hier: JET_TblInfo-Enumeration'
title: JET_TblInfo-Enumeration
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
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349455"
---
# <a name="jet_tblinfo-enumeration"></a>JET_TblInfo-Enumeration

Informationsebenen zum Abrufen von Tabellen Informationen mit jetgettableinfo.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Standardoption Ruft ein <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> ab, das Informationen zur Tabelle enthält. Verwenden Sie diese Option mit <a href="dn292198(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Name</td>
<td>Ruft den Namen der Tabelle ab. Verwenden Sie diese Option mit <a href="dn292204(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>Dbid</td>
<td>Ruft den <a href="hh596176(v=exchg.10).md">JET_DBID</a> der Datenbank ab, die die Tabelle enthält. Verwenden Sie diese Option mit <a href="dn292197(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Spaceusage</td>
<td>Das Verhalten der-Methode hängt von der Größe des Arrays ab, das an die-Methode weitergegeben wird. Das Array muss mindestens zwei Einträge enthalten. Der erste Eintrag enthält die Anzahl der im Besitz befindlichen Blöcke in der Tabelle. Der zweite Eintrag enthält die Anzahl der verfügbaren Blöcke in der Tabelle. Wenn das Array mehr als zwei Einträge enthält, bestehen die verbleibenden Bytes des Puffers aus einem Array von-Strukturen, die eine Liste von Blöcken darstellen. Diese Struktur enthält zwei Member: die letzte Seitenzahl im Block und die Anzahl der Seiten im Wertebereich. Verwenden Sie diese Option mit <a href="dn292202(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>Spacezuweisung</td>
<td>Das an jetgettableinfo über gegebene Array muss über zwei Einträge verfügen. Der erste Eintrag wird auf die Anzahl der Seiten in der Tabelle festgelegt. Der zweite Eintrag wird auf die zieldichte von Seiten für die Tabelle festgelegt. Verwenden Sie diese Option mit <a href="dn292202(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Leerraum</td>
<td>Ruft die Anzahl der eigenen Seiten in der Tabelle ab. Verwenden Sie diese Option mit <a href="dn292201(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>Leerraum verfügbar</td>
<td>Ruft die Anzahl der verfügbaren Seiten in der Tabelle ab. Verwenden Sie diese Option mit <a href="dn292201(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Templatetablename</td>
<td>Wenn die Tabelle eine abgeleitete Tabelle ist, wird das Ergebnis mit dem Namen der Tabelle ausgefüllt, von der die abgeleitete Tabelle Ihre DDL geerbt hat. Wenn die Tabelle keine abgeleitete Tabelle ist, wird für den Puffer eine leere Zeichenfolge verwendet. Verwenden Sie diese Option mit <a href="dn292204(v=exchg.10).md">jetgettableinfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
