---
description: 'Weitere Informationen finden Sie hier: compactgrbit-Enumeration'
title: Compactgrbit-Enumeration
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350505"
---
# <a name="compactgrbit-enumeration"></a>Compactgrbit-Enumeration

Optionen für [jetcompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, compactgrbit)](./api.jetcompact-method.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>Stats</td>
<td>Bewirkt, dass jetcompact Statistiken für die Quelldatenbank in einer Datei namens DFRGINFO.TXT abgibt. Die Statistik enthält den Namen der einzelnen Tabellen in der Quelldatenbank, die Anzahl der Zeilen in jeder Tabelle, die Gesamtgröße aller Zeilen in jeder Tabelle, die Gesamtgröße in Bytes aller Spalten vom Typ <a href="hh577895(v=exchg.10).md">LONGTEXT</a> oder <a href="hh577895(v=exchg.10).md">LONGBINARY</a> , die groß genug sind, um getrennt vom Datensatz, die Anzahl der Blattseiten des gruppierten Indexes und die Anzahl der Blattseiten für lange Werte gespeichert zu werden. Außerdem werden zusammenfassende Statistiken einschließlich der Größe der Quelldatenbank, der Zieldatenbank, der für die Daten Bank Komprimierung benötigten Zeit und des temporären Daten Bank Speicherplatzes ebenfalls ebenfalls gekippt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Reparieren</td>
<td><strong>Veraltet.</strong> Wird verwendet, wenn die Quelldatenbank bekanntermaßen beschädigt ist. Sie ermöglicht eine ganze Reihe neuer Verhalten, die so viele Daten wie möglich aus der Quelldatenbank retten sollen. Jetcompact mit diesem Options Satz kann <a href="hh564840(v=exchg.10).md">Erfolg</a> zurückgeben, aber nicht alle in der Quelldatenbank erstellten Daten kopieren. Daten, die sich in beschädigten Teilen der Quelldatenbank befanden, werden übersprungen.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
