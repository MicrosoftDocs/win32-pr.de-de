---
description: Wird verwendet, um codierte Daten zu decodieren. Dies wird in der Regel zum Laden von Ressourcen aus Dateisystemen wie ZIP-Dateien verwendet. Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: ID3DX10DataLoader::D eComPress-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373518"
---
# <a name="id3dx10dataloaderdecompress-method"></a><span data-ttu-id="af12f-105">ID3DX10DataLoader::D eComPress-Methode</span><span class="sxs-lookup"><span data-stu-id="af12f-105">ID3DX10DataLoader::Decompress method</span></span>

<span data-ttu-id="af12f-106">Wird verwendet, um codierte Daten zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="af12f-106">Used to decompress encoded data.</span></span> <span data-ttu-id="af12f-107">Dies wird in der Regel zum Laden von Ressourcen aus Dateisystemen wie ZIP-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="af12f-107">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="af12f-108">Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af12f-108">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

## <a name="syntax"></a><span data-ttu-id="af12f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="af12f-109">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="af12f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="af12f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af12f-111">*ppData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="af12f-111">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af12f-112">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="af12f-112">Type: **void\*\***</span></span>

<span data-ttu-id="af12f-113">Zeiger auf die zu entkomprimierenden Rohdaten.</span><span class="sxs-lookup"><span data-stu-id="af12f-113">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="af12f-114">*pcbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af12f-114">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af12f-115">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="af12f-115">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="af12f-116">Die Größe der Daten, auf die von ppData verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="af12f-116">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af12f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af12f-117">Return value</span></span>

<span data-ttu-id="af12f-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af12f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af12f-119">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="af12f-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af12f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af12f-120">Remarks</span></span>

<span data-ttu-id="af12f-121">Die [**ID3DX10DataLoader-Schnittstelle**](id3dx10dataloader.md) kann geerbt und deren Member neu definiert werden.</span><span class="sxs-lookup"><span data-stu-id="af12f-121">[**ID3DX10DataLoader Interface**](id3dx10dataloader.md) can be inherited and its members redefined.</span></span> <span data-ttu-id="af12f-122">DECOMPRESS konnte neu definiert werden, um Ihre eigenen benutzerdefinierten Dateiformate zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="af12f-122">Decompress could be redefined to support your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="af12f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af12f-123">Requirements</span></span>



| <span data-ttu-id="af12f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af12f-124">Requirement</span></span> | <span data-ttu-id="af12f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="af12f-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af12f-126">Header</span><span class="sxs-lookup"><span data-stu-id="af12f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="af12f-127"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="af12f-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="af12f-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="af12f-128">Library</span></span><br/> | <dl> <span data-ttu-id="af12f-129"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af12f-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af12f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af12f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af12f-131">ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="af12f-131">ID3DX10DataLoader</span></span>](id3dx10dataloader.md)
</dt> <dt>

[<span data-ttu-id="af12f-132">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="af12f-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
