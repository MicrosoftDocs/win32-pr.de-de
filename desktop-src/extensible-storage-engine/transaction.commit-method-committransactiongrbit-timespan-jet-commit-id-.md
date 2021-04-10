---
description: 'Weitere Informationen finden Sie unter: Transaction. Commit-Methode (committransaktiongrbit, TimeSpan, JET_COMMIT_ID)'
title: Transaction. Commit-Methode (committransaktiongrbit, TimeSpan, JET_COMMIT_ID)
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
ms.openlocfilehash: 18df363e4320a4b1a53c34e15fcf68939fce96ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042727"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a>Transaction. Commit-Methode (committransaktiongrbit, TimeSpan, JET_COMMIT_ID)

Commit für eine Transaktion durchsetzen. Dieses Objekt sollte sich in einer Transaktion befinden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [Microsoft. ISAM. ESENT. Interop. committransaktiongrbit](./committransactiongrbit-enumeration.md)  
    
    Jetcommittransaction-Optionen.

<!-- end list -->

  - durablecommit  
    Typ: [System. TimeSpan](/dotnet/api/system.timespan)  
    
    Dauer für das Commit von verzögerten Transaktionen.

<!-- end list -->

  - commitId  
    Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Commit-ID für diesen Commitdatensatz.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Transaktionsklasse](./transaction-class.md)

[Transaktions Mitglieder](./transaction-members.md)

[Commit-Überladung](./transaction.commit-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
