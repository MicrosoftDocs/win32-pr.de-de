---
description: 'Weitere Informationen finden Sie unter: CimMofDeserializer.DeserializeClasses-Methode (Byte[], UInt32, IEnumerable, <CimClass> String, String, OnClassNeeded, GetIncludedFileContent)'
title: CimMofDeserializer.DeserializeClasses-Methode (Byte[], UInt32, IEnumerable(CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},System.String,System.String,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 9479f30dc8a17c8685a33ad2990313ee85f8434d05fbde549394f3d6a68e32ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050678"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-string-string-onclassneeded-getincludedfilecontent"></a>CimMofDeserializer.DeserializeClasses-Methode (Byte, \[ \] UInt32, IEnumerable, \<CimClass\> String, String, OnClassNeeded, GetIncludedFileContent)

Deserialisiert CIM-Klassen basierend auf serialisierten Daten, der Auflistung übergeordneter CIM-Klassen, Computer- und Namespacenamen und Rückrufen.

**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntax

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    string computerName,
    string namespaceName,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    String^ computerName,
    String^ namespaceName,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        computerName:string *
        namespaceName:string *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    computerName As String,
    namespaceName As String,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
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

<!-- end list -->

  - Klassen  
    Typ: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>
    
    Ein optionaler Cache von übergeordneten CIM-Klassen.

<!-- end list -->

  - computerName  
    [System.String](/dotnet/api/system.string?view=netframework-4.8)
    
    Der Computername.

<!-- end list -->

  - namespaceName  
    [System.String](/dotnet/api/system.string?view=netframework-4.8)
    
    Der Namespacename.

<!-- end list -->

  - onClassNeededCallback  
    Typ: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)
    
    Eine Rückruffunktion, die verwendet wird, um während der Deserialisierung ein angefordertes Klassenobjekt zur Verfügung zu stellen.

<!-- end list -->

  - getIncludedFileCallback  
    Typ: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)
    
    Eine Rückruffunktion, die verwendet wird, um den Dateipufferinhalt einer angegebenen Datei anzugeben.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Eine [ \<T\> IEnumerable-Schnittstelle,](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) die zum Aufzählen der CIM-Klassen verwendet werden kann.

## <a name="see-also"></a>Siehe auch

[CimClass-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Microsoft.Management.Infrastructure.Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
