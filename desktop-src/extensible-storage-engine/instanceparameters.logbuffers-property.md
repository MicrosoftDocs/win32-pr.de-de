---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. logbuffers.
title: Instanceparameters. logbuffers (Eigenschaft)
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
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363665"
---
# <a name="instanceparameterslogbuffers-property"></a>Instanceparameters. logbuffers (Eigenschaft)

Dient zum Abrufen oder Festlegen des Speichers, der zum Zwischenspeichern von Protokolldaten Sätzen verwendet wird, bevor Sie in die Transaktionsprotokoll Datei geschrieben werden. Die Einheit für diesen Parameter ist die Sektorgröße des Volumes, das die Transaktionsprotokoll Dateien enthält. Die Sektorgröße beträgt fast immer 512 Bytes, sodass es sicher ist, dass diese Größe für die Einheit angenommen wird. Dieser Parameter wirkt sich auf die Leistung aus. Wenn die Auslastung der Datenbank-Engine stark ausgelastet ist, kann dieser Puffer sehr schnell vollständig werden. Eine größere Cache Größe für die Transaktionsprotokoll Datei ist wichtig für eine gute Aktualisierungs Leistung bei einer solchen hohen Lade Bedingung. Der Standardwert ist für diesen Fall zu klein. Legen Sie diesen Parameter nicht auf eine größere Anzahl von Puffern (in Bytes) als die Hälfte der Größe einer Transaktionsprotokoll Datei fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
