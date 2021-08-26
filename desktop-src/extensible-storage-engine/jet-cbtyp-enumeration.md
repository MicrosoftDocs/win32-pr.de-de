---
description: 'Weitere Informationen zu: JET_cbtyp-Enumeration'
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
ms.openlocfilehash: 209d3ffe9721f51b8c2d510eecb5408ac66cdbeb58309d1f033e2d23730328ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116230"
---
# <a name="jet_cbtyp-enumeration"></a>JET_cbtyp-Enumeration

Typ des gemeldeten Fortschritts.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Dieser Rückruf ist reserviert und gilt immer als ungültig.</td>
</tr>
<tr class="even">
<td></td>
<td>Abschließen</td>
<td>Eine abschließende Spalte wurde auf 0 (null) festgelegt.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeInsert</td>
<td>Dieser Rückruf erfolgt unmittelbar vor dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen Aufruf von JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterInsert</td>
<td>Dieser Rückruf erfolgt unmittelbar nach dem Einfügen eines neuen Datensatzes in eine Tabelle durch einen Aufruf von JetUpdate, aber bevor JetUpdate zurückgegeben wird.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeReplace</td>
<td>Dieser Rückruf erfolgt unmittelbar bevor ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von JetUpdate geändert wird.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterReplace</td>
<td>Dieser Rückruf erfolgt unmittelbar nachdem ein vorhandener Datensatz in einer Tabelle durch einen Aufruf von JetUpdate geändert wurde, aber bevor JetUpdate zurückgegeben wurde.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Dieser Rückruf erfolgt unmittelbar vor dem Löschen eines vorhandenen Datensatzes in einer Tabelle durch einen Aufruf von JetDelete.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>Dieser Rückruf erfolgt unmittelbar nach dem Löschen eines vorhandenen Datensatzes in einer Tabelle durch einen Aufruf von JetDelete.</td>
</tr>
<tr class="odd">
<td></td>
<td>UserDefinedDefaultValue</td>
<td>Dieser Rückruf tritt auf, wenn die Engine den benutzerdefinierten Standardwert einer Spalte aus der Anwendung abrufen muss. Dieser Rückruf ist im Wesentlichen eine eingeschränkte Implementierung von JetRetrieveColumn, die von der Anwendung ausgewertet wird. Maximal ein Spaltenwert kann für einen benutzerdefinierten Standardwert zurückgegeben werden.</td>
</tr>
<tr class="even">
<td></td>
<td>OnlineDefragCompleted</td>
<td>Dieser Rückruf tritt auf, wenn die Onlinedefragmentierung einer Datenbank, die von JetDefragment initiiert wurde, beendet wurde, weil entweder der Prozess abgeschlossen oder das Zeitlimit erreicht wurde.</td>
</tr>
<tr class="odd">
<td></td>
<td>FreeCursorLS</td>
<td>Dieser Rückruf tritt auf, wenn die Anwendung das Kontexthandle für die lokale Storage bereinigen muss, die einem Cursor zugeordnet ist, der von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter JetSetLS. Der Delegat für diesen Rückrufgrund wird mit JetSetSystemParameter mit JET_paramRuntimeCallback konfiguriert.</td>
</tr>
<tr class="even">
<td></td>
<td>FreeTableLS</td>
<td>Dieser Rückruf tritt auf, weil die Anwendung das Kontexthandle für die lokale Storage bereinigen muss, die einer Tabelle zugeordnet ist, die von der Datenbank-Engine freigegeben wird. Weitere Informationen finden Sie unter JetSetLS. Der Delegat für diesen Rückrufgrund wird mit JetSetSystemParameter mit JET_paramRuntimeCallback konfiguriert.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
