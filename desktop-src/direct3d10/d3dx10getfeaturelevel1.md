---
description: Sie erhalten einen Direct3D 10,1-Geräteschnittstellen Zeiger von einem Direct3D 10,0-Schnittstellen Zeiger.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: D3DX10GetFeatureLevel1-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351921"
---
# <a name="d3dx10getfeaturelevel1-function"></a><span data-ttu-id="650e5-103">D3DX10GetFeatureLevel1-Funktion</span><span class="sxs-lookup"><span data-stu-id="650e5-103">D3DX10GetFeatureLevel1 function</span></span>

<span data-ttu-id="650e5-104">Sie erhalten einen Direct3D 10,1-Geräteschnittstellen Zeiger von einem Direct3D 10,0-Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="650e5-104">Get a Direct3D 10.1 device interface pointer from a Direct3D 10.0 interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="650e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="650e5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="650e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="650e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="650e5-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="650e5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650e5-108">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="650e5-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="650e5-109">Zeiger auf das Direct3D 10,0-Gerät (siehe die [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="650e5-109">Pointer to the Direct3D 10.0 device (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> <dt>

<span data-ttu-id="650e5-110">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="650e5-110">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="650e5-111">Typ: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span><span class="sxs-lookup"><span data-stu-id="650e5-111">Type: **[**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span></span>

<span data-ttu-id="650e5-112">Zeiger auf das Direct3D 10,1-Gerät (siehe die [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) -Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="650e5-112">Pointer to the Direct3D 10.1 device (see the [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="650e5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="650e5-113">Return value</span></span>

<span data-ttu-id="650e5-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="650e5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="650e5-115">Diese Funktion gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="650e5-115">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span> <span data-ttu-id="650e5-116">Wenn eine Direct3D 10,1-Geräteschnittstelle abgerufen werden kann, ist diese Funktion erfolgreich und übergibt mithilfe des *ppdevice* -Parameters einen Zeiger an die 10,1-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="650e5-116">If a Direct3D 10.1 device interface can be acquired, this function succeeds and passes a pointer to the 10.1 interface using the *ppDevice* parameter.</span></span> <span data-ttu-id="650e5-117">Wenn eine Direct3D 10,1-Geräteschnittstelle nicht abgerufen werden kann, gibt diese Funktion "E Fail" zurück \_ und gibt für den *ppdevice* -Parameter nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="650e5-117">If a Direct3D 10.1 device interface cannot be acquired, this function returns E\_FAIL, and will not return anything for the *ppDevice* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="650e5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="650e5-118">Remarks</span></span>

<span data-ttu-id="650e5-119">Damit diese Funktion erfolgreich ausgeführt wird, müssen Sie den bereitgestellten [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Zeiger mithilfe eines Aufrufes der [**D3DX10CreateDevice**](d3dx10createdevice.md) -Funktion, der [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) -Funktion, der [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) -Funktion oder der [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) -Funktion abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="650e5-119">For this function to succeed, you must have acquired the supplied [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) pointer using a call to the [**D3DX10CreateDevice**](d3dx10createdevice.md) function, the [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) function, the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function, or the [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) function.</span></span>

<span data-ttu-id="650e5-120">Sie können auf Computern, auf denen Windows Vista Service Pack 1 oder höher ausgeführt wird, und bei installierter Direct3D 10,1-kompatibler Hardware nur ein Direct3D 10,1-Gerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="650e5-120">You can only create a Direct3D 10.1 device on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="650e5-121">Diese Funktion gibt "E \_ Fail" auf allen Computern zurück, die diese Anforderungen nicht erfüllen.</span><span class="sxs-lookup"><span data-stu-id="650e5-121">This function will return E\_FAIL on any computer not meeting these requirements.</span></span> <span data-ttu-id="650e5-122">Sie können diese Funktion jedoch für jede Windows-Version mit installierter d3dx10-dll-Version aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="650e5-122">However, you can call this function on any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="650e5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="650e5-123">Requirements</span></span>



| <span data-ttu-id="650e5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="650e5-124">Requirement</span></span> | <span data-ttu-id="650e5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="650e5-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="650e5-126">Header</span><span class="sxs-lookup"><span data-stu-id="650e5-126">Header</span></span><br/> | <dl> <span data-ttu-id="650e5-127"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="650e5-127"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="650e5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="650e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650e5-129">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="650e5-129">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




