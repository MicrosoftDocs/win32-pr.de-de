---
description: 'Weitere Informationen finden Sie hier: Windows8Api. jetsetcurrsorfilter-Methode'
title: Windows8Api. jetsetcurrsorfilter-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetSetCursorFilter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN[],Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetcursorfilter(v=EXCHG.10)
ms:contentKeyID: 55104447
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0137c25ee6ab548537d797af0a00a7ffcd1f6d5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359921"
---
# <a name="windows8apijetsetcursorfilter-method"></a>Windows8Api. jetsetcurrsorfilter-Methode

Legen Sie ein Array einfacher Filter für [jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md)fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetSetCursorFilter ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    filters As JET_INDEX_COLUMN(), _
    grbit As CursorFilterGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim filters As JET_INDEX_COLUMN()
Dim grbit As CursorFilterGrbitWindows8Api.JetSetCursorFilter(sesid, tableid, _
    filters, grbit)
```

``` csharp
public static void JetSetCursorFilter(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_COLUMN[] filters,
    CursorFilterGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die für den-Befehl zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, der positioniert werden soll.

<!-- end list -->

  - Filter  
    Sorte \[\]  
    
    Einfache Daten Satz Filter.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. Windows8. currsorfiltergrbit](./cursorfiltergrbit-enumeration.md)  
    
    Verschieben von Optionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Windows8Api-Klasse](./windows8api-class.md)

[Windows8Api-Member](./windows8api-members.md)

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
