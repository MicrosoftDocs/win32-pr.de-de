---
description: 'Weitere Informationen finden Sie unter: API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, setcolumngrbit, JET_SETINFO)'
title: API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, setcolumngrbit, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100804
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5afebba00c784abf5bf71ac0f524376bd0f3b066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357067"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-setcolumngrbit-jet_setinfo"></a>API. jetsetcolumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, setcolumngrbit, JET_SETINFO)

Die jetsetcolumn-Funktion ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, um eingefügt zu werden, oder um den aktuellen Datensatz zu aktualisieren. Es kann einen vorhandenen Wert überschreiben, einen neuen Wert zu einer Sequenz von Werten in einer mehrwertigen Spalte hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder den gesamten oder einen Teil eines Long-Werts aktualisieren (eine Spalte vom Typ [LONGTEXT](./jet-coltyp-enumeration.md) oder [LONGBINARY](./jet-coltyp-enumeration.md)).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, von der das Update durchgeführt wird.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, der aktualisiert werden soll. Ein Update sollte vorbereitet werden.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Das festzulegende ColumnID.

<!-- end list -->

  - Daten  
    Sorte \[\]  
    
    Die festzulegenden Daten.

<!-- end list -->

  - dataSize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe der festzulegenden Daten.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. setcolumngrbit](./setcolumngrbit-enumeration.md)  
    
    SetColumn-Optionen.

<!-- end list -->

  - SetInfo  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SETINFO](./jet-setinfo-class.md)  
    
    Wird verwendet, um ITAG oder einen Offset mit langen Werten anzugeben.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein Warnungs Code.  

## <a name="remarks"></a>Bemerkungen

Die SetColumn-Methoden bieten DataType-spezifische über schreibungen, die möglicherweise effizienter sind.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetsetcolumn-Überladung](./api.jetsetcolumn-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
