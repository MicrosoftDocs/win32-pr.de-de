---
description: 'Weitere Informationen finden Sie unter: JET_DbInfo Enumeration'
title: JET_DbInfo Enumeration
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c364b89ccb50542130c988a643fed594a34e370e5adb5e9d0a13f77eab5b04d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112229"
---
# <a name="jet_dbinfo-enumeration"></a>JET_DbInfo Enumeration

Infoebenen zum Abrufen von Datenbankinformationen.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
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
<td>Dateiname</td>
<td>Gibt den Pfad zur Datenbankdatei (Zeichenfolge) zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>Gibt den Dieser Datenbank zugeordneten Locale Identifier (LCID) zurück (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Optionen</td>
<td>Gibt <a href="hh579532(v=exchg.10).md">openDatabaseGrbit zurück.</a> Dies gibt an, ob die Datenbank im exklusiven Modus geöffnet wird. Wenn sich die Datenbank im exklusiven Modus befindet, wird <a href="hh579532(v=exchg.10).md">Exclusive</a> zurückgegeben, andernfalls wird 0 zurückgegeben. Andere Datenbank-Grbit-Optionen für JetAttachDatabase und JetOpenDatabase werden nicht zurückgegeben.</td>
</tr>
<tr class="even">
<td></td>
<td>Transaktionen</td>
<td>Gibt eine Zahl zurück, die größer als die maximale Ebene ist, auf der Transaktionen geschachtelt werden können. Wenn <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> so oft wie dieser Wert aufgerufen wird (in einer Schachtelung, d. h. in derselben Sitzung, ohne Commit oder Rollback), wird beim letzten Aufruf <a href="hh564840(v=exchg.10).md">TransTooDeep</a> zurückgegeben (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Version</td>
<td>Gibt die Hauptversion der Datenbank-Engine (Int32) zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>Dateigröße</td>
<td>Gibt die Dateigröße der Datenbank in Seiten (Int32) zurück.</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceOwned</td>
<td>Gibt den eigenen Speicherplatz der Datenbank in Seiten (Int32) zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAvailable</td>
<td>Gibt den verfügbaren Speicherplatz in der Datenbank in Seiten (Int32) zurück.</td>
</tr>
<tr class="odd">
<td></td>
<td>Sonstiges</td>
<td>Gibt <a href="hh538867(v=exchg.10).md">ein</a> JET_DBINFOMISC zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>Gibt einen booleschen Wert zurück, der angibt, ob die Datenbank angefügt ist (boolescher Wert).</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>Gibt die Seitengröße der Datenbank zurück (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>Gibt den Typ der Datenbank zurück (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
