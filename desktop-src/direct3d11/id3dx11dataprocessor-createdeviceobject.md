---
title: ID3DX11DataProcessor kreatedeviceobject-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Erstellt ein Geräte Objekt.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Kreatedeviceobject-Methode Direct3D 11
- Methode Direct3D 11, ID3DX11DataProcessor Interface
- ID3DX11DataProcessor Interface Direct3D 11, Methode "kreatedeviceobject"
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356036"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="b44a6-107">ID3DX11DataProcessor:: kreatedeviceobject-Methode</span><span class="sxs-lookup"><span data-stu-id="b44a6-107">ID3DX11DataProcessor::CreateDeviceObject method</span></span>

> [!Note]  
> <span data-ttu-id="b44a6-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b44a6-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="b44a6-109">Erstellt ein Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="b44a6-109">Creates a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b44a6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b44a6-110">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="b44a6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b44a6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b44a6-112">*ppdataobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b44a6-112">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b44a6-113">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="b44a6-113">Type: **void\*\***</span></span>

<span data-ttu-id="b44a6-114">Adresse eines Zeigers auf das erstellte Geräte Objekt.</span><span class="sxs-lookup"><span data-stu-id="b44a6-114">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b44a6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b44a6-115">Return value</span></span>

<span data-ttu-id="b44a6-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b44a6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b44a6-117">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="b44a6-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b44a6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b44a6-118">Remarks</span></span>

<span data-ttu-id="b44a6-119">Diese Methode wird von einer [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="b44a6-119">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b44a6-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b44a6-120">Requirements</span></span>



| <span data-ttu-id="b44a6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b44a6-121">Requirement</span></span> | <span data-ttu-id="b44a6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b44a6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b44a6-123">Header</span><span class="sxs-lookup"><span data-stu-id="b44a6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b44a6-124"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b44a6-124"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="b44a6-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b44a6-125">Library</span></span><br/> | <dl> <span data-ttu-id="b44a6-126"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b44a6-126"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b44a6-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b44a6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44a6-128">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="b44a6-128">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="b44a6-129">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b44a6-129">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





