---
description: 'Weitere Informationen finden Sie unter: esentversion. supportslargekeys-Eigenschaft'
title: Esentversion. supportslargekeys-Eigenschaft
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
ms.openlocfilehash: 43ee88b7c0e190d9c717c087deeb5fc4556e6575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363836"
---
# <a name="esentversionsupportslargekeys-property"></a>Esentversion. supportslargekeys-Eigenschaft

Ruft einen Wert ab, der angibt, ob große ( \> 255 Byte) Schlüssel unterstützt werden. Die Schlüsselgröße für einen Index kann im [JET_INDEXCREATE](./jet-indexcreate-class.md) Objekt angegeben werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentversion-Klasse](./esentversion-class.md)

[Esentversion-Member](./esentversion-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
