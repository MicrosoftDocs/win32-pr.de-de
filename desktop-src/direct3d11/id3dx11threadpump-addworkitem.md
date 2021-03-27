---
title: ID3DX11ThreadPump addworkitem-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Fügt der Thread Pumpe ein Arbeits Element hinzu.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Addworkitem-Methode Direct3D 11
- Addworkitem-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump Interface Direct3D 11, addworkitem-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354276"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a><span data-ttu-id="a131b-107">ID3DX11ThreadPump:: addworkitem-Methode</span><span class="sxs-lookup"><span data-stu-id="a131b-107">ID3DX11ThreadPump::AddWorkItem method</span></span>

> [!Note]  
> <span data-ttu-id="a131b-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a131b-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="a131b-109">Fügt der Thread Pumpe ein Arbeits Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="a131b-109">Adds a work item to the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="a131b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a131b-110">Syntax</span></span>


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a><span data-ttu-id="a131b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a131b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a131b-112">*pdataloader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a131b-112">*pDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a131b-113">Typ: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***</span><span class="sxs-lookup"><span data-stu-id="a131b-113">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\***</span></span>

<span data-ttu-id="a131b-114">Das Lade Modul, das vom threadpump verwendet wird, wenn ein Arbeits Element zum Laden von Daten benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a131b-114">The loader that the thread pump will use when a work item requires data to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a131b-115">*pdataprocessor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a131b-115">*pDataProcessor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a131b-116">Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span><span class="sxs-lookup"><span data-stu-id="a131b-116">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***</span></span>

<span data-ttu-id="a131b-117">Der Prozessor, den das Thread-Pump-Element verwendet, wenn für eine Arbeitsaufgabe die Verarbeitung von Daten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a131b-117">The processor that the thread pump will use when a work item requires data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="a131b-118">*phresult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a131b-118">*pHResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a131b-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a131b-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a131b-120">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a131b-120">A pointer to the return value.</span></span> <span data-ttu-id="a131b-121">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a131b-121">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a131b-122">*ppdeviceobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a131b-122">*ppDeviceObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a131b-123">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="a131b-123">Type: **void\*\***</span></span>

<span data-ttu-id="a131b-124">Das Gerät, von dem das-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a131b-124">The device that uses the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a131b-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a131b-125">Return value</span></span>

<span data-ttu-id="a131b-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a131b-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a131b-127">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a131b-127">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a131b-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a131b-128">Requirements</span></span>



| <span data-ttu-id="a131b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a131b-129">Requirement</span></span> | <span data-ttu-id="a131b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a131b-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a131b-131">Header</span><span class="sxs-lookup"><span data-stu-id="a131b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a131b-132"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a131b-132"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="a131b-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a131b-133">Library</span></span><br/> | <dl> <span data-ttu-id="a131b-134"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a131b-134"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a131b-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a131b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a131b-136">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="a131b-136">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="a131b-137">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a131b-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





