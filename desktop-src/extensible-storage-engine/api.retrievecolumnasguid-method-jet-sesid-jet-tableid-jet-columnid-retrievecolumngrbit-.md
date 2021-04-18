---
description: 'Weitere Informationen finden Sie unter: API. retrievecolennasguid-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)'
title: API. retrievecolennasguid-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)
TOCTitle: RetrieveColumnAsGuid method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasguid(v=EXCHG.10)
ms:contentKeyID: 55100854
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5945cbedca8e628829fa8283a576913a641f6378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344023"
---
# <a name="apiretrievecolumnasguid-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a>API. retrievecolennasguid-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)

Ruft einen GUID-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function RetrieveColumnAsGuid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Guid)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Guid)

returnValue = Api.RetrieveColumnAsGuid(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<Guid> RetrieveColumnAsGuid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, von dem die Spalte abgerufen werden soll.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Das abzurufende ColumnID.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)  
    
    Abruf Optionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[Guid](/dotnet/api/system.guid)\>  
Die aus der Spalte abgerufenen Daten als GUID. NULL, wenn die Spalte NULL ist.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Retrievecolübernasguid-Überladung](./api.retrievecolumnasguid-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
