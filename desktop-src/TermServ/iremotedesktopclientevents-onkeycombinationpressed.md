---
title: Iremotedesktopclientevents-Methode (onkeycombinationpressed)
description: Wird aufgerufen, wenn in der Remote Sitzung Sondertasten Kombinationen gedrückt werden.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Onkeycombinationpressed-Methode Remotedesktopdienste
- Onkeycombinationpressed-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onkeycombinationpressed-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391728"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a><span data-ttu-id="db6d2-106">Iremotedesktopclientevents:: onkeycombinationpressed-Methode</span><span class="sxs-lookup"><span data-stu-id="db6d2-106">IRemoteDesktopClientEvents::OnKeyCombinationPressed method</span></span>

<span data-ttu-id="db6d2-107">Wird aufgerufen, wenn in der Remote Sitzung Sondertasten Kombinationen gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="db6d2-107">Called when special key combinations are pressed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6d2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db6d2-108">Syntax</span></span>


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a><span data-ttu-id="db6d2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db6d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6d2-110">*Tastenkombination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db6d2-110">*keyCombination* \[in\]</span></span>
<span data-ttu-id="db6d2-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="db6d2-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="db6d2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db6d2-112">Return value</span></span>

<span data-ttu-id="db6d2-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="db6d2-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6d2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db6d2-114">Requirements</span></span>



| <span data-ttu-id="db6d2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db6d2-115">Requirement</span></span> | <span data-ttu-id="db6d2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="db6d2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db6d2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db6d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db6d2-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="db6d2-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="db6d2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db6d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db6d2-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db6d2-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="db6d2-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="db6d2-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="db6d2-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6d2-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="db6d2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="db6d2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db6d2-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6d2-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="db6d2-125">IID</span><span class="sxs-lookup"><span data-stu-id="db6d2-125">IID</span></span><br/>                      | <span data-ttu-id="db6d2-126">Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.</span><span class="sxs-lookup"><span data-stu-id="db6d2-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db6d2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db6d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6d2-128">**Iremotedesktopclientevents**</span><span class="sxs-lookup"><span data-stu-id="db6d2-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





