---
description: 'Weitere Informationen finden Sie unter: Api.IntersectIndexes-Methode'
title: Api.IntersectIndexes-Methode
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88bcc872fc557e3942a119845206661bd48705317163520924059af5456f6e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983680"
---
# <a name="apiintersectindexes-method"></a>Api.IntersectIndexes-Methode

Überschneiden Sie eine Gruppe von Indexbereichen, und geben Sie die Lesezeichen der Datensätze zurück, die in allen Indexbereichen gefunden werden. Siehe auch [JetIntersectIndexes(JET_SESID, \[ \] , Int32, JET_RECORDLIST, IntersectIndexesGrbit).](./api.jetintersectindexes-method.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableids  
    Typ: \[\]  
    
    Die zu verwendenden tableids. Jede tableid muss aus einem anderen Index in derselben Tabelle sein und über einen aktiven Indexbereich verfügen. Verwenden [Sie JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit),](./api.jetsetindexrange-method.md) um einen Indexbereich zu erstellen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\>  
Die Lesezeichen der Datensätze, die in allen Indexbereichen gefunden werden. Die Lesezeichen werden in der Reihenfolge des Primärschlüssels zurückgegeben.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
