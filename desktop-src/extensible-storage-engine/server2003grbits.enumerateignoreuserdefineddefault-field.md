---
description: 'Weitere Informationen finden Sie unter: Feld "Server2003Grbits.EnumerateIgnoreUserDefinedDefault"'
title: Server2003Grbits.EnumerateIgnoreUserDefinedDefault-Feld (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b3c110e1aeb54d38805b5ee6ad116ed8fcbbdc7274d0548b582fd88b0e8ac1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978560"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a>Server2003Grbits.EnumerateIgnoreUserDefinedDefault-Feld

Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben. Diese Option verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Aufzählen der Werte für diese Spalte aufgerufen wird.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a>Hinweise

Diese Option ist nur für Windows Server 2003 SP1 und höher verfügbar.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Server2003Grbits-Klasse](./server2003grbits-class.md)

[Server2003Grbits-Member](./server2003grbits-members.md)

[Microsoft.Isam.Esent.Interop.Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
