---
description: 'Weitere Informationen finden Sie unter: Api.RetrieveColumnAsByte-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Api.RetrieveColumnAsByte-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100838
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc7268c19235a806b47a27ec1671ed18dbceda46129d3927dd9f7e11edf2818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983040"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid"></a>Api.RetrieveColumnAsByte-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID)

Ruft einen Bytespaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
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

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\>  
Die aus der Spalte als Byte abgerufenen Daten. NULL, wenn die Spalte NULL ist.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[RetrieveColumnAsByte-Überladung](./api.retrievecolumnasbyte-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
