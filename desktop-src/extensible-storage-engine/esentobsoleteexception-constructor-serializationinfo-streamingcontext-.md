---
description: 'Weitere Informationen finden Sie unter: esentobsoleteexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentobsoleteexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102167
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b287a61396f0d908c888b84553e5dc67df907be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356105"
---
# <a name="esentobsoleteexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="4fdfe-103">Esentobsoleteexception-Konstruktor (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="4fdfe-103">EsentObsoleteException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="4fdfe-104">Initialisiert eine neue Instanz der esentobsoleteexception-Klasse.</span><span class="sxs-lookup"><span data-stu-id="4fdfe-104">Initializes a new instance of the EsentObsoleteException class.</span></span> <span data-ttu-id="4fdfe-105">Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.</span><span class="sxs-lookup"><span data-stu-id="4fdfe-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="4fdfe-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4fdfe-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4fdfe-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4fdfe-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4fdfe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fdfe-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentObsoleteException(info, context)
```

``` csharp
protected EsentObsoleteException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="4fdfe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fdfe-109">Parameters</span></span>

  - <span data-ttu-id="4fdfe-110">info</span><span class="sxs-lookup"><span data-stu-id="4fdfe-110">info</span></span>  
    <span data-ttu-id="4fdfe-111">Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="4fdfe-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="4fdfe-112">Die Daten, die zum Deserialisieren des-Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4fdfe-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="4fdfe-113">context</span><span class="sxs-lookup"><span data-stu-id="4fdfe-113">context</span></span>  
    <span data-ttu-id="4fdfe-114">Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="4fdfe-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="4fdfe-115">Der Deserialisierungskontext.</span><span class="sxs-lookup"><span data-stu-id="4fdfe-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fdfe-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fdfe-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fdfe-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="4fdfe-117">Reference</span></span>

[<span data-ttu-id="4fdfe-118">EsentObsoleteException-Klasse</span><span class="sxs-lookup"><span data-stu-id="4fdfe-118">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="4fdfe-119">Esentobsoleteexception-Member</span><span class="sxs-lookup"><span data-stu-id="4fdfe-119">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="4fdfe-120">Esentobsoleteexception-Überladung</span><span class="sxs-lookup"><span data-stu-id="4fdfe-120">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="4fdfe-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4fdfe-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
