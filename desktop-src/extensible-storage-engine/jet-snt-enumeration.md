---
description: 'Weitere Informationen zu: JET_SNT-Enumeration'
title: JET_SNT-Enumeration
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d25137c9e976d05bd065837fed7753e26e3afdae020499b3388948e11733fd77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252524"
---
# <a name="jet_snt-enumeration"></a>JET_SNT-Enumeration

Typ des gemeldeten Fortschritts.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a>Member

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>Starten</td>
<td>Rückruf für den Anfang eines Vorgangs.</td>
</tr>
<tr class="even">
<td></td>
<td>Fortschritt</td>
<td>Rückruf für den Vorgangsfortschritt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Abgeschlossen</td>
<td>Rückruf für den Abschluss eines Vorgangs.</td>
</tr>
<tr class="even">
<td></td>
<td>Fehler</td>
<td>Rückruf für Fehler während des Vorgangs.</td>
</tr>
<tr class="odd">
<td></td>
<td>RecoveryStep</td>
<td>Rückruf für die Wiederherstellungssteuerung.
<p>Wird für die interne Verarbeitung in Versionen des Windows Betriebssystems vor Windows 8 verwendet. Dieser Wert gilt nicht für Versionen von Windows, die mit Windows 8 beginnen.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
