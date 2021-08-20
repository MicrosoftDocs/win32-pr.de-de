---
description: Weitere Informationen finden Sie unter SystemParameters.OutstandingIOMax (Eigenschaft).
title: SystemParameters.OutstandingIOMax (Eigenschaft)
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 820ff3d1351d72505c0d78d590b49ae291bfd3df51fa8477d3026ca9a1683abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117702302"
---
# <a name="systemparametersoutstandingiomax-property"></a>SystemParameters.OutstandingIOMax (Eigenschaft)

Dieser Parameter steuert, wie viele Datenbankdatei-E/A-Dateien pro Datenträger gleichzeitig im Hostbetriebssystem in die Warteschlange gestellt werden können. Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich verbessern.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
