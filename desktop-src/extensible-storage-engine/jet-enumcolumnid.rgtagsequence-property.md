---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMNID.rgtagSequence-Eigenschaft'
title: JET_ENUMCOLUMNID.rgtagSequence-Eigenschaft
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 026432a6d5b2363df09640141ec9f190d6637258692ce8233b32c004a1dbde86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765966"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a>JET_ENUMCOLUMNID.rgtagSequence-Eigenschaft

Ruft das Array von einsbasierten Indizes im Array von Spaltenwerten für eine bestimmte Spalte ab oder legt dieses fest. Ein einzelnes Element ist eine itagSequence, die in der JET_RETRIEVECOLUMN. Eine itagSequence von 0 (null) bedeutet "skip". Eine itagSequence von 1 bedeutet, dass der erste Spaltenwert der Spalte, 2 die zweite Spalte und so weiter zurückgeben.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: \[\]  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMNID-Klasse](./jet-enumcolumnid-class.md)

[JET_ENUMCOLUMNID Mitglieder](./jet-enumcolumnid-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
