---
description: 'Weitere Informationen finden Sie unter: cimfufdeserializer. deserializeclasses-Methode (Byte [], UInt32, IEnumerable <CimClass> , String, String, onclassbenötigte, getincludedfilecontent)'
title: Cimfufdeserializer. deserializeclasses-Methode (Byte [], UInt32, IEnumerable (cimclass), String, String, onclassbenötigte, getincludedfilecontent) (Microsoft. Management. Infrastructure. Serialization)
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
ms.openlocfilehash: 5772ca08a94c27e1ae0b110e05192004b9e4df2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524809"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-string-string-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="0336b-103">Cimfufdeserializer. deserializeclasses-Methode (Byte \[ \] , UInt32, IEnumerable \<CimClass\> , String, String, onclassbenötigte, getincludedfilecontent)</span><span class="sxs-lookup"><span data-stu-id="0336b-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>, String, String, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="0336b-104">Deserialisiert CIM-Klassen basierend auf serialisierten Daten, Auflistung von übergeordneten CIM-Klassen, Computer-und Namespace Namen und Rückrufe.</span><span class="sxs-lookup"><span data-stu-id="0336b-104">Deserializes CIM classes based on serialized data, collection of parent CIM classes, computer and namespace names, and callbacks.</span></span>

<span data-ttu-id="0336b-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0336b-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="0336b-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="0336b-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="0336b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0336b-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="0336b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0336b-108">Parameters</span></span>

  - <span data-ttu-id="0336b-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="0336b-109">serializedData</span></span>  
    <span data-ttu-id="0336b-110">Typ: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="0336b-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="0336b-111">Ein Puffer, der die serialisierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0336b-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="0336b-112">offset</span><span class="sxs-lookup"><span data-stu-id="0336b-112">offset</span></span>  
    <span data-ttu-id="0336b-113">Typ: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="0336b-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="0336b-114">Der Byte Offset für den Speicherort, an dem mit dem Lesen der Daten begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0336b-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="0336b-115">Wenn die-Methode zurückgegeben wird, zeigt der Offset auf das nächste Byte nach den deserialisierten Klassen.</span><span class="sxs-lookup"><span data-stu-id="0336b-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="0336b-116">Klassen</span><span class="sxs-lookup"><span data-stu-id="0336b-116">classes</span></span>  
    <span data-ttu-id="0336b-117">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="0336b-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="0336b-118">Ein optionaler Cache von übergeordneten CIM-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0336b-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="0336b-119">computerName</span><span class="sxs-lookup"><span data-stu-id="0336b-119">computerName</span></span>  
    [<span data-ttu-id="0336b-120">System.String</span><span class="sxs-lookup"><span data-stu-id="0336b-120">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="0336b-121">Der Computername.</span><span class="sxs-lookup"><span data-stu-id="0336b-121">The computer name.</span></span>

<!-- end list -->

  - <span data-ttu-id="0336b-122">namespaceName</span><span class="sxs-lookup"><span data-stu-id="0336b-122">namespaceName</span></span>  
    [<span data-ttu-id="0336b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0336b-123">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="0336b-124">Der Namespacename.</span><span class="sxs-lookup"><span data-stu-id="0336b-124">The namespace name.</span></span>

<!-- end list -->

  - <span data-ttu-id="0336b-125">onclassneeddcallback</span><span class="sxs-lookup"><span data-stu-id="0336b-125">onClassNeededCallback</span></span>  
    <span data-ttu-id="0336b-126">Typ: [onclasserforderliche](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="0336b-126">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="0336b-127">Eine Rückruffunktion, die zum Bereitstellen eines angeforderten Klassen Objekts während der Deserialisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0336b-127">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="0336b-128">getincludfilecallback</span><span class="sxs-lookup"><span data-stu-id="0336b-128">getIncludedFileCallback</span></span>  
    <span data-ttu-id="0336b-129">Typ: [getincludedfilecontent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="0336b-129">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="0336b-130">Eine Rückruffunktion, die verwendet wird, um den Datei Pufferinhalt einer angegebenen Datei bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0336b-130">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0336b-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0336b-131">Return value</span></span>

<span data-ttu-id="0336b-132">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="0336b-132">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="0336b-133">Eine [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) -Schnittstelle, die zum Auflisten der CIM-Klassen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0336b-133">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="0336b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0336b-134">See also</span></span>

<span data-ttu-id="0336b-135">[Cimclass-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0336b-135">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="0336b-136">[Microsoft. Management. Infrastructure. Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0336b-136">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
