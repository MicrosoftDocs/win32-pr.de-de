---
description: Weitere Informationen finden Sie in der esentstopwatch. threadstats-Eigenschaft.
title: Esentstopwatch. threadstats (Eigenschaft)
TOCTitle: 'ThreadStats property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch.threadstats(v=EXCHG.10)
ms:contentKeyID: 55102996
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.get_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.set_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 241b7d80e86eb3c773aecd58b7d16e749e040611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357832"
---
# <a name="esentstopwatchthreadstats-property"></a>Esentstopwatch. threadstats (Eigenschaft)

Ruft die gesamte ESENT-Arbeitsstatistik ab, die von der aktuellen Instanz gemessen wird.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ThreadStats As JET_THREADSTATS
    Get
    Private Set
'Usage
Dim instance As EsentStopwatch
Dim value As JET_THREADSTATS

value = instance.ThreadStats
```

``` csharp
public JET_THREADSTATS ThreadStats { get; private set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentstopwatch-Klasse](./esentstopwatch-class.md)

[Esentstopwatch-Member](./esentstopwatch-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
