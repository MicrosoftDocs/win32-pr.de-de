---
description: 'Weitere Informationen finden Sie unter: Konvertierungen. lcmapflagsfromcompareoptions-Methode'
title: Konvertierungen. lcmapflagsfromcompareoptions-Methode
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350503"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a>Konvertierungen. lcmapflagsfromcompareoptions-Methode

Legen Sie CompareOptions fest, und wandeln Sie Sie aus LCMapString in Flags um. Unbekannte Optionen werden ignoriert.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a>Parameter

  - compareOptions  
    Typ: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
    
    Die Optionen, die konvertiert werden sollen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. UInt32](/dotnet/api/system.uint32)  
Die LCMapString-Flags, die den Vergleichs Optionen entsprechen. Nicht unterstützte Optionen werden ignoriert.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Konvertierungs Klasse](./conversions-class.md)

[Konvertierungs Elemente](./conversions-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
