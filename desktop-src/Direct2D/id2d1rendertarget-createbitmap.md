---
title: ID2D1RenderTarget-Methoden
description: Erstellt eine Direct2D-Bitmap.
ms.assetid: b45d353f-ae33-4110-b7c8-f14661017e0f
keywords:
- Methoden der Methode "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4576b9111d9180b395527bad8b06ee3f9a8eef2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373853"
---
# <a name="id2d1rendertargetcreatebitmap-methods"></a><span data-ttu-id="69c90-104">ID2D1RenderTarget:: kreatebitmap-Methoden</span><span class="sxs-lookup"><span data-stu-id="69c90-104">ID2D1RenderTarget::CreateBitmap methods</span></span>

<span data-ttu-id="69c90-105">Erstellt eine Direct2D-Bitmap.</span><span class="sxs-lookup"><span data-stu-id="69c90-105">Creates a Direct2D bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="69c90-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="69c90-106">Overload list</span></span>



| <span data-ttu-id="69c90-107">Methode</span><span class="sxs-lookup"><span data-stu-id="69c90-107">Method</span></span>                                                                                                                                                                                                   | <span data-ttu-id="69c90-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69c90-108">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="69c90-109">[**"Kreatebitmap" (D2D1 \_ size \_ U, D2D1 \_ Bitmap \_ Properties&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="69c90-109">[**CreateBitmap(D2D1\_SIZE\_U,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span>                                | <span data-ttu-id="69c90-110">Erstellt eine nicht initialisierte Direct2D-Bitmap.</span><span class="sxs-lookup"><span data-stu-id="69c90-110">Creates an uninitialized Direct2D bitmap.</span></span> <br/>                          |
| <span data-ttu-id="69c90-111">[**"Kreatebitmap" (D2D1 \_ size \_ U, void \* , UInt32, D2D1 \_ Bitmap \_ Properties \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="69c90-111">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES\*,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap))</span></span> | <span data-ttu-id="69c90-112">Erstellt eine Direct2D-Bitmap aus einem Zeiger auf in-Memory-Quelldaten.</span><span class="sxs-lookup"><span data-stu-id="69c90-112">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span><br/>  |
| <span data-ttu-id="69c90-113">[**"Kreatebitmap" (D2D1 \_ size \_ U, void \* , UInt32, D2D1 \_ Bitmap \_ Properties&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span><span class="sxs-lookup"><span data-stu-id="69c90-113">[**CreateBitmap(D2D1\_SIZE\_U,void\*,UINT32,D2D1\_BITMAP\_PROPERTIES&,ID2D1Bitmap\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties__id2d1bitmap))</span></span>  | <span data-ttu-id="69c90-114">Erstellt eine Direct2D-Bitmap aus einem Zeiger auf in-Memory-Quelldaten.</span><span class="sxs-lookup"><span data-stu-id="69c90-114">Creates a Direct2D bitmap from a pointer to in-memory source data.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="69c90-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69c90-115">Requirements</span></span>



| <span data-ttu-id="69c90-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69c90-116">Requirement</span></span> | <span data-ttu-id="69c90-117">Wert</span><span class="sxs-lookup"><span data-stu-id="69c90-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="69c90-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="69c90-118">Library</span></span><br/> | <dl> <span data-ttu-id="69c90-119"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69c90-119"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="69c90-120">DLL</span><span class="sxs-lookup"><span data-stu-id="69c90-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="69c90-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69c90-121"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c90-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69c90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c90-123">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="69c90-123">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

