---
title: GXFPF_ Konstanten (textstor. h)
description: Gxfpf \_ \ Konstanten geben die zurück zugebende Zeichenposition basierend auf den Bildschirm Koordinaten des Punkts relativ zu einem umgebenden Zeichen an.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475813"
---
# <a name="gxfpf_-constants"></a><span data-ttu-id="e4df5-103">Gxfpf- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="e4df5-103">GXFPF\_\* Constants</span></span>

<span data-ttu-id="e4df5-104">Gxfpf- \_ \* Konstanten geben die zurück zugebende Zeichenposition basierend auf den Bildschirm Koordinaten des Punkts relativ zu einem umgebenden Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="e4df5-104">GXFPF\_\* constants specify the character position to return based on the screen coordinates of the point relative to a character bounding box.</span></span>



| <span data-ttu-id="e4df5-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="e4df5-105">Constant/value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="e4df5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4df5-106">Description</span></span>                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <span data-ttu-id="e4df5-107"><dt>**Gxfpf \_ Round am \_ nächsten**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e4df5-107"><dt>**GXFPF\_ROUND\_NEAREST**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="e4df5-108">Wenn die Bildschirm Koordinaten des Punkts in einem umgebenden Feld für Zeichen enthalten sind, ist die zurückgegebene Zeichenposition der umgebende Rand, der den Bildschirm Koordinaten des Punkts am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="e4df5-108">If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.</span></span><br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <span data-ttu-id="e4df5-109"><dt>**Gxfpf \_ Nächstgelegene**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="e4df5-109"><dt>**GXFPF\_NEAREST**</dt> <dt>( 0x2 )</dt></span></span> </dl>                    | <span data-ttu-id="e4df5-110">Wenn die Bildschirm Koordinaten des Punkts nicht in einem umgebenden Feld für das Zeichen enthalten sind, wird die nächstgelegene Zeichenposition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4df5-110">If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.</span></span><br/>                                                      |



## <a name="remarks"></a><span data-ttu-id="e4df5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4df5-111">Remarks</span></span>

<span data-ttu-id="e4df5-112">Die *dwFlags* -Parameter der Methoden [ITextStoreACP:: getacpfrompoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) und [ITF contextowner:: getacpfrompoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) verwenden diese Konstanten.</span><span class="sxs-lookup"><span data-stu-id="e4df5-112">The *dwflags* parameters of the [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) and [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) methods use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4df5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4df5-113">Requirements</span></span>



| <span data-ttu-id="e4df5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4df5-114">Requirement</span></span> | <span data-ttu-id="e4df5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e4df5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4df5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4df5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e4df5-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4df5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e4df5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4df5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e4df5-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4df5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4df5-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e4df5-120">Redistributable</span></span><br/>          | <span data-ttu-id="e4df5-121">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e4df5-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="e4df5-122">Header</span><span class="sxs-lookup"><span data-stu-id="e4df5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4df5-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4df5-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4df5-124">IDL</span><span class="sxs-lookup"><span data-stu-id="e4df5-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4df5-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4df5-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4df5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4df5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4df5-127">ITextStoreACP:: getacpfrompoint</span><span class="sxs-lookup"><span data-stu-id="e4df5-127">ITextStoreACP::GetACPFromPoint</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[<span data-ttu-id="e4df5-128">ITF contextowner:: getacpfrompoint</span><span class="sxs-lookup"><span data-stu-id="e4df5-128">ITfContextOwner::GetACPFromPoint</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





