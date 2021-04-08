---
title: IMsRdpDriveV2 driveletterindex (Eigenschaft)
description: Enthält den Index des Buchstabens für das Laufwerk.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Driveletterindex-Eigenschaft Remotedesktopdienste
- Driveletterindex-Eigenschaft Remotedesktopdienste, IMsRdpDriveV2-Schnittstelle
- IMsRdpDriveV2 Interface Remotedesktopdienste, driveletterindex (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957222"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a><span data-ttu-id="6a75c-106">IMsRdpDriveV2::D riveletterindex (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6a75c-106">IMsRdpDriveV2::DriveLetterIndex property</span></span>

<span data-ttu-id="6a75c-107">Enthält den Index des Buchstabens für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="6a75c-107">Contains the index of the letter for the drive.</span></span>

<span data-ttu-id="6a75c-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6a75c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a75c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a75c-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a><span data-ttu-id="6a75c-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6a75c-110">Property value</span></span>

<span data-ttu-id="6a75c-111">Der Index des Buchstabens für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="6a75c-111">The index of the letter for the drive.</span></span> <span data-ttu-id="6a75c-112">0 = "A", 1 = "B" usw.</span><span class="sxs-lookup"><span data-stu-id="6a75c-112">0 = "A", 1 = "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a75c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a75c-113">Requirements</span></span>



| <span data-ttu-id="6a75c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a75c-114">Requirement</span></span> | <span data-ttu-id="6a75c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6a75c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a75c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a75c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a75c-117">Windows 7 mit SP1</span><span class="sxs-lookup"><span data-stu-id="6a75c-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="6a75c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a75c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a75c-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a75c-119">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="6a75c-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6a75c-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a75c-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a75c-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a75c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6a75c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a75c-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a75c-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a75c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a75c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a75c-125">**IMsRdpDriveV2**</span><span class="sxs-lookup"><span data-stu-id="6a75c-125">**IMsRdpDriveV2**</span></span>](imsrdpdrivev2.md)
</dt> </dl>

 

 





