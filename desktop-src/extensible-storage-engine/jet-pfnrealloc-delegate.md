---
description: 'Weitere Informationen finden Sie hier: JET_PFNREALLOC-Delegaten'
title: JET_PFNREALLOC Delegat
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960865"
---
# <a name="jet_pfnrealloc-delegate"></a><span data-ttu-id="1ebe5-103">JET_PFNREALLOC Delegat</span><span class="sxs-lookup"><span data-stu-id="1ebe5-103">JET_PFNREALLOC delegate</span></span>

<span data-ttu-id="1ebe5-104">Rückruf, der von jetenreeratecolrens verwendet wird, um Speicher für die Ausgabepuffer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-104">Callback used by JetEnumerateColumns to allocate memory for its output buffers.</span></span>

<span data-ttu-id="1ebe5-105">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="1ebe5-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ebe5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ebe5-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ebe5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebe5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ebe5-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a><span data-ttu-id="1ebe5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ebe5-109">Parameters</span></span>

  - <span data-ttu-id="1ebe5-110">context</span><span class="sxs-lookup"><span data-stu-id="1ebe5-110">context</span></span>  
    <span data-ttu-id="1ebe5-111">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="1ebe5-111">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="1ebe5-112">Der für jetenreeratecolumschlag angegebene Kontext.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-112">Context given to JetEnumerateColumns.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ebe5-113">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="1ebe5-113">memory</span></span>  
    <span data-ttu-id="1ebe5-114">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="1ebe5-114">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="1ebe5-115">Wenn ungleich 0 (null), ein Zeiger auf einen Speicherblock, der zuvor von diesem Rückruf zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-115">If non-zero, a pointer to a memory block previously allocated by this callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ebe5-116">requestedSize</span><span class="sxs-lookup"><span data-stu-id="1ebe5-116">requestedSize</span></span>  
    <span data-ttu-id="1ebe5-117">Typ: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="1ebe5-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="1ebe5-118">Die neue Größe des Speicherblocks (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="1ebe5-118">The new size of the memory block (in bytes).</span></span> <span data-ttu-id="1ebe5-119">Wenn dieser Wert 0 ist und ein Speicherblock angegeben wird, wird dieser Speicherblock freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-119">If this is 0 and a memory block is specified, that memory block will be freed.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1ebe5-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ebe5-120">Return value</span></span>

<span data-ttu-id="1ebe5-121">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="1ebe5-121">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
<span data-ttu-id="1ebe5-122">Ein Zeiger auf den neu belegten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-122">A pointer to newly allocated memory.</span></span> <span data-ttu-id="1ebe5-123">Wenn kein Arbeitsspeicher zugeordnet werden konnte, sollte [0](/dotnet/api/system.intptr.zero) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1ebe5-123">If memory could not be allocated then [Zero](/dotnet/api/system.intptr.zero) should be returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ebe5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ebe5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ebe5-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="1ebe5-125">Reference</span></span>

[<span data-ttu-id="1ebe5-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ebe5-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
