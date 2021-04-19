---
description: Weitere Informationen finden Sie in der temptablegrbit-Enumeration.
title: Temptablegrbit-Enumeration
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372811"
---
# <a name="temptablegrbit-enumeration"></a>Temptablegrbit-Enumeration

Optionen für die Erstellung temporärer Tabellen.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
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
<td>Zierenden</td>
<td>Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von JetSeek für die Suche nach Datensätzen nach Index Schlüssel zuzulassen. Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Eindeutig</td>
<td>Mit dieser Option wird angefordert, dass Datensätze mit doppelten Index Schlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden. Vor Windows Server 2003 hat die Datenbank-Engine immer angenommen, dass diese Option wirksam ist, weil alle gruppierten Indizes auch ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die Option <a href="dn351284(v=exchg.10).md">ForwardOnly</a> ebenfalls angegeben ist. Es ist nicht möglich zu wissen, welches Duplikat gewinnt und welche Duplikate im allgemeinen verworfen werden. Wenn jedoch die errorondupli-sertion-Option angefordert wird, gewinnt der erste Datensatz mit einem bestimmten Index Schlüssel, der in die temporäre Tabelle eingefügt werden soll.</td>
</tr>
<tr class="even">
<td></td>
<td>Aktualisierbar</td>
<td>Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, damit Datensätze, die zuvor eingefügt wurden, geändert werden können. Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Bildlauffähigkeit</td>
<td>Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="dn292217(v=exchg.10).md">jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)</a>zu ermöglichen. Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</td>
</tr>
<tr class="even">
<td></td>
<td>Sortnullshigh</td>
<td>Mit dieser Option wird angefordert, dass NULL-Schlüssel Spaltenwerte näher am Ende des Indexes liegen als Schlüssel Spaltenwerte ungleich NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>Forcematerialisierung</td>
<td>Diese Option zwingt den temporären Tabellen-Manager dazu, einen Versuch zu verwerfen, eine clever-Strategie zum Verwalten der temporären Tabelle zu wählen, die zu einer verbesserten Leistung führt.</td>
</tr>
<tr class="even">
<td></td>
<td>Erroronduplialisieinsertion</td>
<td>Mit dieser Option wird angefordert, dass jeder Versuch, einen Datensatz mit demselben Index Schlüssel wie ein zuvor eingefügter Datensatz einzufügen, sofort mit <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>fehlschlägt. Wenn diese Option nicht angefordert wird, wird möglicherweise sofort ein Duplikat erkannt, oder es kann zu einem späteren Zeitpunkt in Abhängigkeit von der Strategie, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt wurde, ein Fehler auftreten. Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[Nur Weiterleitung](./server2003grbits.forwardonly-field.md)

[Intrinsies clvsonly](./windows7grbits.intrinsiclvsonly-field.md)
