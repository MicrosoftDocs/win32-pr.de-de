---
description: Weitere Informationen finden Sie in der crashdumpgrbit-Enumeration.
title: Crashdumpgrbit-Enumeration (Microsoft. ISAM. ESENT. Interop. Windows7)
TOCTitle: CrashDumpGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.crashdumpgrbit(v=EXCHG.10)
ms:contentKeyID: 39515535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3108190143115b1e6be5b7e0981d49c4bd9d4afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344239"
---
# <a name="crashdumpgrbit-enumeration"></a>Crashdumpgrbit-Enumeration

Optionen für jetkonfigurations reprocessforcrashdump.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CrashDumpGrbit
'Usage
Dim instance As CrashDumpGrbit
```

``` csharp
[FlagsAttribute]
public enum CrashDumpGrbit
```

## <a name="members"></a>Member

<table>
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
<td>Keine</td>
<td>Standardoptionen.</td>
</tr>
<tr class="even">
<td></td>
<td>Minimum</td>
<td>Das minimal Abbild umfasst cacheminimum.</td>
</tr>
<tr class="odd">
<td></td>
<td>Maximum</td>
<td>Das Maximum für das dumpmaximum umfasst cachemaximum.</td>
</tr>
<tr class="even">
<td></td>
<td>Cacheminimum</td>
<td>Cacheminimum schließt Seiten ein, die in einem latchmodus vorliegen. Cacheminimum schließt Seiten ein, die für den Arbeitsspeicher verwendet werden. Cacheminimum schließt Seiten ein, die mit Fehlern gekennzeichnet sind.</td>
</tr>
<tr class="odd">
<td></td>
<td>Cachemaximum</td>
<td>Cache Maximum umfasst Cache-Minimalwert. Cache Maximum umfasst das gesamte Cache Image.</td>
</tr>
<tr class="even">
<td></td>
<td>Cacheingecludedirtypages</td>
<td>Dump schließt geänderte Seiten ein.</td>
</tr>
<tr class="odd">
<td></td>
<td>Cacheingecludecachedpages</td>
<td>Dump schließt Seiten ein, die gültige Daten enthalten.</td>
</tr>
<tr class="even">
<td></td>
<td>Cacheingecludecorruptedpages</td>
<td>Dump enthält beschädigte Seiten (teuer zu berechnen).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop. Windows7-Namespace](./microsoft.isam.esent.interop.windows7-namespace.md)
