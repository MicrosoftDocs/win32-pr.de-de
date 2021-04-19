---
description: Weitere Informationen finden Sie in der opentablegrbit-Enumeration.
title: Opentablegrbit-Enumeration
TOCTitle: OpenTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opentablegrbit(v=EXCHG.10)
ms:contentKeyID: 39510721
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfb2d75fc17e37dc669acf1fd84f38c957d467f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349888"
---
# <a name="opentablegrbit-enumeration"></a>Opentablegrbit-Enumeration

Optionen für jetopentable.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenTableGrbit
'Usage
Dim instance As OpenTableGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenTableGrbit
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
<td>Denyschreiben</td>
<td>Diese Tabelle kann nicht für den Schreibzugriff durch eine andere Sitzung geöffnet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Denyread</td>
<td>Diese Tabelle kann nicht für den Lesezugriff durch eine andere Sitzung geöffnet werden.</td>
</tr>
<tr class="even">
<td></td>
<td>ReadOnly</td>
<td>Fordern Sie schreibgeschützten Zugriff auf die Tabelle an.</td>
</tr>
<tr class="odd">
<td></td>
<td>Aktualisierbar</td>
<td>Fordern Sie Schreibzugriff auf die Tabelle an.</td>
</tr>
<tr class="even">
<td></td>
<td>Permitddl</td>
<td>Lässt DDL-Änderungen an einer Tabelle zu, die als fixedddl gekennzeichnet ist. Diese Option muss mit denyread verwendet werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>NoCache</td>
<td>Seiten für diese Tabelle nicht zwischenspeichern.</td>
</tr>
<tr class="even">
<td></td>
<td>Preread</td>
<td>Gibt einen Hinweis an, dass sich die Tabelle wahrscheinlich nicht im Puffer Cache befindet, und dass das vorab lesen für die Leistung von Vorteil sein kann.</td>
</tr>
<tr class="odd">
<td></td>
<td>Sequenziell</td>
<td>Angenommen, ein sequenzielles Zugriffsmuster und Datenbankseiten werden vorab abgerufen.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass1</td>
<td>Die Tabelle gehört zur Statistik Klasse 1.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass2</td>
<td>Die Tabelle gehört zu der stats-Klasse 2.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass3</td>
<td>Die Tabelle gehört zu den stats-Klassen 3.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass4</td>
<td>Die Tabelle gehört zu den Statistik Klassen 4.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass5</td>
<td>Die Tabelle gehört zur Statistik Klasse 5.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass6</td>
<td>Die Tabelle gehört zur Statistik Klasse 6.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass7</td>
<td>Die Tabelle gehört zu den Statistik Klassen 7.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass8</td>
<td>Die Tabelle gehört zu den Statistik Klassen 8.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass9</td>
<td>Die Tabelle gehört zu den Statistik Klassen 9.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass10</td>
<td>Die Tabelle gehört zu den Statistik Klassen 10.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass11</td>
<td>Die Tabelle gehört zur Statistik Klasse 11.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass12</td>
<td>Die Tabelle gehört zur Statistik Klasse 12.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass13</td>
<td>Die Tabelle gehört zur Statistik Klasse 13.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass14</td>
<td>Die Tabelle gehört zur Statistik Klasse 14.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass15</td>
<td>Die Tabelle gehört zu den Statistik Klassen 15.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
