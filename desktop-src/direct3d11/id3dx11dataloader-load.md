---
title: ID3DX11DataLoader Load-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Lädt Daten von einem Datenträger.
ms.assetid: 21dee078-af8f-4ca1-bb2e-d4ecc0471609
keywords:
- Load-Methode Direct3D 11
- Load-Methode Direct3D 11, ID3DX11DataLoader-Schnittstelle
- ID3DX11DataLoader-Schnittstelle Direct3D 11, Load-Methode
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Load
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f720a5e6884bfdf1935c6d93f7a05decae5e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982613"
---
# <a name="id3dx11dataloaderload-method"></a><span data-ttu-id="ab9cd-107">ID3DX11DataLoader:: Load-Methode</span><span class="sxs-lookup"><span data-stu-id="ab9cd-107">ID3DX11DataLoader::Load method</span></span>

> [!Note]  
> <span data-ttu-id="ab9cd-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="ab9cd-109">Lädt Daten von einem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-109">Loads data from a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab9cd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab9cd-110">Syntax</span></span>


```C++
HRESULT Load();
```



## <a name="parameters"></a><span data-ttu-id="ab9cd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab9cd-111">Parameters</span></span>

<span data-ttu-id="ab9cd-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab9cd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab9cd-113">Return value</span></span>

<span data-ttu-id="ab9cd-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab9cd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab9cd-115">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab9cd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab9cd-116">Remarks</span></span>

<span data-ttu-id="ab9cd-117">Diese Methode wird von einer [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab9cd-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab9cd-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ab9cd-118">Requirements</span></span>



| <span data-ttu-id="ab9cd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab9cd-119">Requirement</span></span> | <span data-ttu-id="ab9cd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ab9cd-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9cd-121">Header</span><span class="sxs-lookup"><span data-stu-id="ab9cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ab9cd-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab9cd-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="ab9cd-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab9cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="ab9cd-124"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab9cd-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab9cd-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab9cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab9cd-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="ab9cd-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="ab9cd-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ab9cd-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





