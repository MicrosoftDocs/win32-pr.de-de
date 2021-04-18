---
title: Iremotedesktopclientevents-Methode (onadminmessagereceived)
description: Wird aufgerufen, wenn das Client Steuerelement eine administrative Nachricht empfängt.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- Onadminmessagereceived-Methode Remotedesktopdienste
- Onadminmessagereceived-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onadminmessagereceived-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392071"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a><span data-ttu-id="549f4-106">Iremotedesktopclientevents:: onadminmessagereceived-Methode</span><span class="sxs-lookup"><span data-stu-id="549f4-106">IRemoteDesktopClientEvents::OnAdminMessageReceived method</span></span>

<span data-ttu-id="549f4-107">Wird aufgerufen, wenn das Client Steuerelement eine administrative Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="549f4-107">Called when the client control receives an administrative message.</span></span>

## <a name="syntax"></a><span data-ttu-id="549f4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="549f4-108">Syntax</span></span>


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a><span data-ttu-id="549f4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="549f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="549f4-110">*AdminMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="549f4-110">*adminMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="549f4-111">Die Meldung.</span><span class="sxs-lookup"><span data-stu-id="549f4-111">The message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="549f4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="549f4-112">Return value</span></span>

<span data-ttu-id="549f4-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="549f4-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="549f4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="549f4-114">Requirements</span></span>



| <span data-ttu-id="549f4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="549f4-115">Requirement</span></span> | <span data-ttu-id="549f4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="549f4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549f4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="549f4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="549f4-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="549f4-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="549f4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="549f4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="549f4-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="549f4-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="549f4-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="549f4-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="549f4-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="549f4-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="549f4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="549f4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="549f4-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="549f4-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="549f4-125">IID</span><span class="sxs-lookup"><span data-stu-id="549f4-125">IID</span></span><br/>                      | <span data-ttu-id="549f4-126">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="549f4-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="549f4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="549f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549f4-128">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="549f4-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





