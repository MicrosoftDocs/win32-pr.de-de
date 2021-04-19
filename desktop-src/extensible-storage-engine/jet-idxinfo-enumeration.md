---
description: 'Weitere Informationen finden Sie hier: JET_IdxInfo-Enumeration'
title: JET_IdxInfo-Enumeration
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352723"
---
# <a name="jet_idxinfo-enumeration"></a>JET_IdxInfo-Enumeration

Info Ebenen für das Abrufen von Indexinformationen mit jetgetindexinfo. und jetgettableindexinfo.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
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
<td>Gibt eine <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> -Struktur mit Informationen über den Index zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>List</td>
<td>Gibt eine <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> -Struktur mit Informationen über den Index zurück.</td>
</tr>
<tr class="odd">
<td></td>
<td>Systabcursor</td>
<td><strong>Veraltet.</strong> Systabcursor ist veraltet.</td>
</tr>
<tr class="even">
<td></td>
<td>OLC</td>
<td><strong>Veraltet.</strong> OLC ist veraltet.</td>
</tr>
<tr class="odd">
<td></td>
<td>Reabtolc</td>
<td><strong>Veraltet.</strong> Zurücksetzen von OLC ist veraltet.</td>
</tr>
<tr class="even">
<td></td>
<td>Spacezuweisung</td>
<td>Gibt eine ganze Zahl mit der Speicherplatz Verwendung des Indexes zurück.</td>
</tr>
<tr class="odd">
<td></td>
<td>LCID</td>
<td>Gibt eine ganze Zahl mit der LCID des Indexes zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>Langid</td>
<td><strong>Veraltet.</strong> Die langid ist veraltet. Verwenden Sie stattdessen LCID.</td>
</tr>
<tr class="odd">
<td></td>
<td>Anzahl</td>
<td>Gibt eine ganze Zahl mit der Anzahl der Indizes in der Tabelle zurück.</td>
</tr>
<tr class="even">
<td></td>
<td>Varsegmac</td>
<td>Gibt einen Ushort-Wert mit dem Wert cbvarsegmac zurück, mit dem der Index erstellt wurde.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexId</td>
<td>Gibt einen <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> zurück, der den Index identifiziert.</td>
</tr>
<tr class="even">
<td></td>
<td>Keymost</td>
<td>Eingeführt in Windows Vista. Gibt einen ushort mit dem Wert cbkeymost zurück, mit dem der Index erstellt wurde.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
