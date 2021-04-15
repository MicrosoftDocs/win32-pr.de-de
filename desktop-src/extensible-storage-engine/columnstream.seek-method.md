---
description: 'Weitere Informationen zu: columnstream. Seek-Methode'
title: Columnstream. Seek-Methode
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527560"
---
# <a name="columnstreamseek-method"></a><span data-ttu-id="b3f32-103">Columnstream. Seek-Methode</span><span class="sxs-lookup"><span data-stu-id="b3f32-103">ColumnStream.Seek method</span></span>

<span data-ttu-id="b3f32-104">Legt die Position im aktuellen Stream fest.</span><span class="sxs-lookup"><span data-stu-id="b3f32-104">Sets the position in the current stream.</span></span>

<span data-ttu-id="b3f32-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3f32-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b3f32-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3f32-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f32-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3f32-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a><span data-ttu-id="b3f32-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3f32-108">Parameters</span></span>

  - <span data-ttu-id="b3f32-109">offset</span><span class="sxs-lookup"><span data-stu-id="b3f32-109">offset</span></span>  
    <span data-ttu-id="b3f32-110">Typ: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="b3f32-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="b3f32-111">Byte Offset relativ zum Ursprungs Parameter.</span><span class="sxs-lookup"><span data-stu-id="b3f32-111">Byte offset relative to the origin parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="b3f32-112">Origin</span><span class="sxs-lookup"><span data-stu-id="b3f32-112">origin</span></span>  
    <span data-ttu-id="b3f32-113">Typ: [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)</span><span class="sxs-lookup"><span data-stu-id="b3f32-113">Type: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)</span></span>  
    
    <span data-ttu-id="b3f32-114">Ein SeekOrigin, der den Bezugspunkt für die neue Position angibt.</span><span class="sxs-lookup"><span data-stu-id="b3f32-114">A SeekOrigin indicating the reference point for the new position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b3f32-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3f32-115">Return value</span></span>

<span data-ttu-id="b3f32-116">Typ: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="b3f32-116">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
<span data-ttu-id="b3f32-117">Die neue Position im aktuellen Stream.</span><span class="sxs-lookup"><span data-stu-id="b3f32-117">The new position in the current stream.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b3f32-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3f32-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3f32-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="b3f32-119">Reference</span></span>

[<span data-ttu-id="b3f32-120">Columnstream-Klasse</span><span class="sxs-lookup"><span data-stu-id="b3f32-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="b3f32-121">Columnstream-Member</span><span class="sxs-lookup"><span data-stu-id="b3f32-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="b3f32-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b3f32-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
