---
description: 'Weitere Informationen finden Sie unter: Api.SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Boolesch)'
title: Api.SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Boolesch)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100917
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c4c70bd382656d460f3f3adf41f0f4fc13a1009d10d3600a2a16cff130ba02d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067020"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-boolean"></a>Api.SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Boolesch)

Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, um eingefügt oder den aktuellen Datensatz zu aktualisieren.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Boolean _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As BooleanApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    bool data
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu aktualisierende Cursor. Ein Update sollte vorbereitet werden.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Die columnid, die festgelegt werden soll.

<!-- end list -->

  - data  
    Typ: [System.Boolean](/dotnet/api/system.boolean)  
    
    Die festzulegenden Daten.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[SetColumn-Überladung](./api.setcolumn-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
