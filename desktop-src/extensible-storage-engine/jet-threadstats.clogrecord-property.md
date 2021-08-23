---
description: 'Weitere Informationen finden Sie unter: JET_THREADSTATS.cLogRecord-Eigenschaft'
title: JET_THREADSTATS.cLogRecord-Eigenschaft (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cLogRecord property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cLogRecord
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.clogrecord(v=EXCHG.10)
ms:contentKeyID: 39511382
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cLogRecord
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cLogRecord
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c4e33e7055e2197a024cf71f21d153841c8ab945604e09810c368d9c3174105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667730"
---
# <a name="jet_threadstatsclogrecord-property"></a>JET_THREADSTATS.cLogRecord-Eigenschaft

Ruft die Gesamtzahl der Transaktionsprotokolldatensätze ab, die von der Datenbank-Engine im aktuellen Thread generiert wurden.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cLogRecord As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cLogRecord
```

``` csharp
public int cLogRecord { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_THREADSTATS-Struktur](./jet-threadstats-structure2.md)

[JET_THREADSTATS Mitglieder](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
