---
description: 'Weitere Informationen finden Sie unter: instanceparameters. TempDirectory-Eigenschaft'
title: Instanceparameters. TempDirectory-Eigenschaft
TOCTitle: 'TempDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.tempdirectory(v=EXCHG.10)
ms:contentKeyID: 55103324
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bbe31b7f437f045f601b18daf92877784d58512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960871"
---
# <a name="instanceparameterstempdirectory-property"></a>Instanceparameters. TempDirectory-Eigenschaft

Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die temporäre Datenbank für die-Instanz enthält, oder legt ihn fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property TempDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.TempDirectory

instance.TempDirectory = value
```

``` csharp
public string TempDirectory { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
