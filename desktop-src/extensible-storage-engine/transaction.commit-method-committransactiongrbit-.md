---
description: 'Weitere Informationen zu: Transaction. Commit-Methode (committransaktiongrbit)'
title: Transaction. Commit-Methode (committransaktiongrbit)
TOCTitle: Commit method (CommitTransactionGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104071
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 048071a08d1211d6091fb6c2c23f9cfe302f8872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217226"
---
# <a name="transactioncommit-method-committransactiongrbit"></a>Transaction. Commit-Methode (committransaktiongrbit)

Commit für eine Transaktion durchsetzen. Dieses Objekt sollte sich in einer Transaktion befinden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit

instance.Commit(grbit)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. committransaktiongrbit](./committransactiongrbit-enumeration.md)  
    
    Jetcommittransaction-Optionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Transaktionsklasse](./transaction-class.md)

[Transaktions Mitglieder](./transaction-members.md)

[Commit-Überladung](./transaction.commit-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
