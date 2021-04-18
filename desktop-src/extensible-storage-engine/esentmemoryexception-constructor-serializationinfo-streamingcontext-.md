---
description: 'Weitere Informationen finden Sie unter: esentmemoryexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentmemoryexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentMemoryException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102121
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bf198808de480964b02801c809ab3cff50d35fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368263"
---
# <a name="esentmemoryexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="6318b-103">Esentmemoryexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="6318b-103">EsentMemoryException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="6318b-104">Initialisiert eine neue Instanz der esentmemoryexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6318b-104">Initializes a new instance of the EsentMemoryException class.</span></span> <span data-ttu-id="6318b-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="6318b-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="6318b-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6318b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6318b-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6318b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6318b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6318b-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentMemoryException(info, context)
```

``` csharp
protected EsentMemoryException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="6318b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6318b-109">Parameters</span></span>

  - <span data-ttu-id="6318b-110">info</span><span class="sxs-lookup"><span data-stu-id="6318b-110">info</span></span>  
    <span data-ttu-id="6318b-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="6318b-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="6318b-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="6318b-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="6318b-113">context</span><span class="sxs-lookup"><span data-stu-id="6318b-113">context</span></span>  
    <span data-ttu-id="6318b-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="6318b-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="6318b-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="6318b-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="6318b-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6318b-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6318b-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="6318b-117">Reference</span></span>

[<span data-ttu-id="6318b-118">EsentMemoryException-Klasse</span><span class="sxs-lookup"><span data-stu-id="6318b-118">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="6318b-119">Esentmemoryexception-Member</span><span class="sxs-lookup"><span data-stu-id="6318b-119">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="6318b-120">Esentmemoryexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="6318b-120">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="6318b-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6318b-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
