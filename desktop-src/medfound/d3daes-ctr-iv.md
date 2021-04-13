---
description: Enthält einen Initialisierungs Vektor (IV) für 128-Bit-Advanced Encryption Standard CTR-Modus (AES-CTR) Blockchiffre Verschlüsselung.
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: D3DAES_CTR_IV-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342539"
---
# <a name="d3daes_ctr_iv-structure"></a><span data-ttu-id="53219-103">D3DAES \_ CTR- \_ IV-Struktur</span><span class="sxs-lookup"><span data-stu-id="53219-103">D3DAES\_CTR\_IV structure</span></span>

<span data-ttu-id="53219-104">Enthält einen Initialisierungs Vektor (IV) für 128-Bit-Advanced Encryption Standard CTR-Modus (AES-CTR) Blockchiffre Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="53219-104">Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="53219-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53219-105">Syntax</span></span>


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a><span data-ttu-id="53219-106">Member</span><span class="sxs-lookup"><span data-stu-id="53219-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53219-107">**IV**</span><span class="sxs-lookup"><span data-stu-id="53219-107">**IV**</span></span>
</dt> <dd>

<span data-ttu-id="53219-108">Der IV im Big-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="53219-108">The IV, in big-endian format.</span></span>

</dd> <dt>

<span data-ttu-id="53219-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="53219-109">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="53219-110">Die Block Anzahl im Big-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="53219-110">The block count, in big-endian format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53219-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53219-111">Remarks</span></span>

<span data-ttu-id="53219-112">Die **D3DAES \_ CTR \_ IV** -Struktur und die [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) -Struktur sind gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="53219-112">The **D3DAES\_CTR\_IV** structure and the [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) structure are equivalent.</span></span>

<span data-ttu-id="53219-113">Weitere Informationen finden Sie unter [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span><span class="sxs-lookup"><span data-stu-id="53219-113">For details, see [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span></span>

## <a name="requirements"></a><span data-ttu-id="53219-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53219-114">Requirements</span></span>



| <span data-ttu-id="53219-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53219-115">Requirement</span></span> | <span data-ttu-id="53219-116">Wert</span><span class="sxs-lookup"><span data-stu-id="53219-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53219-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53219-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53219-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53219-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="53219-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53219-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53219-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53219-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53219-121">Header</span><span class="sxs-lookup"><span data-stu-id="53219-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="53219-122"><dt>D3d9types. h (Include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53219-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53219-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53219-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53219-124">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="53219-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




