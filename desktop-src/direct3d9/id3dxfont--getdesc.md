---
description: Ruft eine Beschreibung des aktuellen Schriftart Objekts ab. Getdescw und getdesca sind mit dieser Methode identisch, mit dem Unterschied, dass ein Zeiger an eine D3DXFONT- \_ oder D3DXFONT-DeScA-Struktur zurückgegeben wird \_ .
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont:: getdesc-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355806"
---
# <a name="id3dxfontgetdesc-method"></a><span data-ttu-id="983a5-104">ID3DXFont:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="983a5-104">ID3DXFont::GetDesc method</span></span>

<span data-ttu-id="983a5-105">Ruft eine Beschreibung des aktuellen Schriftart Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="983a5-105">Gets a description of the current font object.</span></span> <span data-ttu-id="983a5-106">Getdescw und getdesca sind mit dieser Methode identisch, mit dem Unterschied, dass ein Zeiger an eine [**D3DXFONT \_**](d3dxfont-desc.md) -oder **D3DXFONT- \_ DeScA** -Struktur zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="983a5-106">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="983a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="983a5-107">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="983a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="983a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="983a5-109">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="983a5-109">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="983a5-110">Typ: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="983a5-110">Type: **[**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="983a5-111">Zeiger auf eine [**D3DXFONT \_**](d3dxfont-desc.md) -Struktur, die das Schriftart Objekt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="983a5-111">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure that describes the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="983a5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="983a5-112">Return value</span></span>

<span data-ttu-id="983a5-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="983a5-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="983a5-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="983a5-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="983a5-115">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="983a5-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="983a5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="983a5-116">Remarks</span></span>

<span data-ttu-id="983a5-117">Diese Methode beschreibt Unicode-Schriftart Objekte, wenn Unicode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="983a5-117">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="983a5-118">Andernfalls wird getdesca aufgerufen, wodurch ein Zeiger auf die [**D3DXFONT \_ DeScA**](d3dxfont-desc.md) -Struktur zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="983a5-118">Otherwise GetDescA is called, which returns a pointer to the [**D3DXFONT\_DESCA**](d3dxfont-desc.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="983a5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="983a5-119">Requirements</span></span>



| <span data-ttu-id="983a5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="983a5-120">Requirement</span></span> | <span data-ttu-id="983a5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="983a5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="983a5-122">Header</span><span class="sxs-lookup"><span data-stu-id="983a5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="983a5-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="983a5-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="983a5-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="983a5-124">Library</span></span><br/> | <dl> <span data-ttu-id="983a5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="983a5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="983a5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="983a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983a5-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="983a5-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




