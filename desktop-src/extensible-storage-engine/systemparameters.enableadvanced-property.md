---
description: 'Weitere Informationen zu: SystemParameters.EnableAdvanced-Eigenschaft'
title: SystemParameters.EnableAdvanced-Eigenschaft
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07fd683ad6f2f0d2a9afd88b46a7786131e15c370c9046945ad3e9594a533391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106998"
---
# <a name="systemparametersenableadvanced-property"></a>SystemParameters.EnableAdvanced-Eigenschaft

Ruft einen Wert ab, der angibt, ob die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt, oder legt diesen fest. Dieser Parameter wird in Verbindung mit [Configuration](./systemparameters.configuration-property.md) verwendet, um zu verhindern, dass einige Systemparameter von den Standardwerten der ausgewählten Konfiguration entfernt werden. Wird ab Windows Vista unterstützt. Wird auf Windows XP und Windows Server 2003 ignoriert.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
