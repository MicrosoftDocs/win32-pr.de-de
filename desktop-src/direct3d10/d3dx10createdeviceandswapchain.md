---
description: Erstellen Sie das beste Direct3D-Gerät und eine SwapChain.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: D3DX10CreateDeviceAndSwapChain-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355547"
---
# <a name="d3dx10createdeviceandswapchain-function"></a><span data-ttu-id="1d05e-103">D3DX10CreateDeviceAndSwapChain-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d05e-103">D3DX10CreateDeviceAndSwapChain function</span></span>

<span data-ttu-id="1d05e-104">Erstellen Sie das beste Direct3D-Gerät und eine SwapChain.</span><span class="sxs-lookup"><span data-stu-id="1d05e-104">Create the best Direct3D device and a swap chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d05e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d05e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="1d05e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d05e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d05e-107">*padapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d05e-107">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d05e-108">Typ: **[ **idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="1d05e-108">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="1d05e-109">Zeiger auf einen [**idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span><span class="sxs-lookup"><span data-stu-id="1d05e-109">Pointer to a [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span></span>

</dd> <dt>

<span data-ttu-id="1d05e-110">*DriverType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d05e-110">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d05e-111">Type: **[ **d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="1d05e-111">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="1d05e-112">Der Typ des Treibers für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="1d05e-112">The type of driver for the device.</span></span> <span data-ttu-id="1d05e-113">Siehe [**d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span><span class="sxs-lookup"><span data-stu-id="1d05e-113">See [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span></span>

</dd> <dt>

<span data-ttu-id="1d05e-114">*Software* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d05e-114">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d05e-115">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d05e-115">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d05e-116">Ein Handle für die dll, die einen Software-Rasterizer implementiert.</span><span class="sxs-lookup"><span data-stu-id="1d05e-116">A handle to the DLL that implements a software rasterizer.</span></span> <span data-ttu-id="1d05e-117">Muss **null** sein, wenn der DriverType nicht-Software ist.</span><span class="sxs-lookup"><span data-stu-id="1d05e-117">Must be **NULL** if DriverType is non-software.</span></span> <span data-ttu-id="1d05e-118">Das HMODULE einer DLL kann mit [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)oder [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d05e-118">The HMODULE of a DLL can be obtained with [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa), or [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="1d05e-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1d05e-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d05e-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d05e-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d05e-121">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="1d05e-121">Optional.</span></span> <span data-ttu-id="1d05e-122">Geräteerstellungsflags (siehe [**d3d10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)), die [API-Ebenen](d3d10-graphics-programming-guide-api-features-layers.md)aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1d05e-122">Device creation flags (see [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="1d05e-123">Diese Flags können bitweise oder gleich sein.</span><span class="sxs-lookup"><span data-stu-id="1d05e-123">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="1d05e-124">*ptauapchaindesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d05e-124">*pSwapChainDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d05e-125">Typ: **[ **DXGI- \_ Austausch \_ Kette \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span><span class="sxs-lookup"><span data-stu-id="1d05e-125">Type: **[**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span></span>

<span data-ttu-id="1d05e-126">Die Beschreibung der Austausch Kette.</span><span class="sxs-lookup"><span data-stu-id="1d05e-126">Description of the swap chain.</span></span> <span data-ttu-id="1d05e-127">Weitere Informationen finden Sie unter [**DXGI \_ Swap \_ Chain \_**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)Debug.</span><span class="sxs-lookup"><span data-stu-id="1d05e-127">See [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span></span>

</dd> <dt>

<span data-ttu-id="1d05e-128">*ppswapchain* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d05e-128">*ppSwapChain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d05e-129">Typ: **[ **idxgiswapchain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span><span class="sxs-lookup"><span data-stu-id="1d05e-129">Type: **[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span></span>

<span data-ttu-id="1d05e-130">Adresse eines Zeigers auf eine [**idxgiswapchain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="1d05e-130">Address of a pointer to an [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

</dd> <dt>

<span data-ttu-id="1d05e-131">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d05e-131">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d05e-132">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="1d05e-132">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="1d05e-133">Adresse eines Zeigers auf eine [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) , die das neu erstellte Gerät empfängt.</span><span class="sxs-lookup"><span data-stu-id="1d05e-133">Address of a pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) that will receive the newly created device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d05e-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d05e-134">Return value</span></span>

<span data-ttu-id="1d05e-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d05e-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d05e-136">Diese Methode gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="1d05e-136">This method returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d05e-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d05e-137">Remarks</span></span>

<span data-ttu-id="1d05e-138">Um das beste Gerät zu erstellen, implementiert diese Methode mehr als eine Geräte Erstellungs Option.</span><span class="sxs-lookup"><span data-stu-id="1d05e-138">To create the best device, this method implements more than one device creation option.</span></span> <span data-ttu-id="1d05e-139">Zuerst versucht die-Methode, ein 10,1-Gerät (und eine SwapChain) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d05e-139">First, the method attempts to create a 10.1 device (and swap chain).</span></span> <span data-ttu-id="1d05e-140">Wenn dies fehlschlägt, versucht die Methode, ein 10,0-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d05e-140">If that fails, the method attempts to create a 10.0 device.</span></span> <span data-ttu-id="1d05e-141">Wenn dies fehlschlägt, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="1d05e-141">If that fails, the method will fail.</span></span> <span data-ttu-id="1d05e-142">Wenn Ihre Anwendung nur ein 10,1-Gerät oder nur ein 10,0-Gerät erstellen muss, verwenden Sie stattdessen diese APIs:</span><span class="sxs-lookup"><span data-stu-id="1d05e-142">If your application needs to create only a 10.1 device, or a 10.0 device only, use these APIs instead:</span></span>

-   <span data-ttu-id="1d05e-143">Verwenden Sie [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) , um ein Gerät vom Typ Direct3D 10,0 (nur) und eine Austausch Kette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d05e-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) to create a Direct3D 10.0 (only) device and swap chain.</span></span>
-   <span data-ttu-id="1d05e-144">Verwenden Sie [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) , um ein Gerät vom Typ Direct3D 10,1 (nur) und eine Austausch Kette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d05e-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) to create a Direct3D 10.1 (only) device and swap chain.</span></span>

<span data-ttu-id="1d05e-145">Diese Methode erfordert Windows Vista Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1d05e-145">This method requires Windows Vista Service Pack 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d05e-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d05e-146">Requirements</span></span>



| <span data-ttu-id="1d05e-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d05e-147">Requirement</span></span> | <span data-ttu-id="1d05e-148">Wert</span><span class="sxs-lookup"><span data-stu-id="1d05e-148">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d05e-149">Header</span><span class="sxs-lookup"><span data-stu-id="1d05e-149">Header</span></span><br/> | <dl> <span data-ttu-id="1d05e-150"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d05e-150"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d05e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d05e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d05e-152">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="1d05e-152">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
