---
description: 'Weitere Informationen finden Sie hier: System Parameters. legacyfilename-Eigenschaft'
title: System Parameters. legacyfile filename (Eigenschaft)
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
ms.openlocfilehash: 57dd9987ff419d889f80795d07e16c28ef46dc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218248"
---
# <a name="systemparameterslegacyfilenames-property"></a>System Parameters. legacyfile filename (Eigenschaft)

Ruft die Abwärtskompatibilität mit den Datei Benennungs Konventionen früherer Versionen der Datenbank-Engine ab oder legt Sie fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
