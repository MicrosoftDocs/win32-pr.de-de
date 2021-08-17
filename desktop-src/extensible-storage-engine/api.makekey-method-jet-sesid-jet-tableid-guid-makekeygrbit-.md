---
description: 'Weitere Informationen finden Sie unter: Api.MakeKey-Methode (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)'
title: Api.MakeKey-Methode (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Guid,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100823
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 636593d6591c5b6fb39b6ea8079992fd75a397dbd072f757cce52a74601d328e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084777"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-guid-makekeygrbit"></a>Api.MakeKey-Methode (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)

Erstellt einen Suchschlüssel, der dann von [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) und [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit) verwendet](./api.jetsetindexrange-method.md)werden kann.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Guid, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Guid
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    Guid data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, für den der Schlüssel erstellt werden soll.

<!-- end list -->

  - data  
    Typ: [System.Guid](/dotnet/api/system.guid)  
    
    Spaltendaten für die aktuelle Schlüsselspalte des aktuellen Indexes.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)  
    
    Schlüsseloptionen.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[MakeKey-Überladung](./api.makekey-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
