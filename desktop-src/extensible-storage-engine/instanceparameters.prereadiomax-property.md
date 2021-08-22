---
description: 'Weitere Informationen zu: InstanceParameters.PrereadIOMax-Eigenschaft'
title: InstanceParameters.PrereadIOMax-Eigenschaft
TOCTitle: 'PrereadIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PrereadIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.prereadiomax(v=EXCHG.10)
ms:contentKeyID: 55103559
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PrereadIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PrereadIOMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PrereadIOMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PrereadIOMax
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc3af75d137b07df729d987ac4942612ac88aded08d546378b89146d5ae121ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617930"
---
# <a name="instanceparametersprereadiomax-property"></a>InstanceParameters.PrereadIOMax-Eigenschaft

Ruft die maximale Anzahl von E/A-Vorgängen ab, die für einen bestimmten Zweck gesendet werden, oder legt diese fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property PrereadIOMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PrereadIOMax

instance.PrereadIOMax = value
```

``` csharp
public int PrereadIOMax { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[InstanceParameters-Klasse](./instanceparameters-class.md)

[InstanceParameters-Member](./instanceparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
