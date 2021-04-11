---
description: Weitere Informationen finden Sie in der instanceparameters. cachepriority-Eigenschaft.
title: Instanceparameters. cachepriority (Eigenschaft)
TOCTitle: 'CachePriority property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachePriority
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachepriority(v=EXCHG.10)
ms:contentKeyID: 55107435
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachePriority
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachePriority
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachePriority
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachePriority
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf57f833a12687d51521dda416b8ff1c04ebbc49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217567"
---
# <a name="instanceparameterscachepriority-property"></a>Instanceparameters. cachepriority (Eigenschaft)

Ruft die Eigenschaft pro Instanz für relative Cache Prioritäten (Standardwert = 100) ab oder legt Sie fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property CachePriority As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachePriority

instance.CachePriority = value
```

``` csharp
public int CachePriority { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
