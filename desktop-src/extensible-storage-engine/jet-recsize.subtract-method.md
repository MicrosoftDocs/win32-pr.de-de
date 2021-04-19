---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE. Subtract-Methode'
title: JET_RECSIZE. Subtract-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.subtract(v=EXCHG.10)
ms:contentKeyID: 39514591
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9789dac524e57ea762243ed47d513d262d7ebb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362841"
---
# <a name="jet_recsizesubtract-method"></a>JET_RECSIZE. Subtract-Methode

Berechnen Sie den Unterschied in den Größen zwischen zwei JET_RECSIZE Strukturen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function Subtract ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Subtract(s1, s2)
```

``` csharp
public static JET_RECSIZE Subtract(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a>Parameter

  - s1  
    Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Der erste JET_RECSIZE.

<!-- end list -->

  - s2  
    Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Der zweite JET_RECSIZE.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
Eine JET_RECSIZE, die den Unterschied in den Größen zwischen S1 und S2 enthält.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RECSIZE Struktur](./jet-recsize-structure2.md)

[Mitglieder JET_RECSIZE](./jet-recsize-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
