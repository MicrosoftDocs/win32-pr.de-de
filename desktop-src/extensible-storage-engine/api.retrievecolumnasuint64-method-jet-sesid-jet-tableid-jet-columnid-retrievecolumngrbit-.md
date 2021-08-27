---
description: 'Weitere Informationen finden Sie unter: Api.RetrieveColumnAsUInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Api.RetrieveColumnAsUInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint64(v=EXCHG.10)
ms:contentKeyID: 55100907
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee2b3ec2952d9acf65c63b1ddae668a3f112905f475e379d715972ef94f471af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977070"
---
# <a name="apiretrievecolumnasuint64-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>Api.RetrieveColumnAsUInt64-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)

Ruft einen uint64-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of ULong)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of ULong)

returnValue = Api.RetrieveColumnAsUInt64(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ulong> RetrieveColumnAsUInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, aus dem die Spalte abgerufen werden soll.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Die abzurufende columnid.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Abrufoptionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\>  
Die aus der Spalte als UInt64 abgerufenen Daten. NULL, wenn die Spalte NULL ist.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[RetrieveColumnAsUInt64-Überladung](./api.retrievecolumnasuint64-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
