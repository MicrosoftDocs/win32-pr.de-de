---
description: Weitere Informationen finden Sie in der seekgrbit-Enumeration.
title: Seekgrbit-Enumeration
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
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356202"
---
# <a name="seekgrbit-enumeration"></a>Seekgrbit-Enumeration

Optionen für JetSeek.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Seekeq</td>
<td>Der Cursor wird am Index Eintrag positioniert, der am nächsten am Anfang des Indexes liegt, der exakt mit dem Suchschlüssel übereinstimmt.</td>
</tr>
<tr class="even">
<td></td>
<td>Seeklt</td>
<td>Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Seekgt</td>
<td>Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</td>
</tr>
<tr class="even">
<td></td>
<td>Setindexrange</td>
<td>Ein Index Bereich wird automatisch für alle Schlüssel eingerichtet, die exakt mit dem Suchschlüssel übereinstimmen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
