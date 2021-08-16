---
description: 'Weitere Informationen zu: JET_prep-Enumeration'
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
ms.openlocfilehash: 0246114eef784fea2fc145f7cab737c815c17626fc2580b33aa6d09229418066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765054"
---
# <a name="jet_prep-enumeration"></a>JET_prep-Enumeration

Updatetypen für JetPrepareUpdate.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Dieses Flag bewirkt, dass der Cursor sich auf das Einfügen eines neuen Datensatzes vorbereitet. Alle Daten werden mit dem Standardzustand für den Datensatz initialisiert. Wenn die Tabelle über eine Spalte mit automatischer Inkrementierung verfügt, wird diesem Datensatz ein neuer Wert zugewiesen, unabhängig davon, ob das Update letztendlich erfolgreich ist, fehlschlägt oder abgebrochen wird.</td>
</tr>
<tr class="even">
<td></td>
<td>Replace</td>
<td>Dieses Flag bewirkt, dass der Cursor sich auf eine Ersetzung des aktuellen Datensatzes vorbereitet. Wenn die Tabelle über eine Versionsspalte verfügt, wird die Versionsspalte auf den nächsten Wert in ihrer Sequenz festgelegt. Wenn dieses Update nicht abgeschlossen ist, ist der Versionswert im Datensatz nicht betroffen. Es wird eine Updatesperre für den Datensatz eingerichtet, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren, bevor diese Sitzung abgeschlossen wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>Abbrechen</td>
<td>Dieses Flag bewirkt, dass JetPrepareUpdate das Update für diesen Cursor abbricht.</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>Dieses Flag ähnelt JET_prepReplace, aber es wird keine Sperre eingerichtet, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren. Stattdessen erhält diese Sitzung möglicherweise JET_errWriteConflict, wenn Sie JetUpdate aufruft, um das Update abzuschließen.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Dieses Flag bewirkt, dass der Cursor sich auf das Einfügen einer Kopie des vorhandenen Datensatzes vorbereitet. Wenn diese Option verwendet wird, muss ein aktueller Datensatz vorhanden sein. Der Anfangszustand des neuen Datensatzes wird aus dem aktuellen Datensatz kopiert. Lange Werte, die außerhalb des Datensatzes gespeichert werden, werden virtuell kopiert.</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>Dieses Flag bewirkt, dass der Cursor sich auf ein Einfügen desselben Datensatzes und einen Lösch- oder ursprünglichen Datensatz vorbereitet. Sie wird in Fällen verwendet, in denen sich der Primärschlüssel geändert hat.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
