---
title: Imsrdpdevice FriendlyName-Eigenschaft
description: Ruft den anzeigen Amen für das Gerät ab.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- FriendlyName-Eigenschaft Remotedesktopdienste
- FriendlyName-Eigenschaft Remotedesktopdienste, imsrdpdevice-Schnittstelle
- Imsrdpdevice-Schnittstelle Remotedesktopdienste, FriendlyName-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740544"
---
# <a name="imsrdpdevicefriendlyname-property"></a><span data-ttu-id="2c5b8-106">Imsrdpdevice:: FriendlyName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2c5b8-106">IMsRdpDevice::FriendlyName property</span></span>

<span data-ttu-id="2c5b8-107">Ruft den anzeigen Amen für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-107">Retrieves the display name for the device.</span></span>

<span data-ttu-id="2c5b8-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5b8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c5b8-109">Syntax</span></span>


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a><span data-ttu-id="2c5b8-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2c5b8-110">Property value</span></span>

<span data-ttu-id="2c5b8-111">Neuer Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-111">The display name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c5b8-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2c5b8-112">Error codes</span></span>

<span data-ttu-id="2c5b8-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="2c5b8-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c5b8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c5b8-115">Requirements</span></span>



| <span data-ttu-id="2c5b8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c5b8-116">Requirement</span></span> | <span data-ttu-id="2c5b8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2c5b8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5b8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c5b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5b8-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c5b8-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2c5b8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c5b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5b8-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c5b8-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2c5b8-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2c5b8-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c5b8-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c5b8-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c5b8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2c5b8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c5b8-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c5b8-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c5b8-126">IID</span><span class="sxs-lookup"><span data-stu-id="2c5b8-126">IID</span></span><br/>                      | <span data-ttu-id="2c5b8-127">IID \_ imsrdpdevice ist als 60c3b9c8-9E92-4fi5e-a3e7-604a912093ea definiert.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2c5b8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c5b8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5b8-129">**Imsrdpdevice**</span><span class="sxs-lookup"><span data-stu-id="2c5b8-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





