---
description: 'Weitere Informationen finden Sie unter: esentquotaexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentquotaexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentQuotaException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102338
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36748053b8b9b48041c07ff51c99c0144093a9ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348328"
---
# <a name="esentquotaexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="06c09-103">Esentquotaexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="06c09-103">EsentQuotaException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="06c09-104">Initialisiert eine neue Instanz der esentquotaexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="06c09-104">Initializes a new instance of the EsentQuotaException class.</span></span> <span data-ttu-id="06c09-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="06c09-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="06c09-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06c09-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06c09-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="06c09-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06c09-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06c09-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentQuotaException(info, context)
```

``` csharp
protected EsentQuotaException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="06c09-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="06c09-109">Parameters</span></span>

  - <span data-ttu-id="06c09-110">info</span><span class="sxs-lookup"><span data-stu-id="06c09-110">info</span></span>  
    <span data-ttu-id="06c09-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="06c09-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="06c09-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="06c09-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="06c09-113">context</span><span class="sxs-lookup"><span data-stu-id="06c09-113">context</span></span>  
    <span data-ttu-id="06c09-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="06c09-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="06c09-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="06c09-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="06c09-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06c09-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06c09-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="06c09-117">Reference</span></span>

[<span data-ttu-id="06c09-118">EsentQuotaException-Klasse</span><span class="sxs-lookup"><span data-stu-id="06c09-118">EsentQuotaException class</span></span>](./esentquotaexception-class.md)

[<span data-ttu-id="06c09-119">Esentquotaexception-Member</span><span class="sxs-lookup"><span data-stu-id="06c09-119">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="06c09-120">Esentquotaexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="06c09-120">EsentQuotaException overload</span></span>](./esentquotaexception-constructor.md)

[<span data-ttu-id="06c09-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="06c09-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
