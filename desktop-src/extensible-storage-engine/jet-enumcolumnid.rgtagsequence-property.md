---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNID. rgtagsequence-Eigenschaft'
title: JET_ENUMCOLUMNID. rgtagsequence (Eigenschaft)
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
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749857"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a>JET_ENUMCOLUMNID. rgtagsequence (Eigenschaft)

Ruft das Array von einbasierten Indizes in das Array von Spaltenwerten für eine angegebene Spalte ab oder legt dieses fest. Bei einem einzelnen Element handelt es sich um eine in JET_RETRIEVECOLUMN definierte itagsequence. Eine itagsequence-Wert von 0 (null) bedeutet "Skip". Eine itagsequence von 1 bedeutet, dass der erste Spaltenwert der Spalte zurückgegeben wird, der Wert 2 für den zweiten Wert usw.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Sorte \[\]  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMNID-Klasse](./jet-enumcolumnid-class.md)

[Mitglieder JET_ENUMCOLUMNID](./jet-enumcolumnid-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
