---
description: Weitere Informationen finden Sie unter MakeKeyGrbit-Enumeration.
title: MakeKeyGrbit-Enumeration
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5adfb504237710277a75e3c5ecb12e00e8bf54042a01ca1b794a63f2795f3db0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071854"
---
# <a name="makekeygrbit-enumeration"></a>MakeKeyGrbit-Enumeration

Optionen für JetMakeKey.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
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
<td>Keine</td>
<td>Standardoptionen.</td>
</tr>
<tr class="even">
<td></td>
<td>NewKey</td>
<td>Es sollte ein neuer Suchschlüssel erstellt werden. Alle zuvor vorhandenen Suchschlüssel werden verworfen.</td>
</tr>
<tr class="odd">
<td></td>
<td>NormalizedKey</td>
<td>Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert, alle zuvor vorhandenen Suchschlüssel werden verworfen, und der Inhalt des Eingabepuffers wird als neuer Suchschlüssel geladen.</td>
</tr>
<tr class="even">
<td></td>
<td>KeyDataZeroLength</td>
<td>Wenn die Größe des Eingabepuffers 0 (null) ist und die aktuelle Schlüsselspalte eine Spalte variabler Länge ist, gibt diese Option an, dass der Eingabepuffer einen Wert der Länge 0 (null) enthält. Andernfalls würde eine Eingabepuffergröße von 0 (null) einen NULL-Wert angeben.</td>
</tr>
<tr class="odd">
<td></td>
<td>StrLimit</td>
<td>Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte kommen, als Platzhalter betrachtet werden sollen.</td>
</tr>
<tr class="even">
<td></td>
<td>SubStrLimit</td>
<td>Diese Option gibt an, dass der Suchschlüssel so konstruiert werden soll, dass die aktuelle Schlüsselspalte als Präfix-Platzhalter betrachtet wird und dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte kommen, als Platzhalter betrachtet werden sollen.</td>
</tr>
<tr class="odd">
<td></td>
<td>FullColumnStartLimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass alle Schlüsselspalten nach der aktuellen Schlüsselspalte als Platzhalter betrachtet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>FullColumnEndLimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stehen, als Platzhalter betrachtet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>PartialColumnStartLimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass die aktuelle Schlüsselspalte als Präfix-Platzhalter betrachtet wird und dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stammen, als Platzhalter betrachtet werden sollten.</td>
</tr>
<tr class="even">
<td></td>
<td>PartialColumnEndLimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass die aktuelle Schlüsselspalte als Präfix-Platzhalter betrachtet wird und dass alle Schlüsselspalten, die nach der aktuellen Schlüsselspalte stammen, als Platzhalter betrachtet werden sollten.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
