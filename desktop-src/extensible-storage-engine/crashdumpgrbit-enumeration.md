---
description: 'Weitere Informationen zu: CrashDumpGrbit-Enumeration'
title: CrashDumpGrbit-Enumeration (Microsoft.Isam.Esent.Interop.Windows7)
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
ms.openlocfilehash: 6cad58cac50d42b7abaadb179b4068bda2534383113b48430c79d874357c030c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083484"
---
# <a name="crashdumpgrbit-enumeration"></a>CrashDumpGrbit-Enumeration

Optionen für JetConfigureProcessForCrashDump.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Das Mindestabbild enthält CacheMinimum.</td>
</tr>
<tr class="odd">
<td></td>
<td>Maximum</td>
<td>Der maximale Speicherabbildwert schließt CacheMaximum ein.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheMinimum</td>
<td>CacheMinimum enthält Seiten, die latched sind. CacheMinimum enthält Seiten, die für den Arbeitsspeicher verwendet werden. CacheMinimum enthält Seiten, die mit Fehlern gekennzeichnet sind.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheMaximum</td>
<td>Cache maximum includes cache minimum.. (Cachemaximum schließt den Cachemindestwert ein. Das Cachemaximum schließt das gesamte Cacheimage ein.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeDirtyPages</td>
<td>Dump enthält Seiten, die geändert werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheIncludeCachedPages</td>
<td>Dump enthält Seiten, die gültige Daten enthalten.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeCorruptedPages</td>
<td>Dump enthält Seiten, die beschädigt sind (teuer zu berechnen).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop.Windows7-Namespace](./microsoft.isam.esent.interop.windows7-namespace.md)
