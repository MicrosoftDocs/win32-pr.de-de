---
description: Erstellen Sie das beste Direct3D 10-Gerät, das den Anzeige Adapter darstellt. Wenn ein Direct3D 10,1-kompatibles Gerät erstellt werden kann, ist es möglich, einen ID3D10Device1-Schnittstellen Zeiger vom zurückgegebenen Geräteschnittstellen Zeiger zu erhalten.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: D3DX10CreateDevice-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355828"
---
# <a name="d3dx10createdevice-function"></a><span data-ttu-id="15695-104">D3DX10CreateDevice-Funktion</span><span class="sxs-lookup"><span data-stu-id="15695-104">D3DX10CreateDevice function</span></span>

<span data-ttu-id="15695-105">Erstellen Sie das beste Direct3D 10-Gerät, das den Anzeige Adapter darstellt.</span><span class="sxs-lookup"><span data-stu-id="15695-105">Create the best Direct3D 10 device that represents the display adapter.</span></span> <span data-ttu-id="15695-106">Wenn ein Direct3D 10,1-kompatibles Gerät erstellt werden kann, ist es möglich, einen [**ID3D10Device1-Schnittstellen**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) Zeiger vom zurückgegebenen Geräteschnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15695-106">If a Direct3D 10.1-compatible device can be created, it will be possible to acquire an [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) pointer from the returned device interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="15695-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="15695-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="15695-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15695-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15695-109">*padapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-109">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-110">Typ: **[ **idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="15695-110">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="15695-111">Zeiger auf den Anzeige Adapter (siehe die [**idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) -Schnittstelle), wenn ein Hardware Gerät erstellt wird. andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="15695-111">Pointer to the display adapter (see the [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) interface) when creating a hardware device; otherwise set this parameter to **NULL**.</span></span> <span data-ttu-id="15695-112">Wenn beim Erstellen eines Hardware Geräts **null** angegeben wird, verwendet Direct3D den ersten Adapter, der von der [**idxgifactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) -Schnittstelle aufgezählt wird.</span><span class="sxs-lookup"><span data-stu-id="15695-112">If **NULL** is specified when creating a hardware device, Direct3D will use the first adapter enumerated by the [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) interface.</span></span>

</dd> <dt>

<span data-ttu-id="15695-113">*DriverType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-113">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-114">Type: **[ **d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="15695-114">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="15695-115">Der Gerätetreiber-Typ (siehe [**d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) Enumeration).</span><span class="sxs-lookup"><span data-stu-id="15695-115">The device-driver type (see the [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) enumeration).</span></span> <span data-ttu-id="15695-116">Der Treibertyp bestimmt den Gerätetyp, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="15695-116">The driver type determines the type of device you will create.</span></span>

</dd> <dt>

<span data-ttu-id="15695-117">*Software* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15695-117">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-118">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15695-118">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15695-119">Ein Handle für ein geladenes Modul, das einen Software Treiber (z. b. D3D10Ref.dll) implementiert.</span><span class="sxs-lookup"><span data-stu-id="15695-119">A handle to a loaded module that implements a software driver (such as D3D10Ref.dll).</span></span> <span data-ttu-id="15695-120">Zum Abrufen eines Handles aufrufen Sie die [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="15695-120">To get a handle, call the [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

</dd> <dt>

<span data-ttu-id="15695-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="15695-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15695-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15695-123">Geräteerstellungsflags (siehe [**d3d10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) Enumeration) zum Aktivieren von API- [Ebenen](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="15695-123">Device creation flags (see the [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) enumeration) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="15695-124">Diese Flags können bitweise oder gleich sein.</span><span class="sxs-lookup"><span data-stu-id="15695-124">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="15695-125">*ppdevice* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="15695-125">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15695-126">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="15695-126">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="15695-127">Adresse eines Zeigers auf das erstellte Gerät (siehe die [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="15695-127">Address of a pointer to the device created (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15695-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15695-128">Return value</span></span>

<span data-ttu-id="15695-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15695-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15695-130">Diese Funktion gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="15695-130">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15695-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15695-131">Remarks</span></span>

<span data-ttu-id="15695-132">Diese Funktion versucht, das beste Gerät für die Hardware zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15695-132">This function attempts to create the best device for the hardware.</span></span> <span data-ttu-id="15695-133">Zuerst versucht die Funktion, ein 10,1-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15695-133">First, the function attempts to create a 10.1 device.</span></span> <span data-ttu-id="15695-134">Wenn ein 10,1-Gerät nicht erstellt werden kann, versucht die Funktion, ein 10,0-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15695-134">If a 10.1 device cannot be created, the function attempts to create a 10.0 device.</span></span> <span data-ttu-id="15695-135">Wenn keines der Geräte erfolgreich erstellt wurde, gibt die Funktion E \_ Fail zurück.</span><span class="sxs-lookup"><span data-stu-id="15695-135">If neither device is successfully created, the function returns E\_FAIL.</span></span>

<span data-ttu-id="15695-136">Wenn Ihre Anwendung nur ein 10,1-Gerät oder nur ein 10,0-Gerät erstellen muss, verwenden Sie stattdessen die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="15695-136">If your application needs to create only a 10.1 device, or a 10.0 device only, use the following functions instead:</span></span>

-   <span data-ttu-id="15695-137">Verwenden Sie die [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) -Funktion, um nur ein Direct3D 10,0-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15695-137">Use the [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) function to create a Direct3D 10.0 device only.</span></span>
-   <span data-ttu-id="15695-138">Verwenden Sie die [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) -Funktion, um nur ein Direct3D 10,1-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15695-138">Use the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function to create a Direct3D 10.1 device only.</span></span>
-   <span data-ttu-id="15695-139">Verwenden Sie die [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) -Funktion, um einen [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) -Schnittstellen Zeiger von einem [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Schnittstellen Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15695-139">Use the [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) function to get an [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface pointer from an [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface pointer.</span></span>

<span data-ttu-id="15695-140">Ein Direct3D 10,1-Gerät kann nur auf Computern erstellt werden, auf denen Windows Vista Service Pack 1 oder höher ausgeführt wird, und auf denen Direct3D 10,1-kompatible Hardware installiert ist.</span><span class="sxs-lookup"><span data-stu-id="15695-140">A Direct3D 10.1 device can only be created on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="15695-141">Es ist jedoch zulässig, diese Funktion auf Computern mit einer beliebigen Windows-Version aufzurufen, auf der die d3dx10-dll installiert ist.</span><span class="sxs-lookup"><span data-stu-id="15695-141">However, it is legal to call this function on computers running any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="15695-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15695-142">Requirements</span></span>



| <span data-ttu-id="15695-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15695-143">Requirement</span></span> | <span data-ttu-id="15695-144">Wert</span><span class="sxs-lookup"><span data-stu-id="15695-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15695-145">Header</span><span class="sxs-lookup"><span data-stu-id="15695-145">Header</span></span><br/> | <dl> <span data-ttu-id="15695-146"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="15695-146"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15695-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15695-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15695-148">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="15695-148">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
