---
description: 'Weitere Informationen finden Sie hier: JET_DBINFOMISC. cbpagesize-Eigenschaft'
title: JET_DBINFOMISC. cbpagesize (Eigenschaft)
TOCTitle: 'cbPageSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.cbpagesize(v=EXCHG.10)
ms:contentKeyID: 39512879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae2f718c066c1b0cef347141f08e1ed1254e6bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346937"
---
# <a name="jet_dbinfomisccbpagesize-property"></a>JET_DBINFOMISC. cbpagesize (Eigenschaft)

Ruft die Größe der Datenbankseite ab. Der Wert 0 bedeutet 4-KB-Seiten.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbPageSize As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.cbPageSize
```

``` csharp
public int cbPageSize { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_DBINFOMISC-Klasse](./jet-dbinfomisc-class.md)

[Mitglieder JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
