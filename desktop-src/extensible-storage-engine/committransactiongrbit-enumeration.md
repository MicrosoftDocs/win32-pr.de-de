---
description: Weitere Informationen finden Sie unter CommitTransactionGrbit-Enumeration.
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
ms.openlocfilehash: efe052fc01014d3ebb624dbd4183bc8f0584b145
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481786"
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


|  | Membername | Beschreibung | 
|--|-------------|-------------|
|  | Keine | Standardoptionen. | 
|  | LazyFlush | Für die Transaktion wird normalerweise ein Committed ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokolldatei geleert wird, bevor sie an den Aufrufer zurückkehrt. Dadurch wird die Dauer eines Commit-Vorgangs auf Kosten der Dauerhaftigkeit drastisch reduziert. Alle Transaktionen, die vor einem Absturz nicht in das Protokoll geleert werden, werden während der Absturzwiederherstellung beim nächsten Aufruf von JetInit automatisch abgebrochen. Wenn WaitLastLevel0Commit oder WaitAllLevel0Commit angegeben ist, wird diese Option ignoriert. | 
|  | WaitLastLevel0Commit | Wenn die Sitzung zuvor transaktionen ausgeführt hat und sie noch nicht in die Transaktionsprotokolldatei geleert wurden, sollten sie sofort geleert werden. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie zum Aufrufer zurückkehrt. Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mithilfe von JET_bitCommitLazyFlush und nun alle transaktionen auf den Datenträger leeren möchte.<p>Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet. Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</p> | 



## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
