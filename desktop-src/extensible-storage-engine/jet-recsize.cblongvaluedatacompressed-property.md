---
description: 'Weitere Informationen finden Sie unter: JET_RECSIZE. cblongvaluedatacompressed-Eigenschaft.'
title: JET_RECSIZE. cblongvaluedatacompressed-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbLongValueDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cblongvaluedatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbLongValueDataCompressed
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113bb741287e85ef6f7132cd299202a0b9c2af31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393385"
---
# <a name="jet_recsizecblongvaluedatacompressed-property"></a>JET_RECSIZE. cblongvaluedatacompressed (Eigenschaft)

Ruft die komprimierte Größe von Benutzerdaten in der Struktur mit langem Wert ab. Dies entspricht [cblongvaluedata](./jet-recsize.cblongvaluedata-property.md) , wenn keine getrennten langen Werte komprimiert werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbLongValueDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbLongValueDataCompressed
```

``` csharp
public long cbLongValueDataCompressed { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RECSIZE Struktur](./jet-recsize-structure2.md)

[Mitglieder JET_RECSIZE](./jet-recsize-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
