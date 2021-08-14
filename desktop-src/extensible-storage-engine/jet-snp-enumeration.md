---
description: 'Weitere Informationen zu: JET_SNP-Enumeration'
title: JET_SNP-Enumeration
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a18858b7dba79c8e8d0d2a6ab51783ab0a602d595214895f1798b2ef0e084731
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979261"
---
# <a name="jet_snp-enumeration"></a>JET_SNP-Enumeration

Der Typ des Vorgangs, für den der Fortschritt gemeldet wird.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
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
<td>Reparieren</td>
<td>Rückruf ist für eine Reparaturoption vorgesehen.</td>
</tr>
<tr class="even">
<td></td>
<td>Kompakt</td>
<td>Der Rückruf ist für die Datenbankdefragmentierung vorgesehen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Restore</td>
<td>Der Rückruf ist für Wiederherstellungsoptionen vorgesehen.</td>
</tr>
<tr class="even">
<td></td>
<td>Backup</td>
<td>Der Rückruf ist für Sicherungsoptionen vorgesehen.</td>
</tr>
<tr class="odd">
<td></td>
<td>schrubben</td>
<td>Der Rückruf dient zum Nullen der Datenbank.</td>
</tr>
<tr class="even">
<td></td>
<td>UpgradeRecordFormat</td>
<td>Der Rückruf dient zum Aktualisieren des Datensatzformats aller Datenbankseiten.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
