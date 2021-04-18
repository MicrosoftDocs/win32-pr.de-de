---
title: IMsRdpClientSecuredSettings2 (Eigenschaft)
description: Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll. | IMsRdpClientSecuredSettings2 (Eigenschaft)
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Platine-Eigenschaft
- Eigenschaften Remotedesktopdienste der Platine, IMsRdpClientSecuredSettings2-Schnittstelle
- IMsRdpClientSecuredSettings2-Schnittstelle Remotedesktopdienste, Eigenschaft ' PCB '
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365059"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a><span data-ttu-id="c4967-107">IMsRdpClientSecuredSettings2::P CB-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4967-107">IMsRdpClientSecuredSettings2::PCB property</span></span>

<span data-ttu-id="c4967-108">Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4967-108">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="c4967-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c4967-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4967-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4967-110">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="c4967-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c4967-111">Property value</span></span>

<span data-ttu-id="c4967-112">Die Einstellung für die Festplatte.</span><span class="sxs-lookup"><span data-stu-id="c4967-112">The PCB setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4967-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4967-113">Requirements</span></span>



| <span data-ttu-id="c4967-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4967-114">Requirement</span></span> | <span data-ttu-id="c4967-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c4967-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4967-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4967-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c4967-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c4967-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="c4967-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4967-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c4967-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4967-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c4967-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c4967-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4967-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4967-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4967-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c4967-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4967-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4967-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4967-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4967-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4967-125">**IMsRdpClientSecuredSettings2**</span><span class="sxs-lookup"><span data-stu-id="c4967-125">**IMsRdpClientSecuredSettings2**</span></span>](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





