---
description: Weitere Informationen zur ColumnValue.Error-Eigenschaft
title: ColumnValue.Error-Eigenschaft
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.error(v=EXCHG.10)
ms:contentKeyID: 55101202
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Error
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Error
- Microsoft.Isam.Esent.Interop.ColumnValue.set_Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ffbbb66992ecff218b7fdbd7577e2ffbd9f63694ae41967ebc8240f84ebe3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042358"
---
# <a name="columnvalueerror-property"></a>ColumnValue.Error-Eigenschaft

Ruft die Warnung ab, die durch Abrufen oder Festlegen dieser Spalte generiert wird.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Error As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As ColumnValue
Dim value As JET_wrn

value = instance.Error
```

``` csharp
public JET_wrn Error { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[ColumnValue-Klasse](./columnvalue-class.md)

[ColumnValue-Elemente](./columnvalue-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
