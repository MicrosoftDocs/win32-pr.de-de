---
description: 'Weitere Informationen zu: Api.JetRetrieveColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Api.JetRetrieveColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100790
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d8bba8812882ac9d239b49589f089e8ed47c5f2b05102113c1e3270eb82a37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977809"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-retrievecolumngrbit-jet_retinfo"></a>Api.JetRetrieveColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)

Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursorkopierpuffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Indexeintrag abrufen, der auf den aktuellen Datensatz verweist. Neben dem Abrufen des tatsächlichen Spaltenwerts kann JetRetrieveColumn auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, damit die Größe der Anwendungspuffer entsprechend angepasst werden kann.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    actualDataSize, grbit, retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
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

  - data  
    Typ: \[\]  
    
    Der Datenpuffer, in den abgerufen werden soll.

<!-- end list -->

  - dataSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe des Datenpuffers.

<!-- end list -->

  - actualDataSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe des Datenpuffers zurück.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Abrufen von Spaltenoptionen.

<!-- end list -->

  - retinfo  
    Typ: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Wenn pretinfo als NULL angegeben wird, verhält sich die Funktion so, als ob eine ItagSequence von 1 und ein ibLongValue von 0 (null) angegeben worden wären. Dies bewirkt, dass der Spaltenabruf den ersten Wert einer mehrwertigen Spalte abruft und lange Daten bei Offset 0 (null) abruft.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein ESENT-Warnungscode.  

## <a name="remarks"></a>Hinweise

Die RetrieveColumnAs-Funktionen stellen datentypspezifische Abruffunktionen bereit.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetRetrieveColumn-Überladung](./api.jetretrievecolumn-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
