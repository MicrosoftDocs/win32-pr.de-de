---
description: 'Weitere Informationen finden Sie unter: Api.JetGetBookmark-Methode'
title: Api.JetGetBookmark-Methode
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d63bf41af250fcef6328433132fe64dcbdc862dcf8e35990c1ef1cbd02185e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085479"
---
# <a name="apijetgetbookmark-method"></a>Api.JetGetBookmark-Methode

Ruft das Lesezeichen für den Datensatz ab, der dem Indexeintrag an der aktuellen Position eines Cursors zugeordnet ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von [JetGotoBookmark(JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetgotobookmark-method.md)wieder zum gleichen Datensatz zu positionieren. Das Lesezeichen ist nicht länger als [BookmarkMost bytes.](./systemparameters.bookmarkmost-property.md) Siehe auch [GetBookmark(JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
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
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
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
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, aus dem das Lesezeichen abgerufen werden soll.

<!-- end list -->

  - Lesezeichen (bookmark)  
    Typ: \[\]  
    
    Puffer, der das Lesezeichen enthalten soll.

<!-- end list -->

  - bookmarkSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Größe des Lesezeichenpuffers.

<!-- end list -->

  - actualBookmarkSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe des Lesezeichens zurück.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
