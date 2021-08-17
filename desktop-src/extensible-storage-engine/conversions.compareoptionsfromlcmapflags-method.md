---
description: 'Weitere Informationen finden Sie unter: Conversions.CompareOptionsFromLCMapFlags-Methode'
title: Conversions.CompareOptionsFromLCMapFlags-Methode
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfe3a65c52d23ee335a81560775f0063b8ca81a10cc43c1787e353a5b803eed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117901846"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Conversions.CompareOptionsFromLCMapFlags-Methode

Geben Sie Flags für LCMapFlags an, und machen Sie sie in Vergleichsoptionen. Unbekannte Optionen werden ignoriert.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a>Parameter

  - lcmapFlags  
    Typ: [System.UInt32](/dotnet/api/system.uint32)  
    
    LCMapString-Flags.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions, die die (bekannten) Flags beschreiben.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Conversions-Klasse](./conversions-class.md)

[Konvertierungsmitglieder](./conversions-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
