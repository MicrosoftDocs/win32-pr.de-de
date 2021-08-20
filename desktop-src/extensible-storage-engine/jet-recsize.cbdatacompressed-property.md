---
description: 'Weitere Informationen finden Sie unter: JET_RECSIZE.cbDataCompressed-Eigenschaft'
title: JET_RECSIZE.cbDataCompressed -Eigenschaft (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cbDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cbdatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515358
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbDataCompressed
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 469ddbd32965e551923b50f63662eb34835837d416eaa534d02af416d6c3c5f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117893351"
---
# <a name="jet_recsizecbdatacompressed-property"></a>JET_RECSIZE.cbDataCompressed-Eigenschaft

Ruft die komprimierte Größe der Benutzerdaten im Datensatz ab. Dies ist identisch mit [cbData,](./jet-recsize.cbdata-property.md) wenn keine systeminternen Long-Werte komprimiert sind.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbDataCompressed
```

``` csharp
public long cbDataCompressed { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_RECSIZE-Struktur](./jet-recsize-structure2.md)

[JET_RECSIZE Mitglieder](./jet-recsize-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
