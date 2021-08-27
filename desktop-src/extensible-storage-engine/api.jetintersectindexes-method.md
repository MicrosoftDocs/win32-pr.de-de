---
description: 'Weitere Informationen finden Sie unter: Api.JetIntersectIndexes-Methode'
title: Api.JetIntersectIndexes-Methode
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
ms.openlocfilehash: 2b2e9e259d9c90a3067931fbba425ab1b21e5c2a36a73563f593d3b280a40496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978030"
---
# <a name="apijetintersectindexes-method"></a>Api.JetIntersectIndexes-Methode

Berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus verschiedenen sekundären Indizes für dieselbe Tabelle. Dieser Vorgang ist nützlich, um den Satz von Datensätzen in einer Tabelle zu finden, die zwei oder mehr Kriterien entsprechen, die mithilfe von Indexbereichen ausgedrückt werden können. Siehe auch [IntersectIndexes(JET_SESID, \[ \] )](./api.intersectindexes-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - ranges  
    Typ: \[\]  
    
    Ein der zu überschneidenden Indexbereiche. Für die tableids in den Bereichen müssen Indexbereiche festgelegt sein. Verwenden Sie [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit),](./api.jetsetindexrange-method.md) um einen Indexbereich zu erstellen.

<!-- end list -->

  - numRanges  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der Indexbereiche.

<!-- end list -->

  - Eintragsliste  
    Typ: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)  
    
    Gibt Informationen zur temporären Tabelle zurück, die die Schnittmengenergebnisse enthält.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)  
    
    Schnittmengenoptionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
