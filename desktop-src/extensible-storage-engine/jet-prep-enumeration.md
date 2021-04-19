---
description: 'Weitere Informationen finden Sie hier: JET_prep-Enumeration'
title: JET_prep-Enumeration
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368964"
---
# <a name="jet_prep-enumeration"></a>JET_prep-Enumeration

Update Typen für jetprepareupdate.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
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
<td>Einfügen</td>
<td>Dieses Flag bewirkt, dass der Cursor eine Einfügung eines neuen Datensatzes vorbereitet. Alle Daten werden auf den Standardstatus für den Datensatz initialisiert. Wenn die Tabelle eine automatische Inkrement-Spalte aufweist, wird diesem Datensatz ein neuer Wert zugewiesen, unabhängig davon, ob das Update letztendlich erfolgreich ist, fehlschlägt oder abgebrochen wird.</td>
</tr>
<tr class="even">
<td></td>
<td>Replace</td>
<td>Dieses Flag bewirkt, dass der Cursor eine Ersetzung des aktuellen Datensatzes vorbereitet. Wenn die Tabelle eine Versions Spalte aufweist, wird die Versions Spalte auf den nächsten Wert in der zugehörigen Reihenfolge festgelegt. Wenn dieses Update nicht vollständig ausgeführt wird, ist der Versions Wert im Datensatz nicht betroffen. Es wird eine Update Sperre für den Datensatz erstellt, um zu verhindern, dass dieser Datensatz von anderen Sitzungen aktualisiert wird, bevor diese Sitzung abgeschlossen ist.</td>
</tr>
<tr class="odd">
<td></td>
<td>Abbrechen</td>
<td>Dieses Flag bewirkt, dass jetprepareupdate das Update für diesen Cursor abbricht.</td>
</tr>
<tr class="even">
<td></td>
<td>Replacumolock</td>
<td>Dieses Flag ähnelt JET_prepReplace, es wird jedoch keine Sperre erstellt, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren. Stattdessen erhält diese Sitzung möglicherweise JET_errWriteConflict, wenn jetupdate aufgerufen wird, um das Update abzuschließen.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Dieses Flag bewirkt, dass der Cursor eine Einfügung einer Kopie des vorhandenen Datensatzes vorbereitet. Wenn diese Option verwendet wird, muss ein aktueller Datensatz vorhanden sein. Der ursprüngliche Zustand des neuen Datensatzes wird aus dem aktuellen Datensatz kopiert. Lange Werte, die außerhalb des Datensatzes gespeichert werden, werden virtuell kopiert.</td>
</tr>
<tr class="even">
<td></td>
<td>Insertcopydeleteoriginal</td>
<td>Dieses Flag bewirkt, dass der Cursor eine Einfügung desselben Datensatzes und einen Löschvorgang oder den ursprünglichen Datensatz vorbereitet. Sie wird in Fällen verwendet, in denen sich der Primärschlüssel geändert hat.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
