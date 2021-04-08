---
description: 'Weitere Informationen über: indexInfo. indexsegments-Eigenschaft'
title: IndexInfo. indexsegments (Eigenschaft)
TOCTitle: 'IndexSegments property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.indexsegments(v=EXCHG.10)
ms:contentKeyID: 55103239
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
- Microsoft.Isam.Esent.Interop.IndexInfo.get_IndexSegments
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d366d3ddd5ba7a33faeb44459830dbaadcc221e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753352"
---
# <a name="indexinfoindexsegments-property"></a>IndexInfo. indexsegments (Eigenschaft)

Ruft die Segmente des Indexes ab.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property IndexSegments As IList(Of IndexSegment)
    Get
'Usage
Dim instance As IndexInfo
Dim value As IList(Of IndexSegment)

value = instance.IndexSegments
```

``` csharp
public IList<IndexSegment> IndexSegments { get; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[IndexSegment](./indexsegment-class.md)\>  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[IndexInfo-Klasse](./indexinfo-class.md)

[IndexInfo-Member](./indexinfo-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
