---
description: 'Weitere Informationen finden Sie unter: instanceparameters. LogFileDirectory-Eigenschaft'
title: Instanceparameters. LogFileDirectory (Eigenschaft)
TOCTitle: 'LogFileDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfiledirectory(v=EXCHG.10)
ms:contentKeyID: 55103562
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileDirectory
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4977185809372c5ec20deff15ca1eba11434881b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366257"
---
# <a name="instanceparameterslogfiledirectory-property"></a>Instanceparameters. LogFileDirectory (Eigenschaft)

Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, der die Transaktionsprotokolle für die-Instanz enthält, oder legt ihn fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property LogFileDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.LogFileDirectory

instance.LogFileDirectory = value
```

``` csharp
public string LogFileDirectory { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
