---
description: 'Weitere Informationen finden Sie hier: esenterrorexception-Konstruktor'
title: Esenterrorexception-Konstruktor
TOCTitle: 'EsentErrorException constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0728eb316c7d5a5d3cf4a1ad13c2e35451318225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347019"
---
# <a name="esenterrorexception-constructor"></a><span data-ttu-id="6be62-103">Esenterrorexception-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="6be62-103">EsentErrorException constructor</span></span>

<span data-ttu-id="6be62-104">Initialisiert eine neue Instanz der esenterrorexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="6be62-104">Initializes a new instance of the EsentErrorException class.</span></span> <span data-ttu-id="6be62-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="6be62-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="6be62-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6be62-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6be62-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6be62-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6be62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6be62-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentErrorException(info, context)
```

``` csharp
protected EsentErrorException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="6be62-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6be62-109">Parameters</span></span>

  - <span data-ttu-id="6be62-110">info</span><span class="sxs-lookup"><span data-stu-id="6be62-110">info</span></span>  
    <span data-ttu-id="6be62-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="6be62-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="6be62-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="6be62-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="6be62-113">context</span><span class="sxs-lookup"><span data-stu-id="6be62-113">context</span></span>  
    <span data-ttu-id="6be62-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="6be62-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="6be62-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="6be62-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="6be62-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6be62-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6be62-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="6be62-117">Reference</span></span>

[<span data-ttu-id="6be62-118">EsentErrorException-Klasse</span><span class="sxs-lookup"><span data-stu-id="6be62-118">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="6be62-119">Esenterrorexception-Member</span><span class="sxs-lookup"><span data-stu-id="6be62-119">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="6be62-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="6be62-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
