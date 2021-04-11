---
description: 'Weitere Informationen finden Sie unter: API. gettablecolumns-Methode (JET_SESID JET_TABLEID)'
title: API. gettablecolumns-Methode (JET_SESID, JET_TABLEID)
TOCTitle: GetTableColumns method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107218
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 393f730920ce7abb3ef24916c9e1c9e9591ba020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128069"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_tableid"></a>API. gettablecolumns-Methode (JET_SESID, JET_TABLEID)

Durchläuft alle Spalten in der Tabelle, wobei Informationen zu den einzelnen Spalten zurückgegeben werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die Spalten Informationen abgerufen werden sollen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\>  
Ein Iterator über ColumnInfo für jede Spalte in der Tabelle.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Gettablecolumns-Überladung](./api.gettablecolumns-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
