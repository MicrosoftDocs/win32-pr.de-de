---
description: 'Weitere Informationen finden Sie hier: Server2003Grbits. WaitAllLevel0Commit Field'
title: Server2003Grbits. WaitAllLevel0Commit-Feld (Microsoft. ISAM. ESENT. Interop. Server2003)
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
ms.openlocfilehash: 16390069adf81ead8e819bc5148a88e30900b508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865611"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a>Server2003Grbits. WaitAllLevel0Commit-Feld

Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde und die noch nicht in die Transaktionsprotokoll Datei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden. Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet. Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Server2003Grbits-Klasse](./server2003grbits-class.md)

[Server2003Grbits-Member](./server2003grbits-members.md)

[Microsoft. ISAM. ESENT. Interop. Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
