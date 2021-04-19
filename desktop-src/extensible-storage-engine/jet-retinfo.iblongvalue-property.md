---
description: 'Weitere Informationen finden Sie hier: JET_RETINFO. iblongvalue-Eigenschaft'
title: JET_RETINFO. iblongvalue (Eigenschaft)
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103801
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39b2ed312f7db54ff799ce2aa52554349d020dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345149"
---
# <a name="jet_retinfoiblongvalue-property"></a>JET_RETINFO. iblongvalue (Eigenschaft)

Ruft den Offset auf das erste Byte ab, das aus einer Spalte vom Typ [LONGBINARY](./jet-coltyp-enumeration.md)oder [LONGTEXT](./jet-coltyp-enumeration.md)abgerufen werden soll, oder legt diesen fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RETINFO-Klasse](./jet-retinfo-class.md)

[Mitglieder JET_RETINFO](./jet-retinfo-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
