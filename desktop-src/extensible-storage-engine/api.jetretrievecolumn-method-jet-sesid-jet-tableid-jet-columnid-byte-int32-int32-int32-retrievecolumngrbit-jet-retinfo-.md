---
description: 'Weitere Informationen finden Sie unter: API. jetretrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)'
title: API. jetretrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349599"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a>API. jetretrievecolumschlag-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)

Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist. Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
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
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
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

  - Daten  
    Sorte \[\]  
    
    Der Datenpuffer, in den der abgerufen werden soll.

<!-- end list -->

  - dataSize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des Daten Puffers.

<!-- end list -->

  - dataOffset  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Offset im Datenpuffer, in den Daten gelesen werden sollen.

<!-- end list -->

  - actualdatasize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe des Daten Puffers zurück.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. retrievecolenngrbit](./retrievecolumngrbit-enumeration.md)  
    
    Abrufen von Spalten Optionen.

<!-- end list -->

  - retinfo  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Wenn pretinfo als NULL angegeben wird, verhält sich die Funktion so, als ob eine itagsequence von 1 und ein iblongvalue-Wert von 0 (null) angegeben wurde. Dies bewirkt, dass der Spalten Abruf den ersten Wert einer mehrwertigen Spalte abruft und lange Daten bei Offset 0 (null) abruft.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein ESENT-Warnungs Code.  

## <a name="remarks"></a>Bemerkungen

Dies ist eine interne Methode, die einen Puffer Offset und eine Größe einnimmt.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetretrievecolübern-Überladung](./api.jetretrievecolumn-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
