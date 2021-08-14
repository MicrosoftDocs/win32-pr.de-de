---
description: 'Weitere Informationen finden Sie unter: JET_INDEXCREATE.cbKeyMost-Eigenschaft.'
title: JET_INDEXCREATE.cbKeyMost-Eigenschaft
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17908b19cba3ed047b98f4532982001019516d9b32e2799c29a6671cbd862fe7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232680"
---
# <a name="jet_indexcreatecbkeymost-property"></a>JET_INDEXCREATE.cbKeyMost-Eigenschaft

Ruft die maximal zulässige Größe für Schlüssel im Index in Bytes ab oder legt diese fest. Die unterstützte maximale Mindestschlüsselgröße beträgt JET_cbKeyMostMin (255). Dies ist die maximale Legacyschlüsselgröße. Die maximale Schlüsselgröße hängt von der Datenbankseitengröße [DatabasePageSize ab.](./jet-param-enumeration.md) Die maximale Schlüsselgröße kann mit [KeyMost abgerufen werden.](./systemparameters.keymost-property.md) Dieser Parameter wird auf Windows XP und Windows Server 2003 ignoriert. Im Gegensatz zur nicht verwalteten API wird **IndexKeyMost()** (JET_bitIndexKeyMost) nicht benötigt, sie wird automatisch hinzugefügt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_INDEXCREATE-Klasse](./jet-indexcreate-class.md)

[JET_INDEXCREATE Mitglieder](./jet-indexcreate-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
