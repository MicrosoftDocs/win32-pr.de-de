---
description: 'Weitere Informationen zu: TermGrbit-Enumeration'
title: TermGrbit-Enumeration
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83bf60be88aa1db7bac30c96c0c438d453c6fc24279b18502205ce96e60b9f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978370"
---
# <a name="termgrbit-enumeration"></a>TermGrbit-Enumeration

Optionen für [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
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
<td>Abgeschlossen</td>
<td>Fordert an, dass die Instanz sauber heruntergefahren wird. Alle optionalen Bereinigungsarbeiten, die normalerweise zur Laufzeit im Hintergrund ausgeführt werden, werden sofort abgeschlossen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Abrupten</td>
<td>Fordert an, dass die Instanz so schnell wie möglich heruntergefahren wird. Alle optionalen Arbeiten, die normalerweise zur Laufzeit im Hintergrund ausgeführt werden, werden abgebrochen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[Schmutzig](./windows7grbits.dirty-field.md)
