---
description: 'Weitere Informationen finden Sie unter: cimmufdeserializer. deserializeclasses-Methode (Byte [], UInt32)'
title: Cimmufdeserializer. deserializeclasses-Methode (Byte [], UInt32) (Microsoft. Management. Infrastructure. Serialization)
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
ms.openlocfilehash: 983fa9e8fe36b872d05c3140c74f572b7d1ebf50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524815"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a>Cimmufdeserializer. deserializeclasses-Methode (Byte \[ \] , UInt32)

Deserialisiert CIM-Klassen auf der Grundlage von serialisierten Daten.

**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)  

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
    Typ: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Ein Puffer, der die serialisierten Daten enthält.

<!-- end list -->

  - offset  
    Typ: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Der Byte Offset für den Speicherort, an dem mit dem Lesen der Daten begonnen werden soll. Wenn die-Methode zurückgegeben wird, zeigt der Offset auf das nächste Byte nach den deserialisierten Klassen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Eine [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) -Schnittstelle, die zum Auflisten der CIM-Klassen verwendet werden kann.

## <a name="see-also"></a>Siehe auch

[Cimclass-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Microsoft. Management. Infrastructure. Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
