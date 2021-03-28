---
title: ID3DX11ThreadPump waitforallitems-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Wartet, bis alle Arbeitselemente in der Thread Pumpe abgeschlossen sind.
ms.assetid: 6dfdaee8-e563-4c37-a2c1-4b115e29c434
keywords:
- Waitforallitems-Methode Direct3D 11
- Waitforallitems-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump Interface Direct3D 11, waitforallitems-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.WaitForAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40abbab67d6743be2190d5e81c733f63b52b32f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995937"
---
# <a name="id3dx11threadpumpwaitforallitems-method"></a><span data-ttu-id="214d1-107">ID3DX11ThreadPump:: waitforallitems-Methode</span><span class="sxs-lookup"><span data-stu-id="214d1-107">ID3DX11ThreadPump::WaitForAllItems method</span></span>

> [!Note]  
> <span data-ttu-id="214d1-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="214d1-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="214d1-109">Wartet, bis alle Arbeitselemente in der Thread Pumpe abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="214d1-109">Waits for all work items in the thread pump to finish.</span></span>

## <a name="syntax"></a><span data-ttu-id="214d1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="214d1-110">Syntax</span></span>


```C++
HRESULT WaitForAllItems();
```



## <a name="parameters"></a><span data-ttu-id="214d1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="214d1-111">Parameters</span></span>

<span data-ttu-id="214d1-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="214d1-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="214d1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="214d1-113">Return value</span></span>

<span data-ttu-id="214d1-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="214d1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="214d1-115">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="214d1-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="214d1-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="214d1-116">Requirements</span></span>



| <span data-ttu-id="214d1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="214d1-117">Requirement</span></span> | <span data-ttu-id="214d1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="214d1-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="214d1-119">Header</span><span class="sxs-lookup"><span data-stu-id="214d1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="214d1-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="214d1-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="214d1-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="214d1-121">Library</span></span><br/> | <dl> <span data-ttu-id="214d1-122"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="214d1-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="214d1-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="214d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214d1-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="214d1-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="214d1-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="214d1-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





