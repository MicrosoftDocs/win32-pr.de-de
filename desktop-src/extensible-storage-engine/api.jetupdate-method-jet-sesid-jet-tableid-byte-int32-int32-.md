---
description: Weitere Informationen zur Api.JetUpdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)
title: Api.JetUpdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bf9130715d35fb26b226a2b378f0eba2a853b742ee0a88319ed35f3a121f480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902465"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a>Api.JetUpdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)

Die JetUpdate-Funktion führt einen Aktualisierungsvorgang aus, einschließlich einfügen einer neuen Zeile in eine Tabelle oder Aktualisieren einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [JetDelete(JET_SESID, JET_TABLEID).](./api.jetdelete-method.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, die das Update gestartet hat.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu aktualisierende Cursor. Ein Update sollte vorbereitet werden.

<!-- end list -->

  - Lesezeichen (bookmark)  
    Typ: \[\]  
    
    Gibt das Lesezeichen des aktualisierten Datensatzes zurück. Diese kann NULL sein.

<!-- end list -->

  - bookmarkSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe des Lesezeichenpuffers.

<!-- end list -->

  - actualBookmarkSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe des Lesezeichens zurück.

## <a name="remarks"></a>Hinweise

JetUpdate ist der letzte Schritt beim Ausführen eines Einfüge- oder Aktualisierungsschritts. Das Update wird gestartet, indem [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) und dann [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) einmal oder mehrmals aufgerufen wird, um den Datensatzzustand festzulegen. Schließlich wird JetUpdate(JET_SESID, JET_TABLEID, , \[ \] Int32, Int32) aufgerufen, um den Updatevorgang abzuschließen. Indizes werden nur von JetUpdate oder nicht während JetSetColumn aktualisiert.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[JetUpdate-Überladung](./api.jetupdate-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
