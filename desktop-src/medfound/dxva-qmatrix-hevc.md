---
description: Definiert eine quantisierungsmatrix.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC-Struktur (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524547"
---
# <a name="dxva_qmatrix_hevc-structure"></a><span data-ttu-id="484c2-103">DXVA- \_ QMatrix \_ hevc-Struktur</span><span class="sxs-lookup"><span data-stu-id="484c2-103">DXVA\_Qmatrix\_HEVC structure</span></span>

<span data-ttu-id="484c2-104">Definiert eine quantisierungsmatrix.</span><span class="sxs-lookup"><span data-stu-id="484c2-104">Defines a quantization matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="484c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="484c2-105">Syntax</span></span>


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a><span data-ttu-id="484c2-106">Member</span><span class="sxs-lookup"><span data-stu-id="484c2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="484c2-107">**ucScalingLists0 \[ 6 \] \[ 16\]**</span><span class="sxs-lookup"><span data-stu-id="484c2-107">**ucScalingLists0\[6\]\[16\]**</span></span>
</dt> <dd>

<span data-ttu-id="484c2-108">Enthält die Skalierungs Listen für den 4 x 4-Skalierungs Prozess entsprechend der skinglist \[ 0 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich von 0 bis 5 (einschließlich) liegt, und ich liegt im Bereich von 0 bis 15 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="484c2-108">Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList\[ 0 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="484c2-109">**ucScalingLists1 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="484c2-109">**ucScalingLists1\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="484c2-110">Enthält die Skalierungs Listen für den 8x8-Skalierungs Prozess entsprechend der skinglist \[ 1 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich von 0 bis 5 (einschließlich) liegt, und ich liegt im Bereich von 0 bis 63 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="484c2-110">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 1 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="484c2-111">**ucScalingLists2 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="484c2-111">**ucScalingLists2\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="484c2-112">Enthält die Skalierungs Listen für den 8x8-Skalierungs Prozess entsprechend der skinglist \[ 2 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich von 0 bis 5 (einschließlich) liegt, und ich liegt im Bereich von 0 bis 63 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="484c2-112">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 2 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="484c2-113">**ucScalingLists3 \[ 2 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="484c2-113">**ucScalingLists3\[2\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="484c2-114">Enthält die Skalierungs Listen für den 8x8-Skalierungs Prozess entsprechend der skinglist \[ 3 \] \[ MatrixID \] \[ i \] in der hevc-Spezifikation, wobei MatrixID im Bereich zwischen 0 und 1 (einschließlich) liegt. der Bereich liegt zwischen 0 und 63 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="484c2-114">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 3 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="484c2-115">**ucScalingListDCCoefSizeID2**</span><span class="sxs-lookup"><span data-stu-id="484c2-115">**ucScalingListDCCoefSizeID2**</span></span>
</dt> <dd>

<span data-ttu-id="484c2-116">Enthält den DC-Wert der Skalierungs Liste für die 16x16-Größe mit der sizeid gleich 2 und entspricht der Skalierungs \_ Liste \_ DC \_ coef \_ Minus8 \[ sizeid − 2 \] \[ MatrixID \] + 8 mit sizeid ist gleich 2 und MatrixID im Bereich von 0 bis 5 (einschließlich) in der hevc-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="484c2-116">Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification.</span></span>

</dd> <dt>

<span data-ttu-id="484c2-117">**ucScalingListDCCoefSizeID3**</span><span class="sxs-lookup"><span data-stu-id="484c2-117">**ucScalingListDCCoefSizeID3**</span></span>
</dt> <dd>

<span data-ttu-id="484c2-118">Enthält den DC-Wert der Skalierungs Liste für die Größe 32x32 mit sizeid gleich 3 und entspricht dem Skalierungs \_ Listen- \_ DC \_ coef \_ Minus8 \[ sizeid − 2 \] \[ MatrixID \] + 8 mit sizeid, gleich 3 und MatrixID im Bereich von 0 bis 1 (einschließlich) in der hevc-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="484c2-118">Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="484c2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="484c2-119">Requirements</span></span>



| <span data-ttu-id="484c2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="484c2-120">Requirement</span></span> | <span data-ttu-id="484c2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="484c2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="484c2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="484c2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="484c2-123">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="484c2-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="484c2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="484c2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="484c2-125">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="484c2-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="484c2-126">Header</span><span class="sxs-lookup"><span data-stu-id="484c2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="484c2-127"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="484c2-127"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="484c2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="484c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="484c2-129">Media Foundation Strukturen</span><span class="sxs-lookup"><span data-stu-id="484c2-129">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




