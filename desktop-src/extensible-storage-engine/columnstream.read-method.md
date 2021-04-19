---
description: 'Weitere Informationen zu: columnstream. Read-Methode'
title: Columnstream. Read-Methode
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373293"
---
# <a name="columnstreamread-method"></a><span data-ttu-id="ec7fc-103">Columnstream. Read-Methode</span><span class="sxs-lookup"><span data-stu-id="ec7fc-103">ColumnStream.Read method</span></span>

<span data-ttu-id="ec7fc-104">Liest eine Bytesequenz aus dem aktuellen Stream und setzt die Position in diesem Stream um die Anzahl der gelesenen Bytes nach vorn.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-104">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span>

<span data-ttu-id="ec7fc-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec7fc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec7fc-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ec7fc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7fc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec7fc-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="ec7fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec7fc-108">Parameters</span></span>

  - <span data-ttu-id="ec7fc-109">Puffer</span><span class="sxs-lookup"><span data-stu-id="ec7fc-109">buffer</span></span>  
    <span data-ttu-id="ec7fc-110">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="ec7fc-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="ec7fc-111">Der Puffer, in den gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-111">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="ec7fc-112">offset</span><span class="sxs-lookup"><span data-stu-id="ec7fc-112">offset</span></span>  
    <span data-ttu-id="ec7fc-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ec7fc-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ec7fc-114">Der Offset im Puffer, in den gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-114">The offset in the buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="ec7fc-115">count</span><span class="sxs-lookup"><span data-stu-id="ec7fc-115">count</span></span>  
    <span data-ttu-id="ec7fc-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ec7fc-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ec7fc-117">Die Anzahl der zu lesenden Bytes.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-117">The number of bytes to read.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ec7fc-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec7fc-118">Return value</span></span>

<span data-ttu-id="ec7fc-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ec7fc-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="ec7fc-120">Die Anzahl der in den Puffer gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="ec7fc-120">The number of bytes read into the buffer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ec7fc-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec7fc-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec7fc-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="ec7fc-122">Reference</span></span>

[<span data-ttu-id="ec7fc-123">Columnstream-Klasse</span><span class="sxs-lookup"><span data-stu-id="ec7fc-123">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="ec7fc-124">Columnstream-Member</span><span class="sxs-lookup"><span data-stu-id="ec7fc-124">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="ec7fc-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec7fc-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
