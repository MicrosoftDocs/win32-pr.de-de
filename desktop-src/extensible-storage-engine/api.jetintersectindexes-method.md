---
description: Weitere Informationen finden Sie in der API. jetintersectindexes-Methode.
title: API. jetintersectindexes-Methode
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960892"
---
# <a name="apijetintersectindexes-method"></a>API. jetintersectindexes-Methode

Berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus unterschiedlichen sekundären Indizes für dieselbe Tabelle. Dieser Vorgang ist nützlich, um die Gruppe von Datensätzen in einer Tabelle zu suchen, die mit zwei oder mehr Kriterien übereinstimmen, die mithilfe von Index Bereichen ausgedrückt werden können. Siehe auch [intersectindexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - ranges  
    Sorte \[\]  
    
    Ein, der die zu Intersect Ende Index Bereiche ist. Für den TableIDs-Wert in den Bereichen müssen Index Bereiche festgelegt sein. Verwenden Sie [jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)](./api.jetsetindexrange-method.md) , um einen Index Bereich zu erstellen.

<!-- end list -->

  - numbereiche  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der Index Bereiche.

<!-- end list -->

  - RecordList  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_RECORDLIST](./jet-recordlist-class.md)  
    
    Gibt Informationen über die temporäre Tabelle zurück, die die Überschneidungs Ergebnisse enthält.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. intersectindexesgrbit](./intersectindexesgrbit-enumeration.md)  
    
    Schnittstellen Optionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
