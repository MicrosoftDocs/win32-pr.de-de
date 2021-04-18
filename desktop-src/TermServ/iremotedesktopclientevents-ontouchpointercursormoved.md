---
title: Iremotedesktopclientevents ontouchpointercurrsorverschote-Methode
description: Wird aufgerufen, wenn der Fingerabdruck Cursor verschoben wurde und die EventsEnabled-Eigenschaft auf true festgelegt ist.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- Ontouchpointercursor-Methode Remotedesktopdienste
- Ontouchpointercurrsorverschoder Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, ontouchpointercurrsorverschote-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338336"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a><span data-ttu-id="454af-106">Iremotedesktopclientevents:: ontouchpointercurrsorverschote-Methode</span><span class="sxs-lookup"><span data-stu-id="454af-106">IRemoteDesktopClientEvents::OnTouchPointerCursorMoved method</span></span>

<span data-ttu-id="454af-107">Wird aufgerufen, wenn der Fingerabdruck Cursor verschoben wurde und die [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) -Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="454af-107">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

## <a name="syntax"></a><span data-ttu-id="454af-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="454af-108">Syntax</span></span>


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a><span data-ttu-id="454af-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="454af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="454af-110">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="454af-110">*x* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="454af-111">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="454af-111">*y* \[in\]</span></span>
<span data-ttu-id="454af-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="454af-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="454af-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="454af-113">Return value</span></span>

<span data-ttu-id="454af-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="454af-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="454af-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="454af-115">Requirements</span></span>



| <span data-ttu-id="454af-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="454af-116">Requirement</span></span> | <span data-ttu-id="454af-117">Wert</span><span class="sxs-lookup"><span data-stu-id="454af-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="454af-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="454af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="454af-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="454af-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="454af-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="454af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="454af-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="454af-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="454af-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="454af-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="454af-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="454af-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="454af-124">DLL</span><span class="sxs-lookup"><span data-stu-id="454af-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="454af-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="454af-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="454af-126">IID</span><span class="sxs-lookup"><span data-stu-id="454af-126">IID</span></span><br/>                      | <span data-ttu-id="454af-127">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="454af-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="454af-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="454af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="454af-129">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="454af-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

