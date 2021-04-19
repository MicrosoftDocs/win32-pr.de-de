---
description: Weitere Informationen finden Sie in der System Parameters. keymost-Eigenschaft.
title: System Parameters. keymost-Eigenschaft
TOCTitle: 'KeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.KeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.keymost(v=EXCHG.10)
ms:contentKeyID: 55104043
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.KeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_KeyMost
- Microsoft.Isam.Esent.Interop.SystemParameters.KeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f211e6d5a93679c49ae26e08152190d105f05ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350064"
---
# <a name="systemparameterskeymost-property"></a>System Parameters. keymost-Eigenschaft

Ruft die maximale Schlüsselgröße ab. Dies hängt von der ESENT-Version und der Datenbankseiten Größe ab.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared ReadOnly Property KeyMost As Integer
    Get
'Usage
Dim value As Integer

value = SystemParameters.KeyMost
```

``` csharp
public static int KeyMost { get; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
