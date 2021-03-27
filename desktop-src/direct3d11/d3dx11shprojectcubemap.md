---
title: D3DX11SHProjectCubeMap-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie die spprojectcubemap der sphärischen Harmonics-Bibliothek verwenden, anstatt diese Funktion zu verwenden.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- D3DX11SHProjectCubeMap-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995980"
---
# <a name="d3dx11shprojectcubemap-function"></a><span data-ttu-id="fe206-105">D3DX11SHProjectCubeMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe206-105">D3DX11SHProjectCubeMap function</span></span>

> [!Note]  
> <span data-ttu-id="fe206-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe206-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe206-107">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die für die **spprojectcubemap** verwendete [sphärischen Harmonics](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) -Bibliothek zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe206-107">Instead of using this function, we recommend that you use the [Spherical Harmonics Math](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) library, **SHProjectCubeMap**.</span></span>

 

<span data-ttu-id="fe206-108">Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.</span><span class="sxs-lookup"><span data-stu-id="fe206-108">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe206-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe206-109">Syntax</span></span>


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="fe206-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe206-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe206-111">*pContext*</span><span class="sxs-lookup"><span data-stu-id="fe206-111">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="fe206-112">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="fe206-112">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="fe206-113">Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="fe206-113">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="fe206-114">*Order*</span><span class="sxs-lookup"><span data-stu-id="fe206-114">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="fe206-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe206-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe206-116">Die Reihenfolge der SH-Auswertung generiert Reihenfolge ^ 2-Koeffizienten, deren Grad "Order-1" ist.</span><span class="sxs-lookup"><span data-stu-id="fe206-116">Order of the SH evaluation, generates Order^2 coefficients whose degree is Order-1.</span></span> <span data-ttu-id="fe206-117">Der gültige Bereich liegt zwischen 2 und 6.</span><span class="sxs-lookup"><span data-stu-id="fe206-117">Valid range is between 2 and 6.</span></span>

</dd> <dt>

<span data-ttu-id="fe206-118">*pcubemap*</span><span class="sxs-lookup"><span data-stu-id="fe206-118">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="fe206-119">Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="fe206-119">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="fe206-120">Ein Zeiger auf eine [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , die eine cubemap darstellt, die in sphärischen Harmoniken projiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe206-120">A pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) that represents a cubemap that is going to be projected into spherical harmonics.</span></span>

</dd> <dt>

<span data-ttu-id="fe206-121">*Proxy*</span><span class="sxs-lookup"><span data-stu-id="fe206-121">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="fe206-122">Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="fe206-122">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="fe206-123">Ausgabe SH-Vektor für rot.</span><span class="sxs-lookup"><span data-stu-id="fe206-123">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="fe206-124">*pgout*</span><span class="sxs-lookup"><span data-stu-id="fe206-124">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="fe206-125">Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="fe206-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="fe206-126">Ausgabe SH-Vektor für grün.</span><span class="sxs-lookup"><span data-stu-id="fe206-126">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="fe206-127">*pbout*</span><span class="sxs-lookup"><span data-stu-id="fe206-127">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="fe206-128">Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="fe206-128">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="fe206-129">Ausgabe SH-Vektor für blau.</span><span class="sxs-lookup"><span data-stu-id="fe206-129">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe206-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe206-130">Return value</span></span>

<span data-ttu-id="fe206-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe206-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe206-132">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="fe206-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe206-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fe206-133">Requirements</span></span>



| <span data-ttu-id="fe206-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe206-134">Requirement</span></span> | <span data-ttu-id="fe206-135">Wert</span><span class="sxs-lookup"><span data-stu-id="fe206-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe206-136">Header</span><span class="sxs-lookup"><span data-stu-id="fe206-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fe206-137"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe206-137"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fe206-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe206-138">Library</span></span><br/> | <dl> <span data-ttu-id="fe206-139"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe206-139"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fe206-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe206-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe206-141">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fe206-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

