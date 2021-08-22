---
description: 'Weitere Informationen zu: SystemParameters.StopFlushThreshold-Eigenschaft'
title: SystemParameters.StopFlushThreshold-Eigenschaft
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
ms.openlocfilehash: e383123a5886b1cf2e978f8b2faac80feb8e9ceb7daaa051dd6b778a8c189ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978460"
---
# <a name="systemparametersstopflushthreshold-property"></a>SystemParameters.StopFlushThreshold-Eigenschaft

Ruft den Schwellenwert ab, an dem der Datenbankseitencache das Entfernen von Seiten aus dem Cache beendet, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden, oder legt diesen fest. Wenn die Anzahl der Seitenpuffer im Cache diesen Schwellenwert überschreitet, wird der Hintergrundprozess beendet, der gestartet wurde, um diesen Pool verfügbarer Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von JET_paramCacheSizeMax festgelegt wird. Dieser Schwellenwert muss auch immer größer als der Startschwellenwert sein, der von JET_paramStartFlushThreshold festgelegt wird. Der Abstand zwischen dem Startschwellenwert und dem Beendigungsschwellenwert wirkt sich auf die Effizienz aus, mit der Datenbankseiten vom Hintergrundprozess geleert werden. Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten kombiniert werden können. Ein hoher Stopschwellenwert verringert jedoch die effektive Größe des Datenbankseitencaches.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
