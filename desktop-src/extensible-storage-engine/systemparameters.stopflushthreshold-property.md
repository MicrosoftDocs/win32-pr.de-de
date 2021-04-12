---
description: 'Weitere Informationen finden Sie hier: System Parameters. stopflushthreshold-Eigenschaft'
title: System Parameters. stopflushthreshold (Eigenschaft)
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347968"
---
# <a name="systemparametersstopflushthreshold-property"></a>System Parameters. stopflushthreshold (Eigenschaft)

Ruft den Schwellenwert ab, an dem der Datenbankseiten Cache die Überprüfung von Seiten aus dem Cache beendet, um Platz für nicht zwischengespeicherte Seiten zu schaffen, oder legt diesen fest. Wenn die Anzahl der Seiten Puffer im Cache über diesem Schwellenwert liegt, wird der Hintergrundprozess beendet, der zum Auffüllen dieses Pools verfügbarer Puffer gestartet wurde. Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von JET_paramCacheSizeMax festgelegt wird. Dieser Schwellenwert muss auch immer größer sein als der Start Schwellenwert, der durch JET_paramStartFlushThreshold festgelegt wird. Der Abstand zwischen dem Start Schwellenwert und dem Schwellenwert für das Abbrechen wirkt sich auf die Effizienz aus, mit der Datenbankseiten durch den Hintergrundprozess geleert werden. Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten möglicherweise kombiniert werden. Ein Schwellenwert für hohe Beendigung verringert jedoch die effektive Größe des Datenbankseiten Caches.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
