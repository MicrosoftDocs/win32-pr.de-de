---
description: 'Weitere Informationen finden Sie unter: esentusageexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentusageexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentUsageException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103026
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46100a5f359616b18e5eae0d7b9d9a04b0c2fc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760585"
---
# <a name="esentusageexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="5ec3e-103">Esentusageexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="5ec3e-103">EsentUsageException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="5ec3e-104">Initialisiert eine neue Instanz der esentusageexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="5ec3e-104">Initializes a new instance of the EsentUsageException class.</span></span> <span data-ttu-id="5ec3e-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="5ec3e-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="5ec3e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5ec3e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5ec3e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5ec3e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec3e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ec3e-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentUsageException(info, context)
```

``` csharp
protected EsentUsageException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="5ec3e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ec3e-109">Parameters</span></span>

  - <span data-ttu-id="5ec3e-110">info</span><span class="sxs-lookup"><span data-stu-id="5ec3e-110">info</span></span>  
    <span data-ttu-id="5ec3e-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="5ec3e-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="5ec3e-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="5ec3e-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="5ec3e-113">context</span><span class="sxs-lookup"><span data-stu-id="5ec3e-113">context</span></span>  
    <span data-ttu-id="5ec3e-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="5ec3e-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="5ec3e-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="5ec3e-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ec3e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ec3e-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ec3e-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="5ec3e-117">Reference</span></span>

[<span data-ttu-id="5ec3e-118">EsentUsageException-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ec3e-118">EsentUsageException class</span></span>](./esentusageexception-class.md)

[<span data-ttu-id="5ec3e-119">Esentusageexception-Member</span><span class="sxs-lookup"><span data-stu-id="5ec3e-119">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="5ec3e-120">Esentusageexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="5ec3e-120">EsentUsageException overload</span></span>](./esentusageexception-constructor.md)

[<span data-ttu-id="5ec3e-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ec3e-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
