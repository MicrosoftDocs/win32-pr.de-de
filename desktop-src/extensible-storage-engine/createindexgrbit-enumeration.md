---
description: Weitere Informationen finden Sie in der "kreateingedexgrbit"-Enumeration.
title: Aufzählung von "kreateingedexgrbit"
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352354"
---
# <a name="createindexgrbit-enumeration"></a>Aufzählung von "kreateingedexgrbit"

Optionen für jetkreateingedex.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
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
<td>Indexunique</td>
<td>Doppelte Indexeinträge (Schlüssel) sind nicht zulässig. Dies wird erzwungen, wenn jetupdate aufgerufen wird, nicht wenn jetsetcolumn aufgerufen wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>Indexprimary</td>
<td>Der Index ist ein primärer Index (gruppierter Index). Jede Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index explizit für eine Tabelle definiert wird, erstellt die Datenbank-Engine ihren eigenen primären Index.</td>
</tr>
<tr class="even">
<td></td>
<td>Indexdisallownull</td>
<td>Keine der Spalten, für die der Index erstellt wird, kann einen NULL-Wert enthalten.</td>
</tr>
<tr class="odd">
<td></td>
<td>Index-gnorumull</td>
<td>Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn alle indizierten Spalten NULL sind.</td>
</tr>
<tr class="even">
<td></td>
<td>Index gnoreanynull</td>
<td>Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn eine der indizierten Spalten NULL ist.</td>
</tr>
<tr class="odd">
<td></td>
<td>Index gnorefirstnull</td>
<td>Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn die erste indizierte Spalte NULL ist.</td>
</tr>
<tr class="even">
<td></td>
<td>Indexlazyflush</td>
<td>Gibt an, dass die Index Vorgänge verzögert protokolliert werden. JET_bitIndexLazyFlush wirkt sich nicht auf die Faulheit von Datenaktualisierungen aus. Wenn die Indizierungs Vorgänge durch die Beendigung des Prozesses unterbrochen werden, kann die Wiederherstellung der Datenbank weiterhin in einen konsistenten Zustand versetzt werden, aber der Index ist möglicherweise nicht vorhanden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Indexempty</td>
<td>Versuchen Sie nicht, den Index zu erstellen, da alle Einträge zu NULL ausgewertet werden. bei der Übergabe JET_bitIndexEmpty muss auch grbit JET_bitIgnoreAnyNull angegeben werden. Dies ist eine Leistungsverbesserung. Wenn z. b. eine neue Spalte zu einer Tabelle hinzugefügt wird, dann wird ein Index für diese neu hinzugefügte Spalte erstellt, dann werden alle Datensätze in der Tabelle gescannt, auch wenn Sie niemals dem Index hinzugefügt würden. Durch angeben JET_bitIndexEmpty wird die Überprüfung der Tabelle ausgelassen, was möglicherweise sehr lange dauern kann.</td>
</tr>
<tr class="even">
<td></td>
<td>Indexunversionierung</td>
<td>Bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist. Normalerweise kann eine Sitzung in einer Transaktion in keiner anderen Sitzung einen Index Erstellungs Vorgang sehen. Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt, sodass die zweite Indexerstellung einfach fehlschlägt, anstatt potenziell viele unnötige Daten Bank Vorgänge zu verursachen. Die zweite Transaktion ist möglicherweise nicht in der Lage, den Index sofort zu verwenden. Der Index Erstellungs Vorgang muss durchgeführt werden, bevor er verwendet werden kann. Die Sitzung darf sich zurzeit nicht in einer Transaktion befinden, um einen Index ohne Versionsinformationen zu erstellen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Indexsortnullshigh</td>
<td>Die Angabe dieses Flags bewirkt, dass NULL-Werte nach den Daten für alle Spalten im Index sortiert werden.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
