---
description: 'Weitere Informationen über: Server2003Api. JetUpdate2-Methode'
title: Server2003Api. JetUpdate2-Methode (Microsoft. ISAM. ESENT. Interop. Server2003)
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
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128156"
---
# <a name="server2003apijetupdate2-method"></a>Server2003Api. JetUpdate2-Methode

Die jetupdate-Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete (JET_SESID JET_TABLEID)](./api.jetdelete-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, von der das Update gestartet wurde.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, der aktualisiert werden soll. Ein Update sollte vorbereitet werden.

<!-- end list -->

  - Lesezeichen (bookmark)  
    Sorte \[\]  
    
    Gibt das Lesezeichen des aktualisierten Datensatzes zurück. Diese kann NULL sein.

<!-- end list -->

  - bookmarksize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des Lesezeichen Puffers.

<!-- end list -->

  - actualbookmarksize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe des Lesezeichens zurück.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. Server2003. updategrbit](./updategrbit-enumeration.md)  
    
    Aktualisierungs Optionen.

## <a name="remarks"></a>Bemerkungen

Jetupdate ist der letzte Schritt beim Ausführen eines Einfügevorgangs oder eines Updates. Das Update wird durch Aufrufen von [jetprepareupdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) und anschließendes Aufrufen von [jetsetcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, setcolumngrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) zum Festlegen des Daten Satz Zustands gestartet. Schließlich wird JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, updategrbit) aufgerufen, um den Aktualisierungs Vorgang abzuschließen. Indizes werden nur von jetupdate oder und nicht von jetsetcolumn aktualisiert.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Server2003Api-Klasse](./server2003api-class.md)

[Server2003Api-Member](./server2003api-members.md)

[Microsoft. ISAM. ESENT. Interop. Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
