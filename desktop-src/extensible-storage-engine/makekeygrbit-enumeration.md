---
description: 'Weitere Informationen finden Sie hier: makekeygrbit-Enumeration'
title: Makekeygrbit-Enumeration
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
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128625"
---
# <a name="makekeygrbit-enumeration"></a>Makekeygrbit-Enumeration

Optionen für jetmakekey.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Es muss ein neuer Suchschlüssel erstellt werden. Alle bereits vorhandenen Suchschlüssel werden verworfen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Normalizedkey</td>
<td>Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert, alle bereits vorhandenen Suchschlüssel werden verworfen, und der Inhalt des Eingabe Puffers wird als neuer Suchschlüssel geladen.</td>
</tr>
<tr class="even">
<td></td>
<td>Keydatazerolength</td>
<td>Wenn die Größe des Eingabe Puffers NULL und die aktuelle Schlüssel Spalte eine Spalte variabler Länge ist, gibt diese Option an, dass der Eingabepuffer den Wert 0 (null) enthält. Andernfalls würde eine Eingabepuffergröße von NULL einen NULL-Wert angeben.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obergrenze</td>
<td>Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</td>
</tr>
<tr class="even">
<td></td>
<td>SubStrLimit</td>
<td>Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fullcolumnstartlimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Fullcolumnendlimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Partialcolumnstartlimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</td>
</tr>
<tr class="even">
<td></td>
<td>Partialcolumnendlimit</td>
<td>Der Suchschlüssel sollte so erstellt werden, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
