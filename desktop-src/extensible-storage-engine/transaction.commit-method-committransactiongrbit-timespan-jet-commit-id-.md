---
description: 'Weitere Informationen zu: Transaction.Commit-Methode (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)'
title: Transaction.Commit-Methode (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
TOCTitle: Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104166
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90fd53fd7097db98ab84148b3f32710c369c948ed64c3606d0018cc8e79c877a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890513"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a>Transaction.Commit-Methode (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)

Committen einer Transaktion. Dieses Objekt sollte sich in einer Transaktion befindet.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_ID

instance.Commit(grbit, durableCommit, _
    commitId)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>Parameter

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)  
    
    JetCommitTransaction-Optionen.

<!-- end list -->

  - durableCommit  
    Typ: [System.TimeSpan](/dotnet/api/system.timespan)  
    
    Dauer des Commits für verzögerte Transaktionen.

<!-- end list -->

  - commitId  
    Typ: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Commit-ID für diesen Commitdatensatz.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Transaktionsklasse](./transaction-class.md)

[Transaktionsmember](./transaction-members.md)

[Commitüberladung](./transaction.commit-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
