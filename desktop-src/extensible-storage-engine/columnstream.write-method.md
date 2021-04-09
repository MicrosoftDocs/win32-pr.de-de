---
description: 'Weitere Informationen zu: columnstream. Write-Methode'
title: Columnstream. Write-Methode
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050420"
---
# <a name="columnstreamwrite-method"></a><span data-ttu-id="440c0-103">Columnstream. Write-Methode</span><span class="sxs-lookup"><span data-stu-id="440c0-103">ColumnStream.Write method</span></span>

<span data-ttu-id="440c0-104">Schreibt eine Bytesequenz in den aktuellen Stream und setzt die aktuelle Position in diesem Stream um die Anzahl der geschriebenen Bytes nach vorn.</span><span class="sxs-lookup"><span data-stu-id="440c0-104">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span>

<span data-ttu-id="440c0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="440c0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="440c0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="440c0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="440c0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="440c0-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="440c0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="440c0-108">Parameters</span></span>

  - <span data-ttu-id="440c0-109">Puffer</span><span class="sxs-lookup"><span data-stu-id="440c0-109">buffer</span></span>  
    <span data-ttu-id="440c0-110">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="440c0-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="440c0-111">Der Puffer, aus dem geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="440c0-111">The buffer to write from.</span></span>

<!-- end list -->

  - <span data-ttu-id="440c0-112">offset</span><span class="sxs-lookup"><span data-stu-id="440c0-112">offset</span></span>  
    <span data-ttu-id="440c0-113">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="440c0-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="440c0-114">Der Offset im Puffer, der geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="440c0-114">The offset in the buffer to write.</span></span>

<!-- end list -->

  - <span data-ttu-id="440c0-115">count</span><span class="sxs-lookup"><span data-stu-id="440c0-115">count</span></span>  
    <span data-ttu-id="440c0-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="440c0-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="440c0-117">Die Anzahl der zu schreibenden Bytes.</span><span class="sxs-lookup"><span data-stu-id="440c0-117">The number of bytes to write.</span></span>

## <a name="see-also"></a><span data-ttu-id="440c0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="440c0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="440c0-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="440c0-119">Reference</span></span>

[<span data-ttu-id="440c0-120">Columnstream-Klasse</span><span class="sxs-lookup"><span data-stu-id="440c0-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="440c0-121">Columnstream-Member</span><span class="sxs-lookup"><span data-stu-id="440c0-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="440c0-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="440c0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
