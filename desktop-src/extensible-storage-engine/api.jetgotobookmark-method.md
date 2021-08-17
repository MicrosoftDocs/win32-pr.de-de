---
description: 'Weitere Informationen finden Sie unter: Api.JetGotoBookmark-Methode'
title: Api.JetGotoBookmark-Methode
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff1675637493ffb4aca910fa2030c9e205a953112e294e98231f99ad746f6ce9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117590"
---
# <a name="apijetgotobookmark-method"></a>Api.JetGotoBookmark-Methode

Positioniert einen Cursor an einem Indexeintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist. Das Lesezeichen kann mit jedem Index verwendet werden, der für eine Tabelle definiert ist. Das Lesezeichen für einen Datensatz kann mit [JetGetBookmark(JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) abgerufen werden.](./api.jetgetbookmark-method.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, der positioniert werden soll.

<!-- end list -->

  - Lesezeichen (bookmark)  
    Typ: \[\]  
    
    Das Lesezeichen, das zum Positionieren des Cursors verwendet wird.

<!-- end list -->

  - bookmarkSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe des Lesezeichens.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
