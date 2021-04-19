---
description: Weitere Informationen finden Sie in der API. JetSetCurrentIndex4-Methode.
title: API. JetSetCurrentIndex4-Methode
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
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346500"
---
# <a name="apijetsetcurrentindex4-method"></a>API. JetSetCurrentIndex4-Methode

Legen Sie den aktuellen Index eines Cursors fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, für den der Index festgelegt werden soll.

<!-- end list -->

  - Index  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Name des Indexes, der ausgewählt werden soll. Wenn dieser Wert NULL oder leer ist, wird der primäre Index ausgewählt.

<!-- end list -->

  - indexid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    Die ID des Indexes, der ausgewählt werden soll. Diese ID kann mithilfe von jetgetindexinfo oder jetgettableindexinfo mit der [IndexID](./jet-idxinfo-enumeration.md) -Option abgerufen werden.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. setcurrentindexgrbit](./setcurrentindexgrbit-enumeration.md)  
    
    Legen Sie Index Optionen fest.

<!-- end list -->

  - itagsequence  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Sequenznummer des Werts für mehrwertige Spalten, der verwendet wird, um den Cursor auf dem neuen Index zu positionieren. Dieser Parameter wird nur in Verbindung mit [nomove](./setcurrentindexgrbit-enumeration.md)verwendet. Wenn dieser Parameter nicht vorhanden oder auf 0 (null) festgelegt ist, wird als Wert 1 angenommen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
