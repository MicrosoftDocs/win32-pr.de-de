---
title: Imsrdpdrivecollection (drivebyindex-Eigenschaft)
description: Ruft das Laufwerk am angegebenen Index ab.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Drivebyindex-Eigenschaft Remotedesktopdienste
- Drivebyindex-Eigenschaft Remotedesktopdienste, imsrdpdrivecollection-Schnittstelle
- Imsrdpdrivecollection-Schnittstelle Remotedesktopdienste, drivebyindex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392074"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a><span data-ttu-id="56d63-106">Imsrdpdrivecollection::D rivebyindex-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56d63-106">IMsRdpDriveCollection::DriveByIndex property</span></span>

<span data-ttu-id="56d63-107">Ruft das Laufwerk am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="56d63-107">Retrieves the drive at the specified index.</span></span>

<span data-ttu-id="56d63-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="56d63-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d63-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="56d63-109">Syntax</span></span>


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="56d63-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="56d63-110">Property value</span></span>

<span data-ttu-id="56d63-111">Ein [**imsrdpdrive**](imsrdpdrive.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="56d63-111">An [**IMsRdpDrive**](imsrdpdrive.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56d63-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="56d63-112">Error codes</span></span>

<span data-ttu-id="56d63-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="56d63-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="56d63-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="56d63-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="56d63-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56d63-115">Requirements</span></span>



| <span data-ttu-id="56d63-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56d63-116">Requirement</span></span> | <span data-ttu-id="56d63-117">Wert</span><span class="sxs-lookup"><span data-stu-id="56d63-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56d63-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56d63-118">Minimum supported client</span></span><br/> | <span data-ttu-id="56d63-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56d63-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="56d63-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56d63-120">Minimum supported server</span></span><br/> | <span data-ttu-id="56d63-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56d63-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="56d63-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="56d63-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="56d63-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d63-123"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="56d63-124">DLL</span><span class="sxs-lookup"><span data-stu-id="56d63-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56d63-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d63-125"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="56d63-126">IID</span><span class="sxs-lookup"><span data-stu-id="56d63-126">IID</span></span><br/>                      | <span data-ttu-id="56d63-127">IID \_ imsrdpdrivecollection ist als 7ff17599-da2c-4677-ad35-f60c04fe1585 definiert.</span><span class="sxs-lookup"><span data-stu-id="56d63-127">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56d63-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56d63-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d63-129">**Imsrdpdrivecollection**</span><span class="sxs-lookup"><span data-stu-id="56d63-129">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





