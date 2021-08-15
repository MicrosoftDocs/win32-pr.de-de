---
description: 'Weitere Informationen zu: SystemParameters.StartFlushThreshold-Eigenschaft'
title: SystemParameters.StartFlushThreshold-Eigenschaft
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49a868bf06f6994d61e3f901d5d9a447d2ef63c7909c33db3689fda343e16c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484859"
---
# <a name="systemparametersstartflushthreshold-property"></a>SystemParameters.StartFlushThreshold-Eigenschaft

Ruft den Schwellenwert ab, ab dem der Datenbankseitencache beginnt, Seiten aus dem Cache zu entfernen, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden, oder legt diesen fest. Wenn die Anzahl der Seitenpuffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um diesen Pool verfügbarer Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von JET_paramCacheSizeMax festgelegt wird. Dieser Schwellenwert muss auch immer kleiner als der durch JET_paramStopFlushThreshold festgelegte Stoppschwellenwert sein. Die Entfernungshöhe des Startschwellenwerts bestimmt die Antwortzeit, die der Datenbankseitencache benötigt, um verfügbare Puffer zu erzeugen, bevor die Anwendung sie benötigt. Ein hoher Startschwellenwert gibt dem Hintergrundprozess mehr Zeit zum Reagieren. Ein hoher Startschwellenwert impliziert jedoch einen höheren Stoppschwellenwert, der die effektive Größe des Datenbankseitencaches reduziert.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[SystemParameters-Klasse](./systemparameters-class.md)

[SystemParameters-Member](./systemparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
