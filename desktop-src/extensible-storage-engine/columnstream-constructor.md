---
description: Weitere Informationen finden Sie unter ColumnStream-Konstruktor.
title: ColumnStream-Konstruktor
TOCTitle: 'ColumnStream constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff3395637609ab72046c0bcd53a4264721d022224c0a1ff33a1bbf9f6a71aeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982680"
---
# <a name="columnstream-constructor"></a>ColumnStream-Konstruktor

Initialisiert eine neue Instanz der ColumnStream-Klasse.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID

Dim instance As New ColumnStream(sesid, tableid, _
    columnid)
```

``` csharp
public ColumnStream(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu verwendende Cursor.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Die Columnid der Spalte, aus der Daten festgelegt/abgerufen werden.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[ColumnStream-Klasse](./columnstream-class.md)

[ColumnStream-Member](./columnstream-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
