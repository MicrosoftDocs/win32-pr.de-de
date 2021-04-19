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
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="c9186-103">Cimmufdeserializer. deserializeinhaltungen-Methode (Byte \[ \] , UInt32, IEnumerable \<CimClass\> , onclasserforderliche, getincludedfilecontent)</span><span class="sxs-lookup"><span data-stu-id="c9186-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32, IEnumerable\<CimClass\>, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="c9186-104">Deserialisiert CIM-Instanzen auf der Grundlage von serialisierten Daten, eine Auflistung von übergeordneten CIM-Klassen und Rückrufe.</span><span class="sxs-lookup"><span data-stu-id="c9186-104">Deserializes CIM instances based on serialized data, a collection of parent CIM classes, and callbacks.</span></span>

<span data-ttu-id="c9186-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9186-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="c9186-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="c9186-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="c9186-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9186-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="c9186-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9186-108">Parameters</span></span>

  - <span data-ttu-id="c9186-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="c9186-109">serializedData</span></span>  
    <span data-ttu-id="c9186-110">Typ: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="c9186-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="c9186-111">Ein Puffer, der die serialisierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="c9186-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9186-112">offset</span><span class="sxs-lookup"><span data-stu-id="c9186-112">offset</span></span>  
    <span data-ttu-id="c9186-113">Typ: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="c9186-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="c9186-114">Der Byte Offset für den Speicherort, an dem mit dem Lesen der Daten begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9186-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="c9186-115">Wenn die Methode zurückgegeben wird, zeigt der Offset auf das nächste Byte nach den deserialisierten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="c9186-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9186-116">cimclasses</span><span class="sxs-lookup"><span data-stu-id="c9186-116">cimClasses</span></span>  
    <span data-ttu-id="c9186-117">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="c9186-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="c9186-118">Ein optionaler Cache von übergeordneten CIM-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c9186-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9186-119">onclassneeddcallback</span><span class="sxs-lookup"><span data-stu-id="c9186-119">onClassNeededCallback</span></span>  
    <span data-ttu-id="c9186-120">Typ: [onclasserforderliche](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="c9186-120">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="c9186-121">Eine Rückruffunktion, die zum Bereitstellen eines angeforderten Klassen Objekts während der Deserialisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9186-121">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9186-122">getincludfilecallback</span><span class="sxs-lookup"><span data-stu-id="c9186-122">getIncludedFileCallback</span></span>  
    <span data-ttu-id="c9186-123">Typ: [getincludedfilecontent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="c9186-123">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="c9186-124">Eine Rückruffunktion, die verwendet wird, um den Datei Pufferinhalt einer angegebenen Datei bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c9186-124">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c9186-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9186-125">Return value</span></span>

<span data-ttu-id="c9186-126">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="c9186-126">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="c9186-127">Eine [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) -Schnittstelle, die zum Auflisten der CIM-Klassen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9186-127">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9186-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9186-128">See also</span></span>

<span data-ttu-id="c9186-129">[Ciminstance-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9186-129">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="c9186-130">[Microsoft. Management. Infrastructure. Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9186-130">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
