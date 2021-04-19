---
description: 'Weitere Informationen finden Sie unter: esentexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentexception-Konstruktor (SerializationInfo, StreamingContext) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bdcfe5c3b37746f50926850b45763f9d70de893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366513"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="e5a87-103">Esentexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="e5a87-103">EsentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="e5a87-104">Initialisiert eine neue Instanz der esentexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="e5a87-104">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="e5a87-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="e5a87-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="e5a87-106">**Namespace:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5a87-106">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="e5a87-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5a87-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a87-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a87-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="e5a87-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5a87-109">Parameters</span></span>

  - <span data-ttu-id="e5a87-110">info</span><span class="sxs-lookup"><span data-stu-id="e5a87-110">info</span></span>  
    <span data-ttu-id="e5a87-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="e5a87-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="e5a87-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="e5a87-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="e5a87-113">context</span><span class="sxs-lookup"><span data-stu-id="e5a87-113">context</span></span>  
    <span data-ttu-id="e5a87-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="e5a87-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="e5a87-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="e5a87-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5a87-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5a87-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5a87-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="e5a87-117">Reference</span></span>

[<span data-ttu-id="e5a87-118">Esentexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="e5a87-118">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="e5a87-119">Esentexception-Member</span><span class="sxs-lookup"><span data-stu-id="e5a87-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="e5a87-120">Esentexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="e5a87-120">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="e5a87-121">Microsoft. ISAM. ESENT-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5a87-121">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
