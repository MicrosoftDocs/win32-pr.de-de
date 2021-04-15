---
description: 'Weitere Informationen finden Sie hier: JET_SETINFO. iblongvalue-Eigenschaft'
title: JET_SETINFO. iblongvalue (Eigenschaft)
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103918
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324b3cd5c45be8f463ff9b2a9cfe11f1dcad4554
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525562"
---
# <a name="jet_setinfoiblongvalue-property"></a>JET_SETINFO. iblongvalue (Eigenschaft)

Ruft den Offset bis zum ersten Byte ab, das in einer Spalte vom Typ [LONGBINARY](./jet-coltyp-enumeration.md) oder [LONGTEXT](./jet-coltyp-enumeration.md)festgelegt werden soll, oder legt diesen fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
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

[JET_SETINFO-Klasse](./jet-setinfo-class.md)

[Mitglieder JET_SETINFO](./jet-setinfo-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
