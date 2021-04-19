---
description: 'Weitere Informationen finden Sie unter: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)'
title: API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100926
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 925d8483a799a23bc6551e6d3d13731c7f1f392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368989"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-int64"></a>API. SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)

Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Long _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As LongApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    long data
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, der aktualisiert werden soll. Ein Update sollte vorbereitet werden.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Das festzulegende ColumnID.

<!-- end list -->

  - Daten  
    Typ: [System. Int64](/dotnet/api/system.int64)  
    
    Die festzulegenden Daten.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[SetColumn-Überladung](./api.setcolumn-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
