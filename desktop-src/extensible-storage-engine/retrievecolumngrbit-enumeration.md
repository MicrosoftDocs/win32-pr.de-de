---
description: 'Weitere Informationen finden Sie hier: retrievecolumngrbit-Enumeration'
title: Retrievecolumngrbit-Enumeration
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
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349452"
---
# <a name="retrievecolumngrbit-enumeration"></a>Retrievecolumngrbit-Enumeration

Optionen für jetretrievecolumgen.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Retrievecopy</td>
<td>Dieses Flag bewirkt, dass die Spalte "abrufen" den geänderten Wert anstelle des ursprünglichen Werts abruft. Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen. Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes abgerufen werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>"Retrievefromindex"</td>
<td>Diese Option wird verwendet, um nach Möglichkeit Spaltenwerte aus dem Index abzurufen, ohne auf den Datensatz zuzugreifen. Auf diese Weise kann das unnötige Laden von Datensätzen vermieden werden, wenn benötigte Daten aus Indexeinträgen selbst verfügbar sind.</td>
</tr>
<tr class="even">
<td></td>
<td>Retrievefromprimarybookmark</td>
<td>Diese Option wird zum Abrufen von Spaltenwerten aus dem Index-Lesezeichen verwendet und unterscheidet sich möglicherweise vom Indexwert, wenn eine Spalte sowohl im primären Index als auch im aktuellen Index angezeigt wird. Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index oder der primäre Index ist. Dieses Bit kann nicht festgelegt werden, wenn "retrievefromindex" ebenfalls festgelegt ist.</td>
</tr>
<tr class="odd">
<td></td>
<td>Retrievetag</td>
<td>Diese Option wird verwendet, um die Sequenznummer eines mehrwertigen Spaltenwerts in JET_RETINFO. itagsequence abzurufen. Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf ausgeführt werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Abrufen von evenull</td>
<td>Diese Option wird verwendet, um NULL-Werte für mehrwertige Spalten abzurufen. Wenn diese Option nicht angegeben ist, werden NULL-Werte für mehrwertige Spalten automatisch übersprungen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Retrieveignoredefault</td>
<td>Diese Option wirkt sich nur auf mehrwertige Spalten aus und bewirkt, dass ein NULL-Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und für die Spalte im Datensatz keine Werte festgelegt sind.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
