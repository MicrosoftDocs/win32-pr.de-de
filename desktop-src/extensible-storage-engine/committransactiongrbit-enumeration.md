---
description: Weitere Informationen finden Sie in der committransaktiongrbit-Enumeration.
title: Committransaktiongrbit-Enumeration
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
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366330"
---
# <a name="committransactiongrbit-enumeration"></a>Committransaktiongrbit-Enumeration

Optionen für jetcommittransaction.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Lazyflush</td>
<td>Die Transaktion wird normal ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokoll Datei geleert wurde, bevor Sie an den Aufrufer zurückgegeben wird. Dadurch wird die Dauer eines Commitvorgangs drastisch reduziert und die Dauerhaftigkeit beeinträchtigt. Alle Transaktionen, die vor einem Absturz nicht in das Protokoll geschrieben werden, werden während des nächsten Aufrufens von jetinit automatisch abgebrochen. Wenn WaitLastLevel0Commit oder WaitAllLevel0Commit angegeben wird, wird diese Option ignoriert.</td>
</tr>
<tr class="odd">
<td></td>
<td>WaitLastLevel0Commit</td>
<td>Wenn für die Sitzung bereits ein Commit für Transaktionen ausgeführt wurde und diese noch nicht in die Transaktionsprotokoll Datei geleert wurden, sollten Sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden. Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mit JET_bitCommitLazyFlush committet hat und diese nun auf den Datenträger leeren möchte.
<p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet. Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
