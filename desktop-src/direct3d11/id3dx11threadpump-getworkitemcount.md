---
title: ID3DX11ThreadPump getworkitemcount-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Ruft die Anzahl der Arbeitselemente in der Thread Pumpe ab.
ms.assetid: 04883b25-64dc-41a3-849f-710a59e9d3da
keywords:
- Getworkitemcount-Methode Direct3D 11
- Getworkitemcount-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump-Schnittstelle Direct3D 11, getworkitemcount-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetWorkItemCount
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29668e66dd3d8c6d29cbfc69a4ef12a2fdfd18b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982228"
---
# <a name="id3dx11threadpumpgetworkitemcount-method"></a><span data-ttu-id="beead-107">ID3DX11ThreadPump:: getworkitemcount-Methode</span><span class="sxs-lookup"><span data-stu-id="beead-107">ID3DX11ThreadPump::GetWorkItemCount method</span></span>

> [!Note]  
> <span data-ttu-id="beead-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="beead-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="beead-109">Ruft die Anzahl der Arbeitselemente in der Thread Pumpe ab.</span><span class="sxs-lookup"><span data-stu-id="beead-109">Gets the number of work items in the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="beead-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="beead-110">Syntax</span></span>


```C++
UINT GetWorkItemCount();
```



## <a name="parameters"></a><span data-ttu-id="beead-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="beead-111">Parameters</span></span>

<span data-ttu-id="beead-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="beead-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="beead-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="beead-113">Return value</span></span>

<span data-ttu-id="beead-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="beead-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="beead-115">Die Anzahl der Arbeitselemente, die sich in der Thread Pumpe in der Warteschlange befinden.</span><span class="sxs-lookup"><span data-stu-id="beead-115">The number of work items queued in the thread pump.</span></span>

## <a name="requirements"></a><span data-ttu-id="beead-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="beead-116">Requirements</span></span>



| <span data-ttu-id="beead-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beead-117">Requirement</span></span> | <span data-ttu-id="beead-118">Wert</span><span class="sxs-lookup"><span data-stu-id="beead-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beead-119">Header</span><span class="sxs-lookup"><span data-stu-id="beead-119">Header</span></span><br/>  | <dl> <span data-ttu-id="beead-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="beead-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="beead-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="beead-121">Library</span></span><br/> | <dl> <span data-ttu-id="beead-122"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beead-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="beead-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="beead-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beead-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="beead-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="beead-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="beead-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

