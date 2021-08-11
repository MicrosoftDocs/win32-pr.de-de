---
description: 'Weitere Informationen zu: InstanceParameters.LogBuffers-Eigenschaft'
title: InstanceParameters.LogBuffers-Eigenschaft
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60fbf06d13a8252051830c9a91dd348c2a7295a63212b587bfac9905b3b5903a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255961"
---
# <a name="instanceparameterslogbuffers-property"></a>InstanceParameters.LogBuffers-Eigenschaft

Ruft den Arbeitsspeicher ab, der zum Zwischenspeichern von Protokolldatensätzen verwendet wird, bevor sie in die Transaktionsprotokolldatei geschrieben werden, oder legt diesen fest. Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokolldateien enthält. Die Sektorgröße beträgt fast immer 512 Bytes, daher ist es sicher, diese Größe für die Einheit anzunehmen. Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell voll werden. Eine größere Cachegröße für die Transaktionsprotokolldatei ist entscheidend für eine gute Updateleistung unter einem solchen hohen Auslastungszustand. Der Standardwert ist für diesen Fall bekanntlich zu klein. Legen Sie diesen Parameter nicht auf eine Anzahl von Puffern fest, die größer (in Bytes) als die Hälfte der Größe einer Transaktionsprotokolldatei ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[InstanceParameters-Klasse](./instanceparameters-class.md)

[InstanceParameters-Member](./instanceparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
