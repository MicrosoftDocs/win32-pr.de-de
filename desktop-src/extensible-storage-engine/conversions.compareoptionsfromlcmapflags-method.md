---
description: 'Weitere Informationen finden Sie unter: Konvertierungen. compareoptionsfromlcmapflags-Methode'
title: Konvertierungen. compareoptionsfromlcmapflags-Methode
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
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214920"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Konvertierungen. compareoptionsfromlcmapflags-Methode

Die angegebenen Flags für lcmapflags werden in Vergleichs Optionen umgewandelt. Unbekannte Optionen werden ignoriert.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - lcmapflags  
    Typ: [System. UInt32](/dotnet/api/system.uint32)  
    
    LCMapString-Flags.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions, die die (bekannten) Flags beschreiben.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Konvertierungs Klasse](./conversions-class.md)

[Konvertierungs Elemente](./conversions-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
