---
title: ID3DX11DataLoader DECOMPRESS-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Decodiert codierte Daten.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- DECOMPRESS-Methode Direct3D 11
- DECOMPRESS-Methode Direct3D 11, ID3DX11DataLoader-Schnittstelle
- ID3DX11DataLoader Interface Direct3D 11, DECOMPRESS-Methode
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961760"
---
# <a name="id3dx11dataloaderdecompress-method"></a><span data-ttu-id="36fcf-107">ID3DX11DataLoader::D eComPress-Methode</span><span class="sxs-lookup"><span data-stu-id="36fcf-107">ID3DX11DataLoader::Decompress method</span></span>

> [!Note]  
> <span data-ttu-id="36fcf-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36fcf-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="36fcf-109">Decodiert codierte Daten.</span><span class="sxs-lookup"><span data-stu-id="36fcf-109">Decompresses encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="36fcf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="36fcf-110">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="36fcf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="36fcf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36fcf-112">*ppData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36fcf-112">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36fcf-113">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="36fcf-113">Type: **void\*\***</span></span>

<span data-ttu-id="36fcf-114">Zeiger auf die zu entkomprimierenden Rohdaten.</span><span class="sxs-lookup"><span data-stu-id="36fcf-114">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="36fcf-115">*pcbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36fcf-115">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36fcf-116">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="36fcf-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="36fcf-117">Die Größe der Daten, auf die von ppData verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="36fcf-117">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36fcf-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36fcf-118">Return value</span></span>

<span data-ttu-id="36fcf-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36fcf-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36fcf-120">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="36fcf-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="36fcf-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36fcf-121">Remarks</span></span>

<span data-ttu-id="36fcf-122">Verwenden Sie diese Methode, um Ressourcen aus Dateisystemen (z. b. zip-Dateien) zu laden.</span><span class="sxs-lookup"><span data-stu-id="36fcf-122">Use this method to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="36fcf-123">Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="36fcf-123">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

<span data-ttu-id="36fcf-124">Die [**ID3DX11DataLoader-Schnittstelle**](id3dx11dataloader.md) kann geerbt werden, und die zugehörigen Member werden neu definiert, um benutzerdefinierte Dateiformate</span><span class="sxs-lookup"><span data-stu-id="36fcf-124">[**ID3DX11DataLoader Interface**](id3dx11dataloader.md) can be inherited and its members redefined to support custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fcf-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="36fcf-125">Requirements</span></span>



| <span data-ttu-id="36fcf-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36fcf-126">Requirement</span></span> | <span data-ttu-id="36fcf-127">Wert</span><span class="sxs-lookup"><span data-stu-id="36fcf-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36fcf-128">Header</span><span class="sxs-lookup"><span data-stu-id="36fcf-128">Header</span></span><br/>  | <dl> <span data-ttu-id="36fcf-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="36fcf-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="36fcf-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="36fcf-130">Library</span></span><br/> | <dl> <span data-ttu-id="36fcf-131"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36fcf-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36fcf-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="36fcf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36fcf-133">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="36fcf-133">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="36fcf-134">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="36fcf-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

