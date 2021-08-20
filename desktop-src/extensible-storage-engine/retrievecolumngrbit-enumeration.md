---
description: Weitere Informationen finden Sie unter RetrieveColumnGrbit-Enumeration.
title: RetrieveColumnGrbit-Enumeration
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bd59f610b2ff1423b82539c61eff3d9d770a03d6f8291a1bae53b372fff318f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890668"
---
# <a name="retrievecolumngrbit-enumeration"></a>RetrieveColumnGrbit-Enumeration

Optionen für JetRetrieveColumn.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
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
<td>RetrieveCopy</td>
<td>Dieses Flag bewirkt, dass die Abrufspalte den geänderten Wert anstelle des ursprünglichen Werts abruft. Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen. Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, während des Einfügens oder Aktualisierens eines Datensatzes abgerufen werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveFromIndex</td>
<td>Diese Option wird verwendet, um Spaltenwerte möglichst ohne Zugriff auf den Datensatz aus dem Index abzurufen. Auf diese Weise kann unnötiges Laden von Datensätzen vermieden werden, wenn die benötigten Daten über Indexeinträge selbst verfügbar sind.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveFromPrimaryBookmark</td>
<td>Diese Option wird verwendet, um Spaltenwerte aus dem Index-Lesezeichen abzurufen, und kann sich vom Indexwert unterscheiden, wenn eine Spalte sowohl im primären als auch im aktuellen Index angezeigt wird. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte oder primäre Index ist. Dieses Bit kann nicht festgelegt werden, wenn retrieveFromIndex ebenfalls festgelegt ist.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveTag</td>
<td>Diese Option wird verwendet, um die Sequenznummer eines mehrwertigen Spaltenwerts in JET_RETINFO.itagSequence abzurufen. Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf erfolgen.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveNull</td>
<td>Diese Option wird verwendet, um wertewertige Spalten-NULL-Werte abzurufen. Wenn diese Option nicht angegeben wird, werden die NULL-Werte der mehrwertigen Spalte automatisch übersprungen.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveIgnoreDefault</td>
<td>Diese Option wirkt sich nur auf mehrwertige Spalten aus und bewirkt, dass ein NULL-Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und keine festgelegten Werte für die Spalte im Datensatz enthalten sind.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
