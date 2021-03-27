---
title: D3DX11CreateThreadPump-Funktion (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen Sie ein Thread-Pump.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- D3DX11CreateThreadPump-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982336"
---
# <a name="d3dx11createthreadpump-function"></a><span data-ttu-id="9d284-106">D3DX11CreateThreadPump-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d284-106">D3DX11CreateThreadPump function</span></span>

> [!Note]  
> <span data-ttu-id="9d284-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9d284-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9d284-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9d284-108">See Remarks.</span></span>

 

<span data-ttu-id="9d284-109">Erstellen Sie ein Thread-Pump.</span><span class="sxs-lookup"><span data-stu-id="9d284-109">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d284-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d284-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="9d284-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d284-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d284-112">*ciothreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d284-112">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d284-113">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9d284-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9d284-114">Die Anzahl der zu erstellenden e/a-Threads.</span><span class="sxs-lookup"><span data-stu-id="9d284-114">The number of I/O threads to create.</span></span> <span data-ttu-id="9d284-115">Wenn 0 angegeben wird, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9d284-115">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="9d284-116">*cprocthreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d284-116">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d284-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9d284-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9d284-118">Die Anzahl der zu erstellenden Prozessthreads.</span><span class="sxs-lookup"><span data-stu-id="9d284-118">The number of process threads to create.</span></span> <span data-ttu-id="9d284-119">Wenn 0 angegeben wird, versucht Direct3D, die optimale Anzahl von Threads basierend auf der Hardwarekonfiguration zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9d284-119">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="9d284-120">*ppthreadpump* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9d284-120">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d284-121">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9d284-121">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span></span>

<span data-ttu-id="9d284-122">Die erstellte Thread-Pump.</span><span class="sxs-lookup"><span data-stu-id="9d284-122">The created thread pump.</span></span> <span data-ttu-id="9d284-123">Siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="9d284-123">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d284-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d284-124">Return value</span></span>

<span data-ttu-id="9d284-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d284-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d284-126">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="9d284-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d284-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d284-127">Remarks</span></span>

<span data-ttu-id="9d284-128">Ein Thread Pump ist ein sehr Ressourcen intensives Objekt.</span><span class="sxs-lookup"><span data-stu-id="9d284-128">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="9d284-129">Pro Anwendung sollte nur ein Thread Pump erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9d284-129">Only one thread pump should be created per application.</span></span>

<span data-ttu-id="9d284-130">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="9d284-130">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="9d284-131">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d284-131">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="9d284-132">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9d284-132">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d284-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9d284-133">Requirements</span></span>



| <span data-ttu-id="9d284-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d284-134">Requirement</span></span> | <span data-ttu-id="9d284-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9d284-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d284-136">Header</span><span class="sxs-lookup"><span data-stu-id="9d284-136">Header</span></span><br/>  | <dl> <span data-ttu-id="9d284-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d284-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="9d284-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d284-138">Library</span></span><br/> | <dl> <span data-ttu-id="9d284-139"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d284-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d284-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9d284-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d284-141">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9d284-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

