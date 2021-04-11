---
description: 'Weitere Informationen finden Sie unter: esentdataexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentdataexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentDataException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101275
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43e7578adb10f607ff88062b48d3f2ebb73d34ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215282"
---
# <a name="esentdataexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="ce654-103">Esentdataexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="ce654-103">EsentDataException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="ce654-104">Initialisiert eine neue Instanz der esentdataexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="ce654-104">Initializes a new instance of the EsentDataException class.</span></span> <span data-ttu-id="ce654-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="ce654-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="ce654-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ce654-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ce654-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ce654-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce654-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce654-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDataException(info, context)
```

``` csharp
protected EsentDataException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="ce654-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce654-109">Parameters</span></span>

  - <span data-ttu-id="ce654-110">info</span><span class="sxs-lookup"><span data-stu-id="ce654-110">info</span></span>  
    <span data-ttu-id="ce654-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="ce654-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="ce654-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce654-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce654-113">context</span><span class="sxs-lookup"><span data-stu-id="ce654-113">context</span></span>  
    <span data-ttu-id="ce654-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="ce654-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="ce654-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="ce654-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce654-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce654-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce654-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="ce654-117">Reference</span></span>

[<span data-ttu-id="ce654-118">Esentdataexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce654-118">EsentDataException class</span></span>](./esentdataexception-class.md)

[<span data-ttu-id="ce654-119">Esentdataexception-Member</span><span class="sxs-lookup"><span data-stu-id="ce654-119">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="ce654-120">Esentdataexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="ce654-120">EsentDataException overload</span></span>](./esentdataexception-constructor.md)

[<span data-ttu-id="ce654-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce654-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
