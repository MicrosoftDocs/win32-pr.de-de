---
description: 'Weitere Informationen zu: LegacyFileNames-Enumeration'
title: LegacyFileNames-Enumeration (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: LegacyFileNames enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104275
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8265724c8f69cc9b8e90e6f2d7c777940aa1251ac99f436b9976e2a3c13f03fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614570"
---
# <a name="legacyfilenames-enumeration"></a>LegacyFileNames-Enumeration

Optionen für LegacyFileNames

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Enumeration LegacyFileNames
'Usage
Dim instance As LegacyFileNames
```

``` csharp
public enum LegacyFileNames
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
<td>ESE98FileNames</td>
<td>Wenn diese Option vorhanden ist, verwendet die Datenbank-Engine die folgenden Namenskonventionen für ihre Dateien: o Transaktionsprotokolldateien verwenden . LOG für die Dateierweiterung o Prüfpunktdateien verwendet . CHK für die Dateierweiterung</td>
</tr>
<tr class="even">
<td></td>
<td>EightDotThreeSoftCompat</td>
<td>Behalten Sie die Namenssyntax 8.3 so lange wie möglich bei. (Dies sollte nicht geändert werden, ohne sicherzustellen, dass keine Protokolldateien vorhanden sind.)</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
