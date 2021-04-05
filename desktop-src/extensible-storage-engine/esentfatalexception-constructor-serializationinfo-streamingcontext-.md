---
description: 'Weitere Informationen finden Sie unter: esentfatalexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentfatalexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentFatalException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101554
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2264e3852eb6809f321b9bae162a833e86d7b513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041825"
---
# <a name="esentfatalexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="ddd78-103">Esentfatalexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="ddd78-103">EsentFatalException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="ddd78-104">Initialisiert eine neue Instanz der esentfatalexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="ddd78-104">Initializes a new instance of the EsentFatalException class.</span></span> <span data-ttu-id="ddd78-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="ddd78-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="ddd78-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ddd78-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ddd78-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ddd78-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ddd78-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddd78-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFatalException(info, context)
```

``` csharp
protected EsentFatalException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="ddd78-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddd78-109">Parameters</span></span>

  - <span data-ttu-id="ddd78-110">info</span><span class="sxs-lookup"><span data-stu-id="ddd78-110">info</span></span>  
    <span data-ttu-id="ddd78-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="ddd78-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="ddd78-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ddd78-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="ddd78-113">context</span><span class="sxs-lookup"><span data-stu-id="ddd78-113">context</span></span>  
    <span data-ttu-id="ddd78-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="ddd78-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="ddd78-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="ddd78-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddd78-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddd78-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ddd78-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="ddd78-117">Reference</span></span>

[<span data-ttu-id="ddd78-118">EsentFatalException-Klasse</span><span class="sxs-lookup"><span data-stu-id="ddd78-118">EsentFatalException class</span></span>](./esentfatalexception-class.md)

[<span data-ttu-id="ddd78-119">Esentfatalexception-Member</span><span class="sxs-lookup"><span data-stu-id="ddd78-119">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="ddd78-120">Esentfatalexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="ddd78-120">EsentFatalException overload</span></span>](./esentfatalexception-constructor.md)

[<span data-ttu-id="ddd78-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ddd78-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
