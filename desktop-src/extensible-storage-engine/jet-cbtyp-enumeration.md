---
description: 'Weitere Informationen finden Sie hier: JET_cbtyp-Enumeration'
title: JET_cbtyp-Enumeration
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356822"
---
# <a name="jet_cbtyp-enumeration"></a>JET_cbtyp-Enumeration

Der Typ des Status, der gemeldet wird.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
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
<td>Null</td>
<td>Dieser Rückruf ist reserviert und wird immer als ungültig angesehen.</td>
</tr>
<tr class="even">
<td></td>
<td>Abschließen</td>
<td>Eine finalisierbare Spalte ist auf 0 (null) übergegangen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Beforeingesert</td>
<td>Dieser Rückruf tritt direkt vor dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen jetupdate-Rückruf auf.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterInsert</td>
<td>Dieser Rückruf tritt unmittelbar nach dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen jetupdate-Rückruf auf, aber bevor jetupdate zurückgegeben wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>Beforereplace</td>
<td>Dieser Rückruf tritt direkt vor einem vorhandenen Datensatz in einer Tabelle auf, die durch einen jetupdate-Rückruf geändert wird.</td>
</tr>
<tr class="even">
<td></td>
<td>After replace</td>
<td>Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen jetupdate-Rückruf geändert wurde, jedoch bevor jetupdate zurückgegeben wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Dieser Rückruf tritt auf, kurz bevor ein vorhandener Datensatz in einer Tabelle durch einen jetdelete-Rückruf gelöscht wird.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>Dieser Rückruf tritt auf, wenn ein vorhandener Datensatz in einer Tabelle durch einen-Befehl von jetdelete gelöscht wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>Userdefineddefaultvalue</td>
<td>Dieser Rückruf tritt auf, wenn die Engine den benutzerdefinierten Standardwert einer Spalte aus der Anwendung abrufen muss. Bei diesem Rückruf handelt es sich im Wesentlichen um eine eingeschränkte Implementierung von jetretrievecolumgen, die von der Anwendung ausgewertet wird. Für einen benutzerdefinierten Standardwert können maximal ein Spaltenwert zurückgegeben werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Onlinedefragabgeschlossen</td>
<td>Dieser Rückruf tritt auf, wenn die Online Defragmentierung einer Datenbank, die von jetdefragment initiiert wurde, beendet wurde, weil entweder der Prozess abgeschlossen oder das Zeitlimit erreicht wurde.</td>
</tr>
<tr class="odd">
<td></td>
<td>Freecursorls</td>
<td>Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einem Cursor zugeordnet ist, der von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter jetsetls. Der Delegat für diesen Rückruf Grund wird mithilfe von jetsetsystemparameter mit JET_paramRuntimeCallback konfiguriert.</td>
</tr>
<tr class="even">
<td></td>
<td>Freetablels</td>
<td>Dieser Rückruf tritt auf, wenn die Anwendung das Kontext Handle für den lokalen Speicher bereinigen muss, der einer Tabelle zugeordnet ist, die von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter jetsetls. Der Delegat für diesen Rückruf Grund wird mithilfe von jetsetsystemparameter mit JET_paramRuntimeCallback konfiguriert.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
