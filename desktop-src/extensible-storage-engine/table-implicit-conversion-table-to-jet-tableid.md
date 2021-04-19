---
description: 'Weitere Informationen finden Sie unter: Tabelle implizite Konvertierung (Tabelle in JET_TABLEID)'
title: Implizite Tabellen Konvertierung (Tabelle in JET_TABLEID)
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360685"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a>Implizite Tabellen Konvertierung (Tabelle in JET_TABLEID)

Impliziter Konvertierungs Operator aus einer Tabelle in einen JET_TABLEID. Dadurch kann eine Tabelle mit APIs verwendet werden, die eine JET_TABLEID erwarten.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a>Parameter

  - table  
    Typ: [Microsoft. ISAM. ESENT. Interop. Table](./table-class.md)  
    
    Die zu konvertierende Tabelle.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
Der JET_TABLEID der Tabelle.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Table-Klasse](./table-class.md)

[Tabellen Mitglieder](./table-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
