---
description: 'Weitere Informationen zu: jetrelop Enumeration'
title: Jetrelop-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350418"
---
# <a name="jetrelop-enumeration"></a>Jetrelop-Enumeration

Vergleichs Vorgang für Filter, der als [JET_INDEX_COLUMN](./jet-index-column-class.md)definiert ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
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
<td>Equals</td>
<td>Akzeptieren Sie nur Zeilen, deren Spaltenwert gleich dem angegebenen Wert ist.</td>
</tr>
<tr class="even">
<td></td>
<td>Prefixist</td>
<td>Akzeptieren Sie nur Zeilen, die Spalten aufweisen, deren Präfix mit dem angegebenen Wert übereinstimmt.</td>
</tr>
<tr class="odd">
<td></td>
<td>NotEquals</td>
<td>Akzeptieren Sie nur Zeilen, deren Spaltenwert nicht gleich dem angegebenen Wert ist.</td>
</tr>
<tr class="even">
<td></td>
<td>LessThanOrEqual</td>
<td>Akzeptieren Sie nur Zeilen, deren Spaltenwert kleiner oder gleich einem angegebenen Wert ist.</td>
</tr>
<tr class="odd">
<td></td>
<td>LessThan</td>
<td>Akzeptieren Sie nur Zeilen, deren Spaltenwert kleiner als ein angegebener Wert ist.</td>
</tr>
<tr class="even">
<td></td>
<td>GreaterThanOrEqual</td>
<td>Akzeptieren Sie nur Zeilen, deren Spaltenwert größer oder gleich einem angegebenen Wert ist.</td>
</tr>
<tr class="odd">
<td></td>
<td>GreaterThan</td>
<td>Akzeptieren Sie nur Zeilen, deren Spaltenwert größer als ein angegebener Wert ist.</td>
</tr>
<tr class="even">
<td></td>
<td>Bitmaskequalszero</td>
<td>Akzeptieren Sie nur Zeilen, die über einen Spaltenwert und eine angegebene Bitmaske verfügen, der NULL ergibt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Bitmasklotequalszero</td>
<td>Akzeptieren Sie nur Zeilen mit einem Spaltenwert, der mit einer angegebenen Bitmaske und einem Wert ungleich 0 (null) versehen ist.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
