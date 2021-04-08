---
title: Controlclosestatus-Enumeration
description: Gibt an, ob die Anwendung, die das Steuerelement enthält, das Steuerelement sofort schließen kann
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Controlclosestatus-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949511"
---
# <a name="controlclosestatus-enumeration"></a><span data-ttu-id="11a4b-104">Controlclosestatus-Enumeration</span><span class="sxs-lookup"><span data-stu-id="11a4b-104">ControlCloseStatus enumeration</span></span>

<span data-ttu-id="11a4b-105">Gibt an, ob die Anwendung, die das Steuerelement enthält, das Steuerelement sofort schließen kann</span><span class="sxs-lookup"><span data-stu-id="11a4b-105">Indicates whether the application containing the control can close the control immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a4b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11a4b-106">Syntax</span></span>


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a><span data-ttu-id="11a4b-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="11a4b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="11a4b-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlclosecanfortsetzung**</span><span class="sxs-lookup"><span data-stu-id="11a4b-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span></span>
</dt> <dd>

<span data-ttu-id="11a4b-109">Der Container kann sofort geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="11a4b-109">Container can go ahead with close immediately.</span></span> <span data-ttu-id="11a4b-110">Dies kann vorkommen, wenn das Steuerelement nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="11a4b-110">This can happen if the control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="11a4b-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlclosewaitforevents**</span><span class="sxs-lookup"><span data-stu-id="11a4b-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span></span>
</dt> <dd>

<span data-ttu-id="11a4b-112">Der Container sollte auf Ereignisse mit [**imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md) oder [**imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md)warten.</span><span class="sxs-lookup"><span data-stu-id="11a4b-112">Container should wait for events [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) or [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11a4b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11a4b-113">Requirements</span></span>



| <span data-ttu-id="11a4b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11a4b-114">Requirement</span></span> | <span data-ttu-id="11a4b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="11a4b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11a4b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11a4b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11a4b-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="11a4b-117">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="11a4b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11a4b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11a4b-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="11a4b-119">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="11a4b-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="11a4b-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="11a4b-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11a4b-121"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11a4b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11a4b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a4b-123">**Imsrdpclient:: RequestClose**</span><span class="sxs-lookup"><span data-stu-id="11a4b-123">**IMsRdpClient::RequestClose**</span></span>](imsrdpclient-requestclose.md)
</dt> <dt>

[<span data-ttu-id="11a4b-124">**Imstscaxevents:: onconfirmclose**</span><span class="sxs-lookup"><span data-stu-id="11a4b-124">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="11a4b-125">**Imstscaxevents:: ongetrennte**</span><span class="sxs-lookup"><span data-stu-id="11a4b-125">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





