---
description: 'Weitere Informationen finden Sie unter: Api.MakeKey-Methode (JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)'
title: Api.MakeKey-Methode (JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Single,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100826
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9036df71828f1f8b2a9982bc258d8655b9cba19c82f86657f671583b2fe1ec4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840630"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-single-makekeygrbit"></a>Api.MakeKey-Methode (JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)

Erstellt einen Suchschlüssel, der dann von [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) und [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit) verwendet](./api.jetsetindexrange-method.md)werden kann.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Single, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Single
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    float data,
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
    Typ: [System.Single](/dotnet/api/system.single)  
    
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
