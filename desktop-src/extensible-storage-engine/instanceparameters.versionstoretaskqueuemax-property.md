---
description: 'Weitere Informationen zu: InstanceParameters.VersionStoreTaskQueueMax-Eigenschaft'
title: InstanceParameters.VersionStoreTaskQueueMax-Eigenschaft
TOCTitle: 'VersionStoreTaskQueueMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.versionstoretaskqueuemax(v=EXCHG.10)
ms:contentKeyID: 55103554
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_VersionStoreTaskQueueMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5da5e2e0ac354d3263e4ef4feb0a44a20bd3b458a7375b0fa1c8a6ce75a79e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017650"
---
# <a name="instanceparametersversionstoretaskqueuemax-property"></a>InstanceParameters.VersionStoreTaskQueueMax-Eigenschaft

Ruft die Anzahl der Arbeitselemente für die Hintergrundbereinigung ab, die jederzeit in die Warteschlange des Datenbank-Engine-Threadpools eingereiht werden können, oder legt diese fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property VersionStoreTaskQueueMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.VersionStoreTaskQueueMax

instance.VersionStoreTaskQueueMax = value
```

``` csharp
public int VersionStoreTaskQueueMax { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[InstanceParameters-Klasse](./instanceparameters-class.md)

[InstanceParameters-Member](./instanceparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
