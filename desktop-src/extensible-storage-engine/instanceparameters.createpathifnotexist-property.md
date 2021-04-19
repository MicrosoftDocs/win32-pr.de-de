---
description: 'Weitere Informationen finden Sie hier: instanceparameters. kreatepthifnotexist-Eigenschaft'
title: Instanceparameters. kreatepthifnotexist-Eigenschaft
TOCTitle: 'CreatePathIfNotExist property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.createpathifnotexist(v=EXCHG.10)
ms:contentKeyID: 55103321
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d777c7bae3c375118488105e275edba59e57cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343385"
---
# <a name="instanceparameterscreatepathifnotexist-property"></a>Instanceparameters. kreatepthifnotexist-Eigenschaft

Ruft einen Wert ab, der angibt, ob ESENT automatisch Ordner erstellt, die in den Dateisystem Pfaden fehlen, oder legt diesen fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property CreatePathIfNotExist As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CreatePathIfNotExist

instance.CreatePathIfNotExist = value
```

``` csharp
public bool CreatePathIfNotExist { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
