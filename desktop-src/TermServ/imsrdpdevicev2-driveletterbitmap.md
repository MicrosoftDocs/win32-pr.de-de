---
title: IMsRdpDeviceV2 driveletterbitmap (Eigenschaft)
description: Enthält ein Bitfeld, das eine Zuordnung der im Gerät enthaltenen Laufwerk Buchstaben darstellt.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Driveletterbitmap-Eigenschaft Remotedesktopdienste
- Driveletterbitmap-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2 Interface Remotedesktopdienste, driveletterbitmap (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739993"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a><span data-ttu-id="77df3-106">IMsRdpDeviceV2::D riveletterbitmap-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="77df3-106">IMsRdpDeviceV2::DriveLetterBitmap property</span></span>

<span data-ttu-id="77df3-107">Enthält ein Bitfeld, das eine Zuordnung der im Gerät enthaltenen Laufwerk Buchstaben darstellt.</span><span class="sxs-lookup"><span data-stu-id="77df3-107">Contains a bitfield that represents a map of drive letters contained within the device.</span></span>

<span data-ttu-id="77df3-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="77df3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="77df3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="77df3-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="77df3-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="77df3-110">Property value</span></span>

<span data-ttu-id="77df3-111">Eine Zuordnung von Laufwerk Buchstaben, die im Gerät enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="77df3-111">A map of drive letters contained within the device.</span></span> <span data-ttu-id="77df3-112">Jedes Bit im Wert stellt einen Laufwerk Buchstaben dar.</span><span class="sxs-lookup"><span data-stu-id="77df3-112">Each bit in the value represents a drive letter.</span></span> <span data-ttu-id="77df3-113">Das unwichtigste Bit stellt den Laufwerk Buchstaben "a" dar, das nächste Bit stellt den Laufwerk Buchstaben "B" dar usw.</span><span class="sxs-lookup"><span data-stu-id="77df3-113">The least significant bit represents drive letter "A", the next bit represents drive letter "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="77df3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77df3-114">Requirements</span></span>



| <span data-ttu-id="77df3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77df3-115">Requirement</span></span> | <span data-ttu-id="77df3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="77df3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77df3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77df3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="77df3-118">Windows 7 mit SP1</span><span class="sxs-lookup"><span data-stu-id="77df3-118">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="77df3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77df3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="77df3-120">Windows Server 2008 R2 mit SP1</span><span class="sxs-lookup"><span data-stu-id="77df3-120">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="77df3-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="77df3-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="77df3-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77df3-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="77df3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="77df3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77df3-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77df3-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="77df3-125">IID</span><span class="sxs-lookup"><span data-stu-id="77df3-125">IID</span></span><br/>                      | <span data-ttu-id="77df3-126">IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.</span><span class="sxs-lookup"><span data-stu-id="77df3-126">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="77df3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77df3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77df3-128">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="77df3-128">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





