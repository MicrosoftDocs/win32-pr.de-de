---
description: 'Weitere Informationen finden Sie unter: JET_THREADSTATS.cbLogRecord-Eigenschaft'
title: JET_THREADSTATS.cbLogRecord-Eigenschaft (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cbLogRecord property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cblogrecord(v=EXCHG.10)
ms:contentKeyID: 39511575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cbLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cbLogRecord
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fd244391a0a4565f27db58671ce9dc950d5c676a6396fba27d4f89f76dc1d02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979190"
---
# <a name="jet_threadstatscblogrecord-property"></a>JET_THREADSTATS.cbLogRecord-Eigenschaft

Ruft die Gesamtgröße von Transaktionsprotokolldatensätzen in Bytes ab, die von der Datenbank-Engine im aktuellen Thread generiert wurden.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbLogRecord As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cbLogRecord
```

``` csharp
public int cbLogRecord { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_THREADSTATS Struktur](./jet-threadstats-structure2.md)

[JET_THREADSTATS-Member](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
