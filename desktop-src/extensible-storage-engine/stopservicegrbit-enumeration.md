---
description: Weitere Informationen finden Sie unter StopServiceGrbit-Enumeration.
title: StopServiceGrbit-Enumeration (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c8280bf4abfbc9eb5818d1aab460a17298db7b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477456"
---
# <a name="stopservicegrbit-enumeration"></a>StopServiceGrbit-Enumeration

Optionen für [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Member


|  | Membername | BESCHREIBUNG | 
|--|-------------|-------------|
|  | Alle | Beendet alle ESE-Dienste für die angegebene Instanz. | 
|  | BackgroundUserTasks | Beendet neu startbare clientspezifische Hintergrundwartungsaufgaben (B+-Strukturdefragmentierung). | 
|  | QuiesceCaches | Macht alle dirty Caches auf den Datenträger in Ruhe. Asynchron. Das Ruhen wird abgebrochen, wenn das Resume-Bit anschließend aufgerufen wird. | 
|  | Fortsetzen | Setzt zuvor ausgegebene StopService-Vorgänge fort, d. h. "startet den Dienst neu". Kann mit den oben genannten Grbits kombiniert werden, um bestimmte Dienste wieder aufzunehmen, oder mit 0x0 alle vorherigen beendeten Dienste fortsetzen.<p>Warnung: Dieses Bit kann nur zum Fortsetzen von JET_bitStopServiceBackground und JET_bitStopServiceQuiesceCaches verwendet werden, wenn Sie eine JET_bitStopServiceAll- oder JET_bitStopServiceAPI-JET_bitStopServiceResume verwenden.</p> | 



## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
