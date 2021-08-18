---
description: 'Weitere Informationen finden Sie unter: SystemParameters.LegacyFileNames-Eigenschaft'
title: SystemParameters.LegacyFileNames(Eigenschaft)
TOCTitle: 'LegacyFileNames property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104128
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.LegacyFileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_LegacyFileNames
- Microsoft.Isam.Esent.Interop.SystemParameters.LegacyFileNames
- Microsoft.Isam.Esent.Interop.SystemParameters.set_LegacyFileNames
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73739bda83f83eddbbfa090925b873d78aaeaa1dcdbcce9c527e5467f0f0acf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015955"
---
# <a name="systemparameterslegacyfilenames-property"></a>SystemParameters.LegacyFileNames(Eigenschaft)

Ruft die Abwärtskompatibilität mit den Dateinamenskonventionen früherer Versionen der Datenbank-Engine ab oder legt diese fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property LegacyFileNames As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.LegacyFileNames

SystemParameters.LegacyFileNames = value
```

``` csharp
public static int LegacyFileNames { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
