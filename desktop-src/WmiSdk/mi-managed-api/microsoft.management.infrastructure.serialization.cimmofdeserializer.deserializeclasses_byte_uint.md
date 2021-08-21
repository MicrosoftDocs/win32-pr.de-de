---
description: 'Weitere Informationen finden Sie unter: CimMofDeserializer.DeserializeClasses-Methode (Byte[], UInt32)'
title: CimMofDeserializer.DeserializeClasses-Methode (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@)
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: b05a1eca97c650b130170af2c6c03a958b6022017902e39f15156b08038bad08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317411"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a>CimMofDeserializer.DeserializeClasses-Methode (Byte, \[ \] UInt32)

Deserialisiert CIM-Klassen basierend auf serialisierten Daten.

**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntax

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a>Parameter

  - serializedData  
    Typ: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Ein Puffer, der die serialisierten Daten enthält.

<!-- end list -->

  - offset  
    Typ: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Der Byteoffset zu der Position, an der mit dem Lesen der Daten begonnen werden soll. Wenn die Methode zurückgegeben wird, wird der Offset auf das nächste Byte nach den deserialisierten Klassen zeigen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Eine [ \<T\> IEnumerable-Schnittstelle,](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) die zum Aufzählen der CIM-Klassen verwendet werden kann.

## <a name="see-also"></a>Weitere Informationen

[CimClass-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Microsoft.Management.Infrastructure.Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
