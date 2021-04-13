---
description: 'Weitere Informationen finden Sie unter: esentfragmentationexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentfragmentationexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentFragmentationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101633
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 251e4beaacb1e895c1da1d501b38cf03f211dd99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350519"
---
# <a name="esentfragmentationexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="71088-103">Esentfragmentationexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="71088-103">EsentFragmentationException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="71088-104">Initialisiert eine neue Instanz der esentfragmentationexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="71088-104">Initializes a new instance of the EsentFragmentationException class.</span></span> <span data-ttu-id="71088-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="71088-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="71088-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71088-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71088-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71088-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71088-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71088-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFragmentationException(info, context)
```

``` csharp
protected EsentFragmentationException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="71088-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="71088-109">Parameters</span></span>

  - <span data-ttu-id="71088-110">info</span><span class="sxs-lookup"><span data-stu-id="71088-110">info</span></span>  
    <span data-ttu-id="71088-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="71088-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="71088-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="71088-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="71088-113">context</span><span class="sxs-lookup"><span data-stu-id="71088-113">context</span></span>  
    <span data-ttu-id="71088-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="71088-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="71088-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="71088-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="71088-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71088-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71088-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="71088-117">Reference</span></span>

[<span data-ttu-id="71088-118">EsentFragmentationException-Klasse</span><span class="sxs-lookup"><span data-stu-id="71088-118">EsentFragmentationException class</span></span>](./esentfragmentationexception-class.md)

[<span data-ttu-id="71088-119">Esentfragmentationexception-Member</span><span class="sxs-lookup"><span data-stu-id="71088-119">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="71088-120">Esentfragmentationexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="71088-120">EsentFragmentationException overload</span></span>](./esentfragmentationexception-constructor.md)

[<span data-ttu-id="71088-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="71088-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
