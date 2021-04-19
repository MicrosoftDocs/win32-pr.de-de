---
description: 'Weitere Informationen finden Sie unter: cimfufdeserializer. deserializeinhaltungen-Methode (Byte [], UInt32, onclassbenötigte, getincludedfilecontent)'
title: Cimfufdeserializer. deserializeinhaltungen-Methode (Byte [], UInt32, onclassbenötigte, getincludedfilecontent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 17a8a84f841f07439b716909fbc8d63232032263
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348480"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="5904e-103">Cimfufdeserializer. deserializeinhaltungen-Methode (Byte \[ \] , UInt32, onclasserforderlich, getincludedfilecontent)</span><span class="sxs-lookup"><span data-stu-id="5904e-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="5904e-104">Deserialisiert CIM-Instanzen auf der Grundlage serialisierter Daten und Rückrufe.</span><span class="sxs-lookup"><span data-stu-id="5904e-104">Deserializes CIM instances based on serialized data, and callbacks.</span></span>

<span data-ttu-id="5904e-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5904e-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="5904e-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="5904e-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="5904e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5904e-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="5904e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5904e-108">Parameters</span></span>

  - <span data-ttu-id="5904e-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="5904e-109">serializedData</span></span>  
    <span data-ttu-id="5904e-110">Typ: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="5904e-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="5904e-111">Ein Puffer, der die serialisierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5904e-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="5904e-112">offset</span><span class="sxs-lookup"><span data-stu-id="5904e-112">offset</span></span>  
    <span data-ttu-id="5904e-113">Typ: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="5904e-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="5904e-114">Der Byte Offset für den Speicherort, an dem mit dem Lesen der Daten begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5904e-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="5904e-115">Wenn die Methode zurückgegeben wird, zeigt der Offset auf das nächste Byte nach den deserialisierten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5904e-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="5904e-116">onclassneeddcallback</span><span class="sxs-lookup"><span data-stu-id="5904e-116">onClassNeededCallback</span></span>  
    <span data-ttu-id="5904e-117">Typ: [onclasserforderliche](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="5904e-117">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="5904e-118">Eine Rückruffunktion, die zum Bereitstellen eines angeforderten Klassen Objekts während der Deserialisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5904e-118">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="5904e-119">getincludfilecallback</span><span class="sxs-lookup"><span data-stu-id="5904e-119">getIncludedFileCallback</span></span>  
    <span data-ttu-id="5904e-120">Typ: [getincludedfilecontent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="5904e-120">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="5904e-121">Eine Rückruffunktion, die verwendet wird, um den Datei Pufferinhalt einer angegebenen Datei bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5904e-121">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5904e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5904e-122">Return value</span></span>

<span data-ttu-id="5904e-123">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="5904e-123">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="5904e-124">Eine [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) -Schnittstelle, die zum Auflisten der CIM-Klassen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5904e-124">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="5904e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5904e-125">See also</span></span>

<span data-ttu-id="5904e-126">[Ciminstance-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5904e-126">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="5904e-127">[Microsoft. Management. Infrastructure. Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5904e-127">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
