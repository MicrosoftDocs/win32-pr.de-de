---
description: 'Weitere Informationen finden Sie unter: JET_THREADSTATS. Create-Methode'
title: JET_THREADSTATS. Create-Methode (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a3450835a90c3e21902a6097d9cfb672c51769cc00810d86e338bef40ce2565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251902"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS. Create-Methode

Erstellen Sie eine [JET_THREADSTATS](./jet-threadstats-structure2.md) Struktur mit dem angegebenen Wert.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a>Parameter

  - cPageReferenced  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der besuchten Seiten.

<!-- end list -->

  - cPageRead  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der gelesenen Seiten.

<!-- end list -->

  - cPagePreread  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der vorab gelesenen Seiten.

<!-- end list -->

  - cPageDirtied  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    TNumber of pages dirtied.

<!-- end list -->

  - cPageRedirtied  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der neu ierten Seiten.

<!-- end list -->

  - cLogRecord  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der generierten Protokolldatensätze.

<!-- end list -->

  - cbLogRecord  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Geschriebene Bytes von Protokolldatensätzen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Eine neue [JET_THREADSTATS](./jet-threadstats-structure2.md) struktur mit den angegebenen Werten.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_THREADSTATS-Struktur](./jet-threadstats-structure2.md)

[JET_THREADSTATS Member](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
