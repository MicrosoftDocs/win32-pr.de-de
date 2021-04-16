---
title: Imsrdpdevice redirectionstate (Eigenschaft)
description: Gibt den Umleitungs Status des Geräts an.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Redirectionstate-Eigenschaft Remotedesktopdienste
- Redirectionstate-Eigenschaft Remotedesktopdienste, imsrdpdevice-Schnittstelle
- Imsrdpdevice-Schnittstelle Remotedesktopdienste, redirectionstate-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476452"
---
# <a name="imsrdpdeviceredirectionstate-property"></a><span data-ttu-id="1200f-106">Imsrdpdevice:: redirectionstate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1200f-106">IMsRdpDevice::RedirectionState property</span></span>

<span data-ttu-id="1200f-107">Gibt den Umleitungs Status des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="1200f-107">Indicates the redirection state of the device.</span></span>

<span data-ttu-id="1200f-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1200f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1200f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1200f-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="1200f-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1200f-110">Property value</span></span>

<span data-ttu-id="1200f-111">Legen Sie diesen Parameter auf **Variant \_ false** fest, um die Umleitung zu deaktivieren oder **Variant \_ true** zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="1200f-111">Set this parameter to **VARIANT\_FALSE** to disable redirection or **VARIANT\_TRUE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1200f-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1200f-112">Error codes</span></span>

<span data-ttu-id="1200f-113">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1200f-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="1200f-114">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1200f-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1200f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1200f-115">Requirements</span></span>



| <span data-ttu-id="1200f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1200f-116">Requirement</span></span> | <span data-ttu-id="1200f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1200f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1200f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1200f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1200f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1200f-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1200f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1200f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1200f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1200f-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1200f-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1200f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="1200f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1200f-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1200f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1200f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1200f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1200f-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1200f-126">IID</span><span class="sxs-lookup"><span data-stu-id="1200f-126">IID</span></span><br/>                      | <span data-ttu-id="1200f-127">IID \_ imsrdpdevice ist als 60c3b9c8-9E92-4fi5e-a3e7-604a912093ea definiert.</span><span class="sxs-lookup"><span data-stu-id="1200f-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="1200f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1200f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1200f-129">**Imsrdpdevice**</span><span class="sxs-lookup"><span data-stu-id="1200f-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





