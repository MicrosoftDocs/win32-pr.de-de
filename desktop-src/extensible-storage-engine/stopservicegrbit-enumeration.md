---
description: Weitere Informationen finden Sie in der stopservicegrbit-Enumeration.
title: Stopservicegrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows8)
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
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348213"
---
# <a name="stopservicegrbit-enumeration"></a>Stopservicegrbit-Enumeration

Optionen für [JetStopServiceInstance2 (JET_INSTANCE, stopservicegrbit)](./windows8api.jetstopserviceinstance2-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Membername</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Alle</td>
<td>Beendet alle ESE-Dienste für die angegebene-Instanz.</td>
</tr>
<tr class="even">
<td></td>
<td>Backgroundusertasks</td>
<td>Beendet neu startable-Client spezifische Hintergrund Wartungs Tasks (B +-Struktur Defragmentierung).</td>
</tr>
<tr class="odd">
<td></td>
<td>Stilllegung</td>
<td>Versetzt alle Dirty Caches auf den Datenträger. Asynchron. Der inaktiven Vorgang wird abgebrochen, wenn das Fortsetzungs Bit später aufgerufen wird.</td>
</tr>
<tr class="even">
<td></td>
<td>Fortsetzen</td>
<td>Setzt zuvor ausgestellte Stopp Dienst Vorgänge fort, d. h., der &quot; Dienst wird neu gestartet &quot; . Kann mit oberhalb von grbits kombiniert werden, um bestimmte Dienste fortzusetzen, oder mit 0x0 werden alle vorherigen beendeten Dienste fortgesetzt.
<p>Warnung: dieses Bit kann nur verwendet werden, um JET_bitStopServiceBackground und JET_bitStopServiceQuiesceCaches fortzusetzen, wenn Sie eine JET_bitStopServiceAll oder JET_bitStopServiceAPI durchgeführt haben, schlägt der Versuch, JET_bitStopServiceResume zu verwenden, fehl.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
