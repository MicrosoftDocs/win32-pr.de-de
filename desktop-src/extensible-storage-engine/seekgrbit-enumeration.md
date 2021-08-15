---
description: Weitere Informationen finden Sie unter SeekGrbit-Enumeration.
title: SeekGrbit-Enumeration
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12a65021d8c224d2a0ed50082b3120c94fc8c83f25c9aaf3eaf6e71d3f3f45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978590"
---
# <a name="seekgrbit-enumeration"></a>SeekGrbit-Enumeration

Optionen für JetSeek.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
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
<td>SeekEQ</td>
<td>Der Cursor wird an dem Indexeintrag positioniert, der dem Anfang des Indexes am nächsten ist, der genau mit dem Suchschlüssel entspricht.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekLT</td>
<td>Der Cursor wird an dem Indexeintrag positioniert, der dem Ende des Indexes am nächsten liegt, der kleiner als ein Indexeintrag ist, der genau mit den Suchkriterien übereinstimmen würde.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>Der Cursor wird an dem Indexeintrag positioniert, der dem Ende des Indexes am nächsten liegt, der kleiner oder gleich einem Indexeintrag ist, der genau den Suchkriterien entspricht.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>Der Cursor wird an dem Indexeintrag positioniert, der dem Indexanfang am nächsten liegt, der größer oder gleich einem Indexeintrag ist, der genau mit den Suchkriterien übereinstimmen würde.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekGT</td>
<td>Der Cursor wird an dem Indexeintrag positioniert, der dem Indexanfang am nächsten liegt, der größer als ein Indexeintrag ist, der genau den Suchkriterien entspricht.</td>
</tr>
<tr class="even">
<td></td>
<td>SetIndexRange</td>
<td>Ein Indexbereich wird automatisch für alle Schlüssel eingerichtet, die genau mit dem Suchschlüssel übereinstimmen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
