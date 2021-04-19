---
description: 'Weitere Informationen finden Sie unter: cimmufdeserializer. deserializeinhaltungen-Methode (Byte [], UInt32, IEnumerable <CimClass> , onclasserforderliche, getincludedfilecontent)'
title: Cimfufdeserializer. deserializeinhaltungen-Methode (Byte [], UInt32, IEnumerable (cimclass), onclasserforderliche, getincludedfilecontent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, IEnumerable(CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 081c6d028abdb341d75ff57758c703458fd0b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344986"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a>Cimmufdeserializer. deserializeinhaltungen-Methode (Byte \[ \] , UInt32, IEnumerable \<CimClass\> , onclasserforderliche, getincludedfilecontent)

Deserialisiert CIM-Instanzen auf der Grundlage von serialisierten Daten, eine Auflistung von übergeordneten CIM-Klassen und Rückrufe.

**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntax

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> cimClasses,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ cimClasses,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        cimClasses:IEnumerable<CimClass> *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    cimClasses As IEnumerable(Of CimClass),
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a>Parameter

  - serializedData  
    Typ: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Ein Puffer, der die serialisierten Daten enthält.

<!-- end list -->

  - offset  
    Typ: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Der Byte Offset für den Speicherort, an dem mit dem Lesen der Daten begonnen werden soll. Wenn die Methode zurückgegeben wird, zeigt der Offset auf das nächste Byte nach den deserialisierten Instanzen.

<!-- end list -->

  - cimclasses  
    Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>
    
    Ein optionaler Cache von übergeordneten CIM-Klassen.

<!-- end list -->

  - onclassneeddcallback  
    Typ: [onclasserforderliche](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)
    
    Eine Rückruffunktion, die zum Bereitstellen eines angeforderten Klassen Objekts während der Deserialisierung verwendet wird.

<!-- end list -->

  - getincludfilecallback  
    Typ: [getincludedfilecontent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)
    
    Eine Rückruffunktion, die verwendet wird, um den Datei Pufferinhalt einer angegebenen Datei bereitzustellen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\>

Eine [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) -Schnittstelle, die zum Auflisten der CIM-Klassen verwendet werden kann.

## <a name="see-also"></a>Siehe auch

[Ciminstance-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))  
[Microsoft. Management. Infrastructure. Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
