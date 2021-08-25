---
description: 'Weitere Informationen zu: JET_SNPROG.cunitTotal-Eigenschaft'
title: JET_SNPROG.cunitTotal-Eigenschaft
TOCTitle: 'cunitTotal property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snprog.cunittotal(v=EXCHG.10)
ms:contentKeyID: 55103955
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.set_cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.get_cunitTotal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23ebab88e121ffdfb5114ef7c732f2975e6864fcc5b3d5f10bea7ef3c00082c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945080"
---
# <a name="jet_snprogcunittotal-property"></a>JET_SNPROG.cunitTotal-Eigenschaft

Ruft die Anzahl der Arbeitseinheiten ab, die abgeschlossen werden müssen. Dieser Wert ist immer größer oder gleich cunitDone.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cunitTotal As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_SNPROG
Dim value As Integer

value = instance.cunitTotal
```

``` csharp
public int cunitTotal { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_SNPROG-Klasse](./jet-snprog-class.md)

[JET_SNPROG-Member](./jet-snprog-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
