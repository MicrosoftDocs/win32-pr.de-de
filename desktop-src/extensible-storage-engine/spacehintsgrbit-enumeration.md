---
description: Weitere Informationen finden Sie in der spacehintsgrbit-Enumeration.
title: Spacehintsgrbit-Enumeration
TOCTitle: SpaceHintsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.spacehintsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintHotpointSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintAppendSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.DeleteHintTableSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.None
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve2
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve1
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanForward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanBackward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve3
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.SpaceHintUtilizeParentSpace
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve3
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintHotpointSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintAppendSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanBackward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.SpaceHintUtilizeParentSpace
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve2
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.DeleteHintTableSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanForward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.None
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffc78aab444c73f7ff0eae7ff0eaa84e134ee9bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959053"
---
# <a name="spacehintsgrbit-enumeration"></a>Spacehintsgrbit-Enumeration

Optionen für [JET_SPACEHINTS](./jet-spacehints-class.md).

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SpaceHintsGrbit
'Usage
Dim instance As SpaceHintsGrbit
```

``` csharp
[FlagsAttribute]
public enum SpaceHintsGrbit
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
<td>Spacehintutilizeparameespace</td>
<td>Dadurch wird die interne Zuordnungs Richtlinie geändert, um Speicherplatz hierarchisch aus dem unmittelbar übergeordneten Element einer B-Struktur zu erhalten.</td>
</tr>
<tr class="odd">
<td></td>
<td>"Kreatehintappendsequential"</td>
<td>Dieses Bit ermöglicht das Anfügen von Split-Verhalten entsprechend der Wachstumsdynamik der Tabelle (festgelegt durch cbminblock, ulgrowth, cbmaxblock).</td>
</tr>
<tr class="even">
<td></td>
<td>"Kreatehinthotpointsequential"</td>
<td>Dieses Bit ermöglicht das Anwachsen des hotpointverhaltens entsprechend der Wachstumsdynamik der Tabelle (festgelegt durch cbminblock, ulgrowth, cbmaxblock).</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintReserve1</td>
<td>Reserviert und ignoriert.</td>
</tr>
<tr class="even">
<td></td>
<td>"Retrievehinttablescanforward"</td>
<td>Durch Festlegen dieser Option gibt der Client an, dass die Forward-sequenzielle Überprüfung das vorherrschende Verwendungs Muster dieser Tabelle ist.</td>
</tr>
<tr class="odd">
<td></td>
<td>Retrievehinttablescanabwärts</td>
<td>Durch Festlegen dieser Option gibt der Client an, dass ein rückwärts sequenzieller Scan das vorherrschende Verwendungs Muster dieser Tabelle ist.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveHintReserve2</td>
<td>Reserviert und ignoriert.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintReserve3</td>
<td>Reserviert und ignoriert.</td>
</tr>
<tr class="even">
<td></td>
<td>Deletehinttablesequential</td>
<td>Die Anwendung erwartet, dass diese Tabelle sequenziell (vom niedrigsten zum höchsten Schlüssel) bereinigt wird.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
