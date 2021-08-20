---
description: Erfahren Sie mehr über die Eigenschaft JET_COLUMNBASE.szBaseTableName.
title: JET_COLUMNBASE.szBaseTableName-Eigenschaft
TOCTitle: 'szBaseTableName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.szbasetablename(v=EXCHG.10)
ms:contentKeyID: 55103375
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_szBaseTableName
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_szBaseTableName
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 072bb967f4ed021a69dd6b275007bf47bcb4fcb8fc342cf639d1f98a6bf17cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118076076"
---
# <a name="jet_columnbaseszbasetablename-property"></a>JET_COLUMNBASE.szBaseTableName-Eigenschaft

Ruft die Tabelle ab, von der die aktuelle Tabelle ihre DDL erbt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szBaseTableName As String
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As String

value = instance.szBaseTableName
```

``` csharp
public string szBaseTableName { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_COLUMNBASE-Klasse](./jet-columnbase-class.md)

[JET_COLUMNBASE-Member](./jet-columnbase-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
