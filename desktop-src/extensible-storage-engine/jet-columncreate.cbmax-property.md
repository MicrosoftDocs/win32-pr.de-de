---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNCREATE. cbmax-Eigenschaft'
title: JET_COLUMNCREATE. cbmax (Eigenschaft)
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103390
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_cbMax
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef30df9fd43bb9aa5b9ecb3eadf2f21ac4a8a4f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217564"
---
# <a name="jet_columncreatecbmax-property"></a>JET_COLUMNCREATE. cbmax (Eigenschaft)

Ruft die maximale Länge der Spalte ab oder legt Sie fest. Dies ist nur für Spalten vom Typ [Text](./jet-coltyp-enumeration.md), [LONGTEXT](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) und [LONGBINARY](./jet-coltyp-enumeration.md)von Bedeutung.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Set
'Usage
Dim instance As JET_COLUMNCREATE
Dim value As Integer

value = instance.cbMax

instance.cbMax = value
```

``` csharp
public int cbMax { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_COLUMNCREATE-Klasse](./jet-columncreate-class.md)

[Mitglieder JET_COLUMNCREATE](./jet-columncreate-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
