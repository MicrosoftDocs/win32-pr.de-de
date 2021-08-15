---
description: 'Weitere Informationen finden Sie unter: Api.JetSetCurrentIndex4-Methode'
title: Api.JetSetCurrentIndex4-Methode
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53b35384607e988c2456f4d48f93b49b6974b138e4a71ef8916b174a92a61611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118497884"
---
# <a name="apijetsetcurrentindex4-method"></a>Api.JetSetCurrentIndex4-Methode

Legen Sie den aktuellen Index eines Cursors fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, für den der Index festgelegt werden soll.

<!-- end list -->

  - Index  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Name des auszuwählenden Indexes. Wenn dies NULL oder leer ist, wird der primäre Index ausgewählt.

<!-- end list -->

  - indexid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    Die ID des auszuwählende Indexes. Diese ID kann mit JetGetIndexInfo oder JetGetTableIndexInfo mit der [Option IndexId](./jet-idxinfo-enumeration.md) abgerufen werden.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)  
    
    Legen Sie Indexoptionen fest.

<!-- end list -->

  - itagSequence  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Sequenznummer des mehrwertigen Spaltenwerts, der verwendet wird, um den Cursor auf dem neuen Index zu positionieren. Dieser Parameter wird nur in Verbindung mit [NoMove](./setcurrentindexgrbit-enumeration.md)verwendet. Wenn dieser Parameter nicht vorhanden ist oder auf 0 (null) festgelegt ist, wird davon ausgegangen, dass sein Wert 1 ist.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
