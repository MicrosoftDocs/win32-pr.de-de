---
description: 'Weitere Informationen zu: StopServiceGrbit-Enumeration'
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
ms.openlocfilehash: 7ecd096cc6d55aa989b758f7c30364844d160e59e5eba209f8e38c73ae87d0ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603820"
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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Alle</td>
<td>Beendet alle ESE-Dienste für die angegebene Instanz.</td>
</tr>
<tr class="even">
<td></td>
<td>BackgroundUserTasks</td>
<td>Beendet neustartbare clientspezifische Hintergrundwartungsaufgaben (B+-Strukturdefragmentierung).</td>
</tr>
<tr class="odd">
<td></td>
<td>QuiesceCaches</td>
<td>Lädt alle geänderten Caches in den Ruhespeicher auf den Datenträger. Asynchron. Die Stilllegung wird abgebrochen, wenn das Resume-Bit anschließend aufgerufen wird.</td>
</tr>
<tr class="even">
<td></td>
<td>Fortsetzen</td>
<td>Setzt zuvor ausgegebene StopService-Vorgänge fort, d.h. &quot; startet den Dienst &quot; neu. Kann mit obigen Grbits kombiniert werden, um bestimmte Dienste fortzusetzen, oder mit 0x0 Setzt alle vorherigen beendeten Dienste fort.
<p>Warnung: Dieses Bit kann nur verwendet werden, um JET_bitStopServiceBackground und JET_bitStopServiceQuiesceCaches fortzusetzen. Wenn Sie eine JET_bitStopServiceAll oder JET_bitStopServiceAPI haben, schlägt der Versuch, JET_bitStopServiceResume zu verwenden, fehl.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
