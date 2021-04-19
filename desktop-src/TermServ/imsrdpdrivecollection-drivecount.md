---
title: Imsrdpdrivecollection-drivecount-Eigenschaft
description: Ruft die Anzahl der-Objekte in der-Auflistung ab. | Imsrdpdrivecollection-drivecount-Eigenschaft
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- Drivecount-Eigenschaft Remotedesktopdienste
- Drivecount-Eigenschaft Remotedesktopdienste, imsrdpdrivecollection-Schnittstelle
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste, drivecount-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355772"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a><span data-ttu-id="21dc5-107">Imsrdpdrivecollection::D rivecount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="21dc5-107">IMsRdpDriveCollection::DriveCount property</span></span>

<span data-ttu-id="21dc5-108">Ruft die Anzahl der-Objekte in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="21dc5-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="21dc5-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="21dc5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21dc5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="21dc5-110">Syntax</span></span>


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a><span data-ttu-id="21dc5-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="21dc5-111">Property value</span></span>

<span data-ttu-id="21dc5-112">Die Objekt Anzahl.</span><span class="sxs-lookup"><span data-stu-id="21dc5-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="21dc5-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="21dc5-113">Error codes</span></span>

<span data-ttu-id="21dc5-114">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21dc5-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="21dc5-115">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="21dc5-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="21dc5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21dc5-116">Requirements</span></span>



| <span data-ttu-id="21dc5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21dc5-117">Requirement</span></span> | <span data-ttu-id="21dc5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="21dc5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21dc5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21dc5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="21dc5-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21dc5-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="21dc5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21dc5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="21dc5-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21dc5-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="21dc5-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="21dc5-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="21dc5-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21dc5-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="21dc5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="21dc5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21dc5-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21dc5-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="21dc5-127">IID</span><span class="sxs-lookup"><span data-stu-id="21dc5-127">IID</span></span><br/>                      | <span data-ttu-id="21dc5-128">IID \_ imsrdpdrivecollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.</span><span class="sxs-lookup"><span data-stu-id="21dc5-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21dc5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21dc5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21dc5-130">**Imsrdpdrivecollection**</span><span class="sxs-lookup"><span data-stu-id="21dc5-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





