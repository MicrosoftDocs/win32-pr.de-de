---
description: 'Weitere Informationen zu: JET_RETRIEVECOLUMN.ibLongValue-Eigenschaft'
title: JET_RETRIEVECOLUMN.ibLongValue-Eigenschaft
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103819
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_ibLongValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62b909e617e2401aad77e1cc361c1d4773059c02a06db86886ddae61bfcff512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093420"
---
# <a name="jet_retrievecolumniblongvalue-property"></a>JET_RETRIEVECOLUMN.ibLongValue-Eigenschaft

Ruft den Offset auf das erste Byte ab, das aus einer Spalte vom Typ [LongBinary](./jet-coltyp-enumeration.md) oder [LongText](./jet-coltyp-enumeration.md)abgerufen werden soll, oder legt diesen fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RETRIEVECOLUMN-Klasse](./jet-retrievecolumn-class.md)

[JET_RETRIEVECOLUMN-Member](./jet-retrievecolumn-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
