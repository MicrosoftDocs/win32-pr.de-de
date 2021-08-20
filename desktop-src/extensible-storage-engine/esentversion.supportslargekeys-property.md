---
description: 'Weitere Informationen finden Sie unter: EsentVersion.SupportsLargeKeys(Eigenschaft)'
title: EsentVersion.SupportsLargeKeys (Eigenschaft)
TOCTitle: 'SupportsLargeKeys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion.supportslargekeys(v=EXCHG.10)
ms:contentKeyID: 55103180
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
- Microsoft.Isam.Esent.Interop.EsentVersion.get_SupportsLargeKeys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 19eb0afe6cdf1cc4dcdbc2f29706001b037fb5b9f3560c68f54e93186673111c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117706556"
---
# <a name="esentversionsupportslargekeys-property"></a>EsentVersion.SupportsLargeKeys (Eigenschaft)

Ruft einen Wert ab, der angibt, ob große Schlüssel \> (255 Byte) unterstützt werden. Die Schlüsselgröße für einen Index kann im -Objekt JET_INDEXCREATE [werden.](./jet-indexcreate-class.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared ReadOnly Property SupportsLargeKeys As Boolean
    Get
'Usage
Dim value As Boolean

value = EsentVersion.SupportsLargeKeys
```

``` csharp
public static bool SupportsLargeKeys { get; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentVersion-Klasse](./esentversion-class.md)

[EsentVersion-Member](./esentversion-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
