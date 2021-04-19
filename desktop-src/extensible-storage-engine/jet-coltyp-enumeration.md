---
description: 'Weitere Informationen finden Sie hier: JET_coltyp-Enumeration'
title: JET_coltyp-Enumeration
TOCTitle: JET_coltyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_coltyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_coltyp(v=EXCHG.10)
ms:contentKeyID: 39511169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 616dc80d835e22502b6781355a2eff35a6375e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359496"
---
# <a name="jet_coltyp-enumeration"></a>JET_coltyp-Enumeration

ESENT-Spaltentypen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_coltyp
'Usage
Dim instance As JET_coltyp
```

``` csharp
public enum JET_coltyp
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
<td>Trägers</td>
<td>NULL-Spaltentyp. Ungültige Spalten Erstellung.</td>
</tr>
<tr class="even">
<td></td>
<td>bit</td>
<td>True, false oder NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>UnsignedByte</td>
<td>1-Byte-Ganzzahl ohne Vorzeichen.</td>
</tr>
<tr class="even">
<td></td>
<td>Short</td>
<td>ganze Zahl mit 2 Bytes, signiert.</td>
</tr>
<tr class="odd">
<td></td>
<td>Long</td>
<td>ganze Zahl mit 4 Bytes, signiert.</td>
</tr>
<tr class="even">
<td></td>
<td>Währung</td>
<td>8-Byte-Ganzzahl, signiert.</td>
</tr>
<tr class="odd">
<td></td>
<td>IEEESINGLE</td>
<td>4-Byte-IEEE-Single-precisions.</td>
</tr>
<tr class="even">
<td></td>
<td>IEEEDOUBLE</td>
<td>8-Byte-IEEE mit doppelter Genauigkeit.</td>
</tr>
<tr class="odd">
<td></td>
<td>Datetime</td>
<td>Ganzzahliges Datum, Bruch Zeit.</td>
</tr>
<tr class="even">
<td></td>
<td>Binary</td>
<td>Binärdaten, bis zu 255 Bytes.</td>
</tr>
<tr class="odd">
<td></td>
<td>Text</td>
<td>Textdaten, bis zu 255 Bytes.</td>
</tr>
<tr class="even">
<td></td>
<td>LongBinary</td>
<td>Binärdaten, bis zu 2 GB.</td>
</tr>
<tr class="odd">
<td></td>
<td>LongText</td>
<td>Textdaten (bis zu 2 GB).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
