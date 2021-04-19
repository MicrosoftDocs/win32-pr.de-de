---
description: 'Weitere Informationen finden Sie unter: cimmufdeserializer. deserializeclasses-Methode (Byte [], UInt32, IEnumerable <CimClass> )'
title: Cimmufdeserializer. deserializeclasses-Methode (Byte [], UInt32, IEnumerable (cimclass)) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass)) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass})
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
ms.openlocfilehash: edcdb84e9c3a3fe7a070263385c9ee6551341152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363708"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a><span data-ttu-id="f4b41-103">Cimmufdeserializer. deserializeclasses-Methode (Byte \[ \] , UInt32, IEnumerable \<CimClass\> )</span><span class="sxs-lookup"><span data-stu-id="f4b41-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>)</span></span>

<span data-ttu-id="f4b41-104">Deserialisiert CIM-Klassen auf der Grundlage von serialisierten Daten und eine Auflistung von übergeordneten CIM-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f4b41-104">Deserializes CIM classes based on serialized data, and a collection of parent CIM classes.</span></span>

<span data-ttu-id="f4b41-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4b41-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="f4b41-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="f4b41-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="f4b41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4b41-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass)
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="f4b41-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4b41-108">Parameters</span></span>

  - <span data-ttu-id="f4b41-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="f4b41-109">serializedData</span></span>  
    <span data-ttu-id="f4b41-110">Typ: [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="f4b41-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="f4b41-111">Ein Puffer, der die serialisierten Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f4b41-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4b41-112">offset</span><span class="sxs-lookup"><span data-stu-id="f4b41-112">offset</span></span>  
    <span data-ttu-id="f4b41-113">Typ: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="f4b41-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="f4b41-114">Der Byte Offset für den Speicherort, an dem mit dem Lesen der Daten begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4b41-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="f4b41-115">Wenn die-Methode zurückgegeben wird, zeigt der Offset auf das nächste Byte nach den deserialisierten Klassen.</span><span class="sxs-lookup"><span data-stu-id="f4b41-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4b41-116">Klassen</span><span class="sxs-lookup"><span data-stu-id="f4b41-116">classes</span></span>  
    <span data-ttu-id="f4b41-117">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f4b41-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="f4b41-118">Ein optionaler Cache von übergeordneten CIM-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f4b41-118">An optional cache of parent CIM classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f4b41-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4b41-119">Return value</span></span>

<span data-ttu-id="f4b41-120">Typ: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="f4b41-120">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="f4b41-121">Eine [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) -Schnittstelle, die zum Auflisten der CIM-Klassen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4b41-121">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4b41-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4b41-122">See also</span></span>

<span data-ttu-id="f4b41-123">[Cimclass-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4b41-123">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="f4b41-124">[Microsoft. Management. Infrastructure. Serialization-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4b41-124">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
