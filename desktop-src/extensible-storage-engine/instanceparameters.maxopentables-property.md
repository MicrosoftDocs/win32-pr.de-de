---
description: 'Weitere Informationen finden Sie im folgenden Artikel: instanceparameters. maxOpenTables-Eigenschaft'
title: Instanceparameters. maxOpenTables (Eigenschaft)
TOCTitle: 'MaxOpenTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxopentables(v=EXCHG.10)
ms:contentKeyID: 55107442
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 623d2f1fe536fb2b5916c96e97de8904fa5a7c86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348747"
---
# <a name="instanceparametersmaxopentables-property"></a>Instanceparameters. maxOpenTables (Eigenschaft)

Ruft die Anzahl der für diese Instanz reservierten B +-strukturressourcen ab oder legt Sie fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property MaxOpenTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxOpenTables

instance.MaxOpenTables = value
```

``` csharp
public int MaxOpenTables { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
