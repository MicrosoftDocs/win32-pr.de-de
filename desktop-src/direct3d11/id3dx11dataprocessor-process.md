---
title: ID3DX11DataProcessor Process-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Verarbeitet Daten.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Prozess Methode Direct3D 11
- Process Method Direct3D 11, ID3DX11DataProcessor Interface
- ID3DX11DataProcessor-Schnittstelle Direct3D 11, Prozess Methode
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530950"
---
# <a name="id3dx11dataprocessorprocess-method"></a><span data-ttu-id="aafac-107">ID3DX11DataProcessor::P rocess-Methode</span><span class="sxs-lookup"><span data-stu-id="aafac-107">ID3DX11DataProcessor::Process method</span></span>

> [!Note]  
> <span data-ttu-id="aafac-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aafac-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="aafac-109">Verarbeitet Daten.</span><span class="sxs-lookup"><span data-stu-id="aafac-109">Processes data.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafac-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="aafac-110">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="aafac-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="aafac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aafac-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aafac-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aafac-113">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="aafac-113">Type: **void\***</span></span>

<span data-ttu-id="aafac-114">Zeiger auf die zu verarbeitenden Daten.</span><span class="sxs-lookup"><span data-stu-id="aafac-114">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="aafac-115">*cbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aafac-115">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aafac-116">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="aafac-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="aafac-117">Die Größe der zu verarbeitenden Daten.</span><span class="sxs-lookup"><span data-stu-id="aafac-117">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aafac-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aafac-118">Return value</span></span>

<span data-ttu-id="aafac-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aafac-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aafac-120">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="aafac-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aafac-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aafac-121">Remarks</span></span>

<span data-ttu-id="aafac-122">Diese Methode wird von einer [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="aafac-122">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aafac-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aafac-123">Requirements</span></span>



| <span data-ttu-id="aafac-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aafac-124">Requirement</span></span> | <span data-ttu-id="aafac-125">Wert</span><span class="sxs-lookup"><span data-stu-id="aafac-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aafac-126">Header</span><span class="sxs-lookup"><span data-stu-id="aafac-126">Header</span></span><br/>  | <dl> <span data-ttu-id="aafac-127"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="aafac-127"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="aafac-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aafac-128">Library</span></span><br/> | <dl> <span data-ttu-id="aafac-129"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aafac-129"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aafac-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aafac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aafac-131">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="aafac-131">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="aafac-132">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="aafac-132">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

