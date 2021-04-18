---
description: Eine Beschreibung des aktuellen Schriftart Objekts erhalten.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font:: getdesc-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365117"
---
# <a name="id3dx10fontgetdesc-method"></a><span data-ttu-id="a8c83-103">ID3DX10Font:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="a8c83-103">ID3DX10Font::GetDesc method</span></span>

<span data-ttu-id="a8c83-104">Eine Beschreibung des aktuellen Schriftart Objekts erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8c83-104">Get a description of the current font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c83-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8c83-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a8c83-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8c83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c83-107">*PDE SC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8c83-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c83-108">Type: **[ **d3dx10 \_ Font \_ DESC**](d3dx10-font-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8c83-108">Type: **[**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="a8c83-109">Zeiger auf eine [**d3dx10 \_ Font \_**](d3dx10-font-desc.md) -Debug-Struktur, die das Schriftart Objekt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a8c83-109">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure that describes the font object.</span></span> <span data-ttu-id="a8c83-110">Wenn Unicode definiert ist, wird ein Zeiger auf einen D3DX10FONT- \_ descw zurückgegeben; andernfalls wird ein Zeiger auf einen D3DX10FONT \_ DeScA zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8c83-110">If UNICODE is defined, a pointer to a D3DX10FONT\_DESCW is returned; otherwise a pointer to a D3DX10FONT\_DESCA is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c83-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8c83-111">Return value</span></span>

<span data-ttu-id="a8c83-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8c83-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8c83-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8c83-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a8c83-114">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="a8c83-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8c83-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8c83-115">Remarks</span></span>

<span data-ttu-id="a8c83-116">Diese Methode beschreibt Unicode-Schriftart Objekte, wenn Unicode definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a8c83-116">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="a8c83-117">Andernfalls wird getdesca aufgerufen, wodurch ein Zeiger auf die D3DX10FONT DeScA-Struktur zurückgegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="a8c83-117">Otherwise GetDescA is called, which returns a pointer to the D3DX10FONT\_DESCA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c83-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8c83-118">Requirements</span></span>



| <span data-ttu-id="a8c83-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8c83-119">Requirement</span></span> | <span data-ttu-id="a8c83-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a8c83-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c83-121">Header</span><span class="sxs-lookup"><span data-stu-id="a8c83-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a8c83-122"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8c83-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8c83-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8c83-123">Library</span></span><br/> | <dl> <span data-ttu-id="a8c83-124"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8c83-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c83-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8c83-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c83-126">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="a8c83-126">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="a8c83-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a8c83-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




