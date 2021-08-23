---
description: 'Weitere Informationen zu: Feld "Server2003Grbits.ForwardOnly"'
title: Feld "Server2003Grbits.ForwardOnly" (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f98dca3e85eb5ad3c57ef1203971078035c7191ca3e5358dba701dcd870f8480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603840"
---
# <a name="server2003grbitsforwardonly-field"></a>Feld "Server2003Grbits.ForwardOnly"

Diese Option fordert an, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für Zwischenabfrageergebnisse optimierte Implementierung verwenden kann. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl. Ein Nebeneffekt dieser Option besteht darin, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthalten kann. Weitere Informationen finden Sie unter [Eindeutig.](./temptablegrbit-enumeration.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Server2003Grbits-Klasse](./server2003grbits-class.md)

[Server2003Grbits-Member](./server2003grbits-members.md)

[Microsoft.Isam.Esent.Interop.Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
