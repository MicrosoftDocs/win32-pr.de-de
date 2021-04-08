---
description: 'Weitere Informationen finden Sie unter: API. jetupdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)'
title: API. jetupdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)
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
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863219"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a>API. jetupdate-Methode (JET_SESID, JET_TABLEID, Byte, Int32, Int32)

Die jetupdate-Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete (JET_SESID JET_TABLEID)](./api.jetdelete-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

## <a name="remarks"></a>Bemerkungen

Jetupdate ist der letzte Schritt beim Ausführen eines Einfügevorgangs oder eines Updates. Das Update wird durch Aufrufen von [jetprepareupdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) und anschließendes Aufrufen von [jetsetcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, setcolumngrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) zum Festlegen des Daten Satz Zustands gestartet. Zum Schluss wird jetupdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) aufgerufen, um den Aktualisierungs Vorgang abzuschließen. Indizes werden nur von jetupdate oder und nicht von jetsetcolumn aktualisiert.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetupdate-Überladung](./api.jetupdate-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
