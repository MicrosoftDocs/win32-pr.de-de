---
description: 'Weitere Informationen finden Sie unter: esentdiskexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentdiskexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentDiskException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4abe19b16d9e6eb6d94d5b4fe1dd067b68c2c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349538"
---
# <a name="esentdiskexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="4adbf-103">Esentdiskexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="4adbf-103">EsentDiskException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="4adbf-104">Initialisiert eine neue Instanz der esentdiskexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="4adbf-104">Initializes a new instance of the EsentDiskException class.</span></span> <span data-ttu-id="4adbf-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="4adbf-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="4adbf-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4adbf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4adbf-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4adbf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4adbf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4adbf-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDiskException(info, context)
```

``` csharp
protected EsentDiskException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="4adbf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4adbf-109">Parameters</span></span>

  - <span data-ttu-id="4adbf-110">info</span><span class="sxs-lookup"><span data-stu-id="4adbf-110">info</span></span>  
    <span data-ttu-id="4adbf-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="4adbf-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="4adbf-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4adbf-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="4adbf-113">context</span><span class="sxs-lookup"><span data-stu-id="4adbf-113">context</span></span>  
    <span data-ttu-id="4adbf-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="4adbf-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="4adbf-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="4adbf-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="4adbf-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4adbf-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4adbf-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="4adbf-117">Reference</span></span>

[<span data-ttu-id="4adbf-118">Esentdiskexception-Klasse</span><span class="sxs-lookup"><span data-stu-id="4adbf-118">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="4adbf-119">Esentdiskexception-Member</span><span class="sxs-lookup"><span data-stu-id="4adbf-119">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="4adbf-120">Esentdiskexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="4adbf-120">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="4adbf-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4adbf-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
