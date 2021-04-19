---
description: 'Weitere Informationen finden Sie unter: esentresourceexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentresourceexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentResourceException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102649
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f7b52e211d155b92a9917670682af735eedf9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369897"
---
# <a name="esentresourceexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="6f1aa-103">Esentresourceexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="6f1aa-103">EsentResourceException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="6f1aa-104">Initialisiert eine neue Instanz der esentresourceexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-104">Initializes a new instance of the EsentResourceException class.</span></span> <span data-ttu-id="6f1aa-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="6f1aa-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f1aa-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f1aa-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6f1aa-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1aa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f1aa-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentResourceException(info, context)
```

``` csharp
protected EsentResourceException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="6f1aa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f1aa-109">Parameters</span></span>

  - <span data-ttu-id="6f1aa-110">info</span><span class="sxs-lookup"><span data-stu-id="6f1aa-110">info</span></span>  
    <span data-ttu-id="6f1aa-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="6f1aa-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="6f1aa-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f1aa-113">context</span><span class="sxs-lookup"><span data-stu-id="6f1aa-113">context</span></span>  
    <span data-ttu-id="6f1aa-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="6f1aa-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="6f1aa-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f1aa-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f1aa-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f1aa-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="6f1aa-117">Reference</span></span>

[<span data-ttu-id="6f1aa-118">EsentResourceException-Klasse</span><span class="sxs-lookup"><span data-stu-id="6f1aa-118">EsentResourceException class</span></span>](./esentresourceexception-class.md)

[<span data-ttu-id="6f1aa-119">Esentresourceexception-Member</span><span class="sxs-lookup"><span data-stu-id="6f1aa-119">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="6f1aa-120">Esentresourceexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="6f1aa-120">EsentResourceException overload</span></span>](./esentresourceexception-constructor.md)

[<span data-ttu-id="6f1aa-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6f1aa-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
