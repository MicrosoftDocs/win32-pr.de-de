---
title: Imsrdpdrive redirectionstate (Eigenschaft)
description: Gibt den Umleitungs Status des Laufwerks an.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Redirectionstate-Eigenschaft Remotedesktopdienste
- Redirectionstate-Eigenschaft Remotedesktopdienste, imsrdpdrive-Schnittstelle
- Imsrdpdrive-Schnittstelle Remotedesktopdienste, redirectionstate-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392075"
---
# <a name="imsrdpdriveredirectionstate-property"></a><span data-ttu-id="20485-106">Imsrdpdrive:: redirectionstate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="20485-106">IMsRdpDrive::RedirectionState property</span></span>

<span data-ttu-id="20485-107">Gibt den Umleitungs Status des Laufwerks an.</span><span class="sxs-lookup"><span data-stu-id="20485-107">Indicates the redirection state of the drive.</span></span>

<span data-ttu-id="20485-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="20485-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="20485-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="20485-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="20485-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="20485-110">Property value</span></span>

<span data-ttu-id="20485-111">Legen Sie diesen Parameter auf **Variant \_ false** fest.</span><span class="sxs-lookup"><span data-stu-id="20485-111">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="20485-112">, wenn Umleitung oder **Variant \_ true** deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="20485-112">to disable redirection or **VARIANT\_TRUE**.</span></span> <span data-ttu-id="20485-113">, um die Umleitung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="20485-113">to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="20485-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="20485-114">Error codes</span></span>

<span data-ttu-id="20485-115">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="20485-115">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="20485-116">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="20485-116">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="20485-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20485-117">Requirements</span></span>



| <span data-ttu-id="20485-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20485-118">Requirement</span></span> | <span data-ttu-id="20485-119">Wert</span><span class="sxs-lookup"><span data-stu-id="20485-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20485-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20485-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20485-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20485-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="20485-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20485-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20485-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20485-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="20485-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="20485-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="20485-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20485-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="20485-126">DLL</span><span class="sxs-lookup"><span data-stu-id="20485-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20485-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20485-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="20485-128">IID</span><span class="sxs-lookup"><span data-stu-id="20485-128">IID</span></span><br/>                      | <span data-ttu-id="20485-129">IID \_ imsrdpdrive ist als d28b5458-f694-47a8-8e61-40356a767e46 definiert.</span><span class="sxs-lookup"><span data-stu-id="20485-129">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="20485-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20485-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20485-131">**Imsrdpdrive**</span><span class="sxs-lookup"><span data-stu-id="20485-131">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





