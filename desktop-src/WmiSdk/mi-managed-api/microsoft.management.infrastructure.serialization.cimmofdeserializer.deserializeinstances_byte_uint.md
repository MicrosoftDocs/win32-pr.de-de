---
description: 'Weitere Informationen zu: CimMofDeserializer.DeserializeInstances-Methode (Byte[], UInt32)'
title: CimMofDeserializer.DeserializeInstances-Methode (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: c44270429dc81c64d26b5e2512686bde97ac7851235eab01ebd545aae762e0ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317329"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a>CimMofDeserializer.DeserializeInstances-Methode (Byte, \[ \] UInt32)

Deserialisiert CIM-Instanzen basierend auf serialisierten Daten.

**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntax

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a>Parameter

  - serializedData  
    Typ: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Ein Puffer, der die serialisierten Daten enthält.

<!-- end list -->

  - offset  
    Typ: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Der Byteoffset zu der Position, an der mit dem Lesen der Daten begonnen werden soll. Wenn die Methode zurückgegeben wird, verweist der Offset auf das nächste Byte nach den deserialisierten Instanzen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\>

Eine [ \<T\> IEnumerable-Schnittstelle,](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) die zum Aufzählen der CIM-Klassen verwendet werden kann.

## <a name="see-also"></a>Weitere Informationen

[CimInstance-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))  
[Microsoft.Management.Infrastructure.Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
