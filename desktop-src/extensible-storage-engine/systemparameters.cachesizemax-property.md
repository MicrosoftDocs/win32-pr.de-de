---
description: 'Weitere Informationen zu: SystemParameters.CacheSizeMax-Eigenschaft'
title: SystemParameters.CacheSizeMax-Eigenschaft
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98c54ee57c28c97829f8b86e65bbc990f758092ec7a97ae9dd5087e1ff8ebe1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117702697"
---
# <a name="systemparameterscachesizemax-property"></a>SystemParameters.CacheSizeMax-Eigenschaft

Ruft die maximale Größe des Datenbankseitencaches ab oder legt diese fest. Die Größe wird auf Datenbankseiten angezeigt. Wenn dieser Parameter auf seinen Standardwert festgelegt wird, wird die maximale Größe des Caches auf die Größe des physischen Arbeitsspeichers festgelegt, wenn JetInit aufgerufen wird.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Referenz

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
