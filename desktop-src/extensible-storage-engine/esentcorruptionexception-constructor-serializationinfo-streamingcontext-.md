---
description: 'Weitere Informationen finden Sie unter: esentverdertionexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentkorruptionexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentCorruptionException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101038
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0e80255d86ed6f953e4010541e98b794537f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960781"
---
# <a name="esentcorruptionexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="7d9d3-103">Esentkorruptionexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="7d9d3-103">EsentCorruptionException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="7d9d3-104">Initialisiert eine neue Instanz der esentkorruptionexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="7d9d3-104">Initializes a new instance of the EsentCorruptionException class.</span></span> <span data-ttu-id="7d9d3-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="7d9d3-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="7d9d3-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d9d3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d9d3-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d9d3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d9d3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d9d3-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentCorruptionException(info, context)
```

``` csharp
protected EsentCorruptionException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="7d9d3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d9d3-109">Parameters</span></span>

  - <span data-ttu-id="7d9d3-110">info</span><span class="sxs-lookup"><span data-stu-id="7d9d3-110">info</span></span>  
    <span data-ttu-id="7d9d3-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="7d9d3-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="7d9d3-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="7d9d3-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="7d9d3-113">context</span><span class="sxs-lookup"><span data-stu-id="7d9d3-113">context</span></span>  
    <span data-ttu-id="7d9d3-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="7d9d3-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="7d9d3-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="7d9d3-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d9d3-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d9d3-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d9d3-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="7d9d3-117">Reference</span></span>

[<span data-ttu-id="7d9d3-118">EsentCorruptionException-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d9d3-118">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="7d9d3-119">Esentverdertionexception-Member</span><span class="sxs-lookup"><span data-stu-id="7d9d3-119">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="7d9d3-120">Esentkorruptionexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="7d9d3-120">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="7d9d3-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7d9d3-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
