---
description: 'Weitere Informationen finden Sie unter: API. jetgetinstanceingefo-Methode'
title: API. jetgetinstancinput Info-Methode
TOCTitle: 'JetGetInstanceInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo(System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetinstanceinfo(v=EXCHG.10)
ms:contentKeyID: 55100729
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetInstanceInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b618c0eb7bf6e861337ebb40a95cb75d4434038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214498"
---
# <a name="apijetgetinstanceinfo-method"></a>API. jetgetinstancinput Info-Methode

Ruft Informationen zu den Instanzen ab, die ausgeführt werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetInstanceInfo ( _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO() _
)
'Usage
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()

Api.JetGetInstanceInfo(numInstances, _
    instances)
```

``` csharp
public static void JetGetInstanceInfo(
    out int numInstances,
    out JET_INSTANCE_INFO[] instances
)
```

#### <a name="parameters"></a>Parameter

  - numinstance  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl von-Instanzen zurück.

<!-- end list -->

  - instances  
    Sorte \[\]  
    
    Gibt ein Array von instanzinformationsobjekten zurück, eines für jede laufende Instanz.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
