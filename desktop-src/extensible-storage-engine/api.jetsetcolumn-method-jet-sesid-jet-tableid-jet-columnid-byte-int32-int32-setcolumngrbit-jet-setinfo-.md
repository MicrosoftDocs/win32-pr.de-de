---
description: 'Weitere Informationen finden Sie unter: Api.JetSetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)'
title: Api.JetSetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100801
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aab9e57caed54bac02f2ad7cc62ff313a41bd0c4158082d310798e6210fb674a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977800"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-setcolumngrbit-jet_setinfo"></a>Api.JetSetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, SetColumnGrbit, JET_SETINFO)

Die JetSetColumn-Funktion ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, um eingefügt oder den aktuellen Datensatz zu aktualisieren. Sie kann einen vorhandenen Wert überschreiben, einer Sequenz von Werten in einer mehrwertigen Spalte einen neuen Wert hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder einen long-Wert (eine Spalte vom Typ [LongText](./jet-coltyp-enumeration.md) oder [LongBinary)](./jet-coltyp-enumeration.md)ganz oder teilweise aktualisieren.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, die das Update vor sich hat.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu aktualisierende Cursor. Ein Update sollte vorbereitet werden.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Die columnid, die festgelegt werden soll.

<!-- end list -->

  - data  
    Typ: \[\]  
    
    Die festzulegenden Daten.

<!-- end list -->

  - dataSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe der daten, die festgelegt werden soll.

<!-- end list -->

  - dataOffset  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Der Offset im Datenpuffer, aus dem Daten festgelegt werden.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)  
    
    SetColumn-Optionen.

<!-- end list -->

  - setinfo  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)  
    
    Wird verwendet, um itag oder long-value offset anzugeben.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein Warnwert.  

## <a name="remarks"></a>Hinweise

Dies ist eine nur interne Version der API, die einen Datenpuffer und einen Offset in den Puffer übernimmt.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetSetColumn-Überladung](./api.jetsetcolumn-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
