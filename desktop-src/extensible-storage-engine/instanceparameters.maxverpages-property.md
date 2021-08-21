---
description: 'Weitere Informationen zu: InstanceParameters.MaxVerPages-Eigenschaft'
title: InstanceParameters.MaxVerPages-Eigenschaft
TOCTitle: 'MaxVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxverpages(v=EXCHG.10)
ms:contentKeyID: 55103318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxVerPages
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ce33867409725a017ee5e80a936e40ecdb0c280f37d92718412d97502002452
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039378"
---
# <a name="instanceparametersmaxverpages-property"></a>InstanceParameters.MaxVerPages-Eigenschaft

Ruft die maximale Anzahl von Versionsspeicherseiten ab, die für diese Instanz reserviert sind, oder legt diese fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property MaxVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxVerPages

instance.MaxVerPages = value
```

``` csharp
public int MaxVerPages { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[InstanceParameters-Klasse](./instanceparameters-class.md)

[InstanceParameters-Member](./instanceparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
