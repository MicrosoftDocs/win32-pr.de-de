---
description: 'Weitere Informationen finden Sie unter: Feld "Server2003Grbits.WaitAllLevel0Commit"'
title: Feld "Server2003Grbits.WaitAllLevel0Commit" (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c6f3946d12b7614818545abc785d521e46b9c05ddedcffab09750846861782e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093170"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a>Feld "Server2003Grbits.WaitAllLevel0Commit"

Alle Transaktionen, für die zuvor ein Committed von einer Sitzung ausgeführt wurde, die noch nicht in die Transaktionsprotokolldatei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie zum Aufrufer zurückkehrt. Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet. Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Server2003Grbits-Klasse](./server2003grbits-class.md)

[Server2003Grbits-Member](./server2003grbits-members.md)

[Microsoft.Isam.Esent.Interop.Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
