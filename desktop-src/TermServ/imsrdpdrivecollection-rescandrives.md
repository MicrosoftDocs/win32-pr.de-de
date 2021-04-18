---
title: Imsrdpdrivecollection-Methode
description: Aktualisiert die Liste der-Objekte in der Auflistung. | Imsrdpdrivecollection-Methode
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Methode Remotedesktopdienste wiederholen
- Methode Remotedesktopdienste neu, imsrdpdrivecollection-Schnittstelle
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste, Methode zum erneuten Kopieren
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365027"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a><span data-ttu-id="fac0f-107">Imsrdpdrivecollection:: rescandrives-Methode</span><span class="sxs-lookup"><span data-stu-id="fac0f-107">IMsRdpDriveCollection::RescanDrives method</span></span>

<span data-ttu-id="fac0f-108">Aktualisiert die Liste der-Objekte in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="fac0f-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac0f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fac0f-109">Syntax</span></span>


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="fac0f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fac0f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac0f-111">*vbooldynredir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fac0f-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac0f-112">Der Standard Umleitungs Status, der auf alle neu ermittelten Geräte oder Laufwerke angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fac0f-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac0f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fac0f-113">Return value</span></span>

<span data-ttu-id="fac0f-114">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fac0f-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="fac0f-115">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fac0f-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac0f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fac0f-116">Requirements</span></span>



| <span data-ttu-id="fac0f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fac0f-117">Requirement</span></span> | <span data-ttu-id="fac0f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fac0f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac0f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fac0f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fac0f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fac0f-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fac0f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fac0f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fac0f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fac0f-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fac0f-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fac0f-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="fac0f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac0f-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="fac0f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fac0f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac0f-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac0f-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="fac0f-127">IID</span><span class="sxs-lookup"><span data-stu-id="fac0f-127">IID</span></span><br/>                      | <span data-ttu-id="fac0f-128">IID \_ imsrdpdrivecollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.</span><span class="sxs-lookup"><span data-stu-id="fac0f-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fac0f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fac0f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac0f-130">**Imsrdpdrivecollection**</span><span class="sxs-lookup"><span data-stu-id="fac0f-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





