---
description: Weitere Informationen finden Sie in der stringcolumnvalue. Value-Eigenschaft.
title: Stringcolumnvalue. Value-Eigenschaft
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55104098
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b1f5dc65f41e1714858c75bed2c22e23680b60cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363395"
---
# <a name="stringcolumnvaluevalue-property"></a>Stringcolumnvalue. Value-Eigenschaft

Ruft den Wert der Spalte ab oder legt ihn fest. Verwenden Sie [SetColumns (JET_SESID, JET_TABLEID, \[ \] )](./api.setcolumns-method.md) , um einen Datensatz mit dem Spaltenwert zu aktualisieren.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Value As String
    Get
    Set
'Usage
Dim instance As StringColumnValue
Dim value As String

value = instance.Value

instance.Value = value
```

``` csharp
public string Value { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Stringcolumnvalue-Klasse](./stringcolumnvalue-class.md)

[Stringcolumnvalue-Member](./stringcolumnvalue-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
