---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMNID.ctagSequence-Eigenschaft'
title: JET_ENUMCOLUMNID.ctagSequence-Eigenschaft
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e60ae86a27f1c82a237ae9c02e54298cbe6aa7de251e9c1c38d7bc08dad42cc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890899"
---
# <a name="jet_enumcolumnidctagsequence-property"></a>JET_ENUMCOLUMNID.ctagSequence-Eigenschaft

Ruft die Anzahl der Spaltenwerte (nach einem basierenden Index) ab, die für die angegebene Spalten-ID aufgezählt werden, oder legt diese fest. Wenn ctagSequence 0 (null) ist, wird rgtagSequence ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufzählt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMNID-Klasse](./jet-enumcolumnid-class.md)

[JET_ENUMCOLUMNID Mitglieder](./jet-enumcolumnid-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
