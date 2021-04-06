---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS. Create-Methode'
title: JET_THREADSTATS. Create-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
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
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758491"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS. Create-Methode

Erstellen Sie eine neue [JET_THREADSTATS](./jet-threadstats-structure2.md) Struktur mit dem angegebenen Wert.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - cpagereferenziert  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Anzahl der besuchten Seiten.

<!-- end list -->

  - cpageread  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Anzahl der gelesenen Seiten.

<!-- end list -->

  - cpagepreread  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der Seiten, die Voraussetzungen sind.

<!-- end list -->

  - cpagedirtied  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Tnumber der Seiten, für die ein Pfad verwendet wurde.

<!-- end list -->

  - cPageRedirtied  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Anzahl der Seiten, für die ein erneuter Versuch besteht.

<!-- end list -->

  - clogrecord  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Anzahl der generierten Protokolldaten Sätze.

<!-- end list -->

  - cblogdatensatz  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Bytes der geschriebenen Protokolldaten Sätze.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Eine neue [JET_THREADSTATS](./jet-threadstats-structure2.md) Struktur mit den angegebenen Werten.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_THREADSTATS Struktur](./jet-threadstats-structure2.md)

[Mitglieder JET_THREADSTATS](./jet-threadstats-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
