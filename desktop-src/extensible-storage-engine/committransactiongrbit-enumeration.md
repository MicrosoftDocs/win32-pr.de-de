---
description: 'Weitere Informationen zu: CommitTransactionGrbit-Enumeration'
title: CommitTransactionGrbit-Enumeration
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec61d29a2bfc3fc502b532b83dbb02640a600a0a5034c9751caab7185f1b037c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117716649"
---
# <a name="committransactiongrbit-enumeration"></a>CommitTransactionGrbit-Enumeration

Optionen für JetCommitTransaction.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a>Member

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>LazyFlush</td>
<td>Für die Transaktion wird normal ein Commit ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokolldatei geleert wird, bevor sie an den Aufrufer zurückgegeben wird. Dadurch wird die Dauer eines Commitvorgangs auf Kosten der Dauerhaftigkeit drastisch reduziert. Jede Transaktion, die vor einem Absturz nicht in das Protokoll geleert wird, wird während der Absturzwiederherstellung beim nächsten Aufruf von JetInit automatisch abgebrochen. Wenn WaitLastLevel0Commit oder WaitAllLevel0Commit angegeben sind, wird diese Option ignoriert.</td>
</tr>
<tr class="odd">
<td></td>
<td>WaitLastLevel0Commit</td>
<td>Wenn für die Sitzung zuvor ein Commit für Transaktionen ausgeführt wurde und sie noch nicht in die Transaktionsprotokolldatei geleert wurden, sollten sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie an den Aufrufer zurückgegeben wird. Dies ist nützlich, wenn die Anwendung zuvor mithilfe von JET_bitCommitLazyFlush mehrere Transaktionen ausgeführt hat und nun alle Transaktionen auf den Datenträger leeren möchte.
<p>Diese Option kann auch dann verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet. Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
