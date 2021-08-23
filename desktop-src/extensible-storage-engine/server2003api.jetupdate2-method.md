---
description: 'Weitere Informationen finden Sie unter: Server2003Api.JetUpdate2-Methode'
title: Server2003Api.JetUpdate2-Methode (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f19d0bb4ab599e2f7a11ac66202c805066c1744b80ed72223d20be423340d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978570"
---
# <a name="server2003apijetupdate2-method"></a>Server2003Api.JetUpdate2-Methode

Die JetUpdate-Funktion führt einen Aktualisierungsvorgang aus, einschließlich einfügen einer neuen Zeile in eine Tabelle oder Aktualisieren einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [JetDelete(JET_SESID, JET_TABLEID).](./api.jetdelete-method.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
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

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)  
    
    Updateoptionen.

## <a name="remarks"></a>Hinweise

JetUpdate ist der letzte Schritt beim Ausführen eines Einfüge- oder Aktualisierungsschritts. Das Update wird gestartet, indem [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) und dann [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) einmal oder mehrmals aufgerufen wird, um den Datensatzzustand festzulegen. Schließlich wird JetUpdate2(JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit) aufgerufen, um den Updatevorgang abzuschließen. Indizes werden nur von JetUpdate oder nicht während JetSetColumn aktualisiert.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Server2003Api-Klasse](./server2003api-class.md)

[Server2003Api-Elemente](./server2003api-members.md)

[Microsoft.Isam.Esent.Interop.Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
